# Feature: confirm a workshop booking

**Status:** Defined in a fictional scenario; not implemented  
**Version:** v0.2, including [D-02](build-finding.md)  
**Decision:** [D-01](decision.md)

## Intent and entry conditions

A signed-in visitor wants one confirmed place in a selected session. Session details exist, and the visitor can return to the session list. Authentication and session browsing are assumed capabilities.

## Requirements

| ID | Required behavior |
| --- | --- |
| R1 | Review shows session title, date, time with timezone, location, and one-place quantity. It explains that availability is confirmed on submission. |
| R2 | The service checks capacity and commits the booking as one protected operation. Two competing requests for the last place cannot both succeed. |
| R3 | Show success only for a confirmed booking, including its reference and session details. The same visitor cannot acquire a second place in the same session by repeating the action. |
| R4 | If the session is full, explain that no place was booked and offer other sessions. Preserve the selected session details for context. |
| R5 | While submitting, prevent additional confirmation actions in the interface and expose a textual pending state. |
| R6 | If the response is lost or times out, preserve the attempt identity and show “Checking your booking.” Retrieve that attempt's outcome; do not assume failure or create a fresh attempt. If checking fails, offer “Check again” using the same identity. |
| R7 | A resolved attempt displays either its confirmed booking or its authoritative rejection. Only after a confirmed rejection with no booking may a visitor start a new attempt if the session permits it. A pending or unknown result remains in the checking state. |
| R8 | Booking creation and result retrieval require authorization for the current visitor. An expired session requires sign-in before checking resumes; retain enough attempt context to resume safely. Another account cannot retrieve the booking. |
| R9 | All actions work by keyboard. Announce pending and resolved outcomes without repeated announcements during polling. On a new outcome view, place focus at its heading. Present errors in text, not color alone. |
| R10 | At narrow widths and 200% zoom, keep session information and actions readable without overlapping or hiding recovery controls. |

R6–R8 incorporate the simulated build finding. The service must support equivalent guarantees before implementation can be called ready.

## States and recovery

| State | Visitor sees | Available action |
| --- | --- | --- |
| Review | Session details and provisional availability | Confirm or return to sessions |
| Submitting | Booking in progress | Wait; duplicate confirm is unavailable |
| Checking | Result is not yet known | Automatic check; Check again after a failed check |
| Authentication required | Sign-in is needed to resolve the attempt | Sign in, then resume checking |
| Confirmed | Booking reference and session details | Return to sessions |
| Full / rejected | Explicit explanation that no booking was created | Choose another session; retry only when eligible under R7 |

## Scope and remaining questions

Included: one-place booking, competing capacity requests, unknown outcomes, authorization, and accessible recovery.

Excluded: payments, cancellation, waitlists, multi-place bookings, and changes to authentication itself.

Engineering must establish the attempt identity, result lookup, persistence, and retention contract. Product and engineering must agree how a still-unresolved attempt is handled after the service's retention window. This is a readiness blocker for release, not permission to label an unknown outcome as failed.

## Success signals to investigate after release

Check whether visitors can distinguish provisional availability from confirmation, recover unknown results without repeated bookings, and understand a full-session response. Choose measurement methods before release; this example contains no measured outcomes.
