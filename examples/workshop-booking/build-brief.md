# Build increment: confirmation and recovery

**Status:** Draft; fictional, not implemented  
**Specification:** [Feature definition v0.2](feature-definition.md)  
**Decisions:** [D-01](decision.md), [D-02](build-finding.md)

## Scope

Implement R1–R10 as one coherent booking increment. Recovery is part of the booking capability, not a later enhancement.

The scenario assumes session browsing and authentication already exist. Actual source paths, components, APIs, and tests must be inspected in a real project; none are claimed here.

## Dependencies and blockers

- Verify that capacity checking and booking creation cannot overbook under concurrent requests.
- Establish an authorized result lookup and stable attempt identity with duplicate prevention.
- Define persistence across sign-in and reload.
- Agree retention and support behavior for attempts that remain unresolved.
- Identify reusable UI components and the project's visual references.

This brief remains Draft until those dependencies are settled. The proposed checks below have not been executed.

## Verification plan

| Requirement | Scenario | Expected result | Evidence |
| --- | --- | --- | --- |
| R1 | Review a session | Required details and provisional-availability explanation are present | Not run |
| R2, R4 | Two visitors confirm the final place concurrently | Exactly one booking; the other visitor receives a full result | Not run |
| R3, R5 | Repeat confirmation rapidly and replay the same attempt | At most one booking; pending feedback is visible | Not run |
| R6, R7 | Service commits but its response is lost | Checking resolves to that booking; no fresh attempt is created | Not run |
| R6, R7 | Result lookup fails, then succeeds | Check again retains attempt identity and displays the authoritative result | Not run |
| R7 | Service rejects without creating a booking | Rejection is clear; any new eligible attempt is separate | Not run |
| R6, R8 | Reload while the outcome is unknown | Preserved attempt context resumes authorized checking without a new booking | Not run |
| R8 | Session expires while resolving; visitor signs in again | Authorized checking resumes for the preserved attempt | Not run |
| R8 | Another account requests the attempt result | No booking details are disclosed | Not run |
| R9 | Complete and recover using a keyboard and screen reader | Actions, focus, and announcements follow the specification | Not run |
| R10 | Review every state at narrow widths and 200% zoom | Content and recovery actions remain usable | Not run |

## Out of scope

Payments, waitlists, cancellation, multi-place booking, and a redesign of browsing or sign-in.

## Completion record

No implementation, test execution, or release has occurred. In a real project, link the implementation and replace Not run with actual results, including failures and unperformed checks.

The [simulated finding](build-finding.md) explains why the verification plan includes a lost response after successful booking.
