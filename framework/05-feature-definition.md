# Feature Definition

Feature definition turns a product opportunity into a clear description of **what the experience needs to do and why**.

It sits between high-level product thinking and detailed implementation.

The goal is not to prescribe every screen upfront.

The goal is to make the intended behavior, rules, states, and boundaries clear enough that design and development can move forward without relying on assumptions.

---

## Feature

### [Feature or capability name]

**Status:** Exploring / Defined / In Build / Shipped
**Owner:**
**Related decision(s):**
**Related work:**

---

## Problem

What problem are we solving?

Describe the user or system problem rather than the proposed interface.

*

---

## User intent

What is the person actually trying to accomplish?

Avoid describing interface actions such as:

> Click the button to submit the form.

Instead describe the underlying intent:

> Confirm that the information is correct and move the request forward.

### Primary intent

*

### Secondary intents

*

---

## Why this matters

Why should this problem be addressed now?

Consider:

* Customer impact

* Business impact

* Operational impact

* Product strategy

* Existing friction

* New capability or dependency

* Evidence from research or behavior

*

---

## Entry conditions

What must already be true before someone can use or encounter this feature?

Examples:

* Signed in

* Has an existing project

* Has permission to perform the action

* Has reached a particular product state

* Required information already exists

* Another workflow has been completed

*

---

## Desired outcome

What should be true when the experience works successfully?

For the person:

*

For the product or business:

*

---

## Core flow

Describe the simplest successful path.

Keep this focused on behavior rather than screen layout.

```text
Entry
  ↓
Understand current state
  ↓
Take action
  ↓
Review consequence
  ↓
Confirm
  ↓
Updated state
```

### Happy path

1.
2.
3.
4.

---

## Key decisions

What decisions does the person need to make?

| Decision | Information needed | Product responsibility |
| -------- | ------------------ | ---------------------- |
|          |                    |                        |
|          |                    |                        |

The product should provide enough information for someone to make the decision without requiring them to understand internal system logic.

---

## Business rules

What rules determine how the feature behaves?

Examples:

* Eligibility
* Quantity limits
* Pricing rules
* Timing
* Availability
* Permissions
* Required information
* Dependencies
* Cancellation behavior

### Rules

1.
2.
3.

If a rule is complicated, explain **why it exists** when that context will help future decisions.

---

## States

What states meaningfully change the experience?

| State   | What the person sees | Available actions |
| ------- | -------------------- | ----------------- |
| Default |                      |                   |
|         |                      |                   |
|         |                      |                   |

Consider:

* Empty
* Loading
* Success
* Error
* Partial completion
* Pending
* Approved
* Rejected
* Expired
* Unavailable
* Changed externally

Only document states that materially affect behavior.

---

## Edge cases

What happens outside the ideal path?

Consider situations such as:

* Required information is missing
* Availability changes
* Another person changes the same object
* The action becomes invalid
* A dependency fails
* Someone returns later
* The user has partial progress
* The system receives conflicting information

| Scenario | Expected behavior |
| -------- | ----------------- |
|          |                   |
|          |                   |

Prioritize meaningful exceptions rather than trying to imagine every theoretical failure.

---

## Errors and recovery

When something goes wrong:

**What happened?**

*

**What does the person need to understand?**

*

**What can they do next?**

*

Whenever possible, design for recovery rather than stopping the workflow.

---

## Information requirements

What information needs to be:

### Shown

*

### Collected

*

### Remembered

*

### Derived by the system

*

Avoid asking people for information the system already knows or can reasonably infer.

---

## Dependencies

What does this feature depend on?

Consider:

* Other product capabilities
* Data
* APIs
* Permissions
* Content
* Operational processes
* Third-party systems
* Decisions that haven't been made yet

### Dependencies

*

---

## Experience requirements

What qualities need to remain true regardless of the final interface?

Examples:

* The primary action is obvious
* Consequential changes are confirmed
* Existing progress is preserved
* Status is understandable without internal terminology
* Important changes are visible before commitment
* The experience works across relevant screen sizes

### Requirements

*

---

## Accessibility considerations

Identify requirements that should be considered before implementation rather than added afterward.

Consider:

* Keyboard interaction
* Focus behavior
* Screen-reader context
* Error identification
* Color-independent meaning
* Dynamic updates
* Touch target size
* Reduced motion
* Content clarity

### Considerations

*

---

## Out of scope

What related problems are intentionally **not** being solved here?

This helps prevent a clearly defined feature from quietly expanding during design or implementation.

*

---

## Open questions

What still needs to be resolved?

| Question | Needed to move forward? | Owner |
| -------- | ----------------------- | ----- |
|          | Yes / No                |       |
|          | Yes / No                |       |

Not every question needs to be answered before work begins.

Separate true blockers from things that can be learned later.

---

## Success signals

What would indicate that the feature is helping?

Consider:

* Completion
* Comprehension
* Reduced effort
* Reduced errors
* Adoption
* Customer feedback
* Operational burden
* Business outcomes

### Signals

*

---

## Ready for build when

Before translating the feature into implementation work, confirm that:

* The problem and intended outcome are clear
* The core flow is understood
* Important rules are defined
* Meaningful states are accounted for
* Major edge cases have expected behaviors
* Blocking questions are resolved
* Scope boundaries are explicit
* Design intent can be explained without relying solely on mockups

The goal is not perfect certainty.

**The goal is to remove the ambiguity that would otherwise become accidental product decisions during implementation.**
