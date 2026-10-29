# Worked example: booking a workshop

**Fictional teaching example.** This scenario, its constraints, and the simulated build finding are invented. Nothing here represents a shipped product, user research, or measured results.

A community learning center offers free workshops with limited places. A visitor chooses a session, reviews the details, and confirms a booking.

## Problem and constraints

The product needs to let people book without implying that a place is guaranteed before confirmation. In this scenario:

- Visitors sign in before booking.
- Each booking reserves one place.
- Capacity can change while someone reviews a session.
- The center's existing service can commit a booking only if capacity remains.
- Checkout holds are not available.
- Payments, waitlists, and cancellation are outside this example.

The working assumption is that showing current availability and explaining confirmation will help visitors understand their booking status. This has not been tested.

## Experience principle

**Show commitment accurately.** Before confirmation, describe availability as provisional. After the system confirms a booking, show an unambiguous receipt. If the result is unknown, explain that uncertainty and help the visitor resolve it.

This principle favors accurate status over an optimistic success message.

## Experience model

| Stage | Visitor intent | Product capability | System dependency |
| --- | --- | --- | --- |
| Choose | Find a suitable session | Show session details and current availability | Read session capacity |
| Review | Check the commitment | Show date, time, location, and provisional availability | Refresh session details |
| Confirm | Reserve one place | Commit a booking if a place remains | Capacity enforcement and authenticated ownership |
| Resolve | Understand the result | Show confirmed, full, or checking status | Retrieve the result of the same booking attempt |

A session's availability and a person's booking status are separate concepts. A session can become full while the person's booking is successfully confirmed.

## Follow the work

1. [Decision D-01](decision.md): choose confirmation-time capacity checks instead of promising a place during review.
2. [Feature definition](feature-definition.md): define the rules and recovery behavior.
3. [Build brief](build-brief.md): select the first increment and map verification to requirements.
4. [Simulated build finding](build-finding.md): show how a timeout exposes a missing product decision and changes the definition.

The feature definition and build brief show the revised v0.2 target. The finding records what changed from v0.1.

## What this example demonstrates

The decision explains why availability remains provisional. Requirements specify what happens when capacity changes. The build brief references those requirements. A simulated timeout finding then expands recovery behavior without inventing an implementation result.

After a real release, a learning log could compare expectations with observed status comprehension, failed attempts, and support questions. No such outcomes are claimed here.
