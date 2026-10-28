# D-01: Confirm capacity when the booking is submitted

**Status:** Accepted within the fictional scenario  
**Applies to:** [Feature definition](feature-definition.md), R1–R4  
**Evidence basis:** Invented scenario constraints; no user research

## Decision

A place is committed only when the booking service confirms it. Review screens describe availability as provisional. If the last place is taken before confirmation, the visitor gets an explicit full-session response and a route back to other sessions.

## Options and tradeoffs

| Option | Benefit | Cost or constraint |
| --- | --- | --- |
| Hold a place during review | Greater certainty while reviewing | Requires hold expiry and recovery behavior; unavailable in the assumed service |
| Check capacity at confirmation | Works with the assumed service and avoids abandoned holds | Someone may lose the last place while reviewing |
| Display success before the service confirms | Immediate feedback | Can falsely imply a reservation; conflicts with the experience principle |

Choose the confirmation-time check. The additional uncertainty is acceptable only if the interface explains when a place becomes committed and handles the full-session outcome clearly.

## Implications

- Availability shown before submission is informational.
- Capacity must be enforced by the service; disabling a button alone cannot prevent overbooking.
- Success requires a confirmed booking result.
- A full response preserves session context and offers other sessions.

## What remains separate

This decision does not define payments, cancellation, waitlists, or how to recover an unknown submission result. The latter is resolved by [D-02 in the simulated build finding](build-finding.md).

## Revisit when

Revisit if a hold capability becomes available or real evidence shows that confirmation-time loss causes substantial confusion or abandonment. Those are evaluation conditions, not observed findings.
