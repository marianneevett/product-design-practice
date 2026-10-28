# Build Brief

A build brief scopes an implementation increment and explains how to verify it.

The [feature definition](05-feature-definition.md) owns product behavior. Reference its requirements here rather than copying rules, states, flows, or accessibility specifications into a second source of truth.

For a small change without a separate feature definition, put the required behavior directly in the issue or brief. Keep the documentation proportional to the decision.

## Increment

### [Name]

**Status:** Draft / Ready for Build / In Build / QA / Shipped  
**Feature definition and version:**  
**Related decisions:**  
**Design references:**  
**Implementation / issue / PR:**  

Reference a reviewed commit or document version when a build depends on a specific specification. If requirements change during implementation, update the references and affected checks.

## Outcome and scope

What will this increment make possible?

| Requirement reference | Included in this increment? | Delivery note |
| --- | --- | --- |
| [Link or requirement ID] | Yes / No | Dependencies, sequencing, or agreed deferral |

Identify deferred requirements explicitly. An increment must leave a coherent experience; defer a whole capability if omitting its recovery or access behavior would make it unsafe or unusable.

## Current implementation

Describe relevant behavior that exists today. Include paths or links to components, services, data models, and tests after inspecting the project.

Distinguish verified behavior from assumptions. Do not mark a proposed capability as implemented.

## Reuse and preserve

What existing components, tokens, contracts, or behavior should this work reuse or preserve? Link to their authoritative locations.

## Dependencies and readiness

| Dependency or open question | Owner | Blocks this increment? | Resolution |
| --- | --- | --- | --- |
| | | Yes / No | |

Include availability of APIs, content, permissions, data, and designs where relevant. Product behavior required by this increment must be settled before marking it Ready for Build.

## Implementation considerations

Record known delivery constraints, compatibility requirements, and integration boundaries.

Engineering chooses the implementation within those boundaries. If a technical limitation changes user-visible behavior, resolve it with the product owner and update the feature definition before building that change.

## Acceptance and verification

Map checks to the source requirements so coverage is visible without maintaining a second specification.

| Requirement reference | Scenario / action | Expected observable result | Evidence |
| --- | --- | --- | --- |
| | | | Not run / result and link |

Cover relevant primary flows, alternate states, failure recovery, permissions, responsive behavior, and accessibility. Include regression checks for behavior this increment could affect.

Expected results are verification targets. Record actual results separately; a written test plan is not evidence that a check passed.

## Out of scope

List adjacent work excluded from this increment. Link to its owning requirement or issue where useful.

## Findings during build

| Finding | Product behavior affected? | Decision / resolution | Documents and checks updated |
| --- | --- | --- | --- |
| | Yes / No | | |

An implementation question can remain an engineering decision when it preserves the specified experience. A new product question should be resolved explicitly rather than silently becoming behavior.

## Completion record

- Implemented requirements and any agreed deferrals:
- Verification performed and evidence:
- Known limitations:
- Updated specification and decision references:
- Follow-up observation or [learning log](07-learning-log.md):

Use Shipped only after release. Record what actually happened, including checks that remain unperformed.
