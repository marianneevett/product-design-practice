# Simulated build finding: a timeout does not establish failure

**Type:** Fictional implementation exercise  
**Status:** Proposed behavior resolved in the example; implementation unverified

## Initial v0.1 assumption

The initial concept treated any failed submission response as a failed booking and offered a fresh retry.

## Simulated finding

Consider this sequence: the service commits the last place, but the response never reaches the browser. The browser cannot tell whether the booking succeeded.

A fresh retry could produce a misleading full-session message even though the visitor already has a booking. Client-side button disabling does not resolve this ambiguity.

This is a hypothetical walkthrough, not the result of an executed test.

## D-02: Resolve the original attempt before allowing another

**Status:** Accepted within the fictional scenario

Preserve the booking attempt's identity and check its authoritative result. Keep the visitor in an explicit checking state while the outcome remains unknown. Require authorized lookup and duplicate prevention.

| Alternative | Tradeoff |
| --- | --- |
| Treat a timeout as failure | Simple UI, but can misstate a successful booking |
| Treat a timeout as success | Reassuring, but can promise a place that does not exist |
| Resolve the original attempt | Accurate recovery, with additional service and interface requirements |

The third option follows the principle of showing commitment accurately. Engineering can choose the mechanism, provided it preserves these guarantees.

## Changes to the specification and build

- Feature definition v0.2 adds R6–R8 and explicit checking and authentication-required states.
- The build brief adds lost-response, lookup-retry, and cross-account access checks.
- Release readiness now depends on the result-lookup and retention contract.
- D-01 remains valid: capacity is still confirmed at submission.

## What has not been established

No evidence yet shows whether visitors understand the checking language or how often they would encounter it. A real release would need operational observation and user feedback before claiming this recovery improves outcomes.
