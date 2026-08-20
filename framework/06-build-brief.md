# Build Brief

A build brief translates product and design intent into a clear implementation target.

It sits between feature definition and development.

The goal is not to prescribe how the system must be engineered.

The goal is to make the intended experience explicit enough that a developer — or an AI coding agent — can implement it without filling important product gaps with assumptions.

---

## Feature

### [Feature or capability name]

**Status:** Ready for Build / In Build / QA / Shipped
**Related feature definition:**
**Related decision(s):**
**Design reference:**

---

## Goal

What are we building, and what should become possible because it exists?

Describe the intended outcome in plain language.

*

---

## Existing behavior

What happens today?

Include existing functionality that should:

* Remain unchanged
* Be modified
* Be removed
* Be reused

### Current behavior

*

---

## Desired behavior

What should happen after this work is complete?

Focus on observable product behavior.

*

---

## User flow

Describe the expected sequence from entry through completion.

```text
Entry
  ↓
Current state
  ↓
User action
  ↓
System response
  ↓
Updated state
```

### Primary flow

1.
2.
3.
4.

---

## Interaction requirements

Define important interaction behavior that should survive implementation.

Consider:

* Primary and secondary actions
* Confirmation behavior
* Progressive disclosure
* Selection behavior
* Editing
* Navigation
* Save behavior
* Feedback
* Loading
* Focus
* Return states

### Requirements

*

---

## Business rules

List the rules implementation must respect.

| Rule | Expected behavior |
| ---- | ----------------- |
|      |                   |
|      |                   |

Avoid leaving product rules implicit in mockups.

---

## States

Define the meaningful product states and what should happen in each.

| State   | What is shown | Available actions |
| ------- | ------------- | ----------------- |
| Default |               |                   |
| Loading |               |                   |
| Empty   |               |                   |
| Error   |               |                   |
| Success |               |                   |

Add feature-specific states as needed.

---

## Edge cases

Document exceptions that would otherwise require implementation-time interpretation.

| Scenario | Expected behavior |
| -------- | ----------------- |
|          |                   |
|          |                   |

Focus on cases with meaningful product consequences.

---

## Data requirements

What information does the experience depend on?

### Read

What existing information needs to be retrieved?

*

### Write

What information needs to be created or updated?

*

### Persist

What needs to remain available across sessions, screens, or states?

*

### Derived

What should the system calculate or infer rather than asking the user to provide?

*

---

## Permissions and access

Who can:

* View this?
* Create it?
* Change it?
* Approve it?
* Delete or cancel it?

| Role | Access |
| ---- | ------ |
|      |        |
|      |        |

If access changes by state, document that explicitly.

---

## Content requirements

Identify copy that carries product meaning rather than leaving it to implementation.

Consider:

* Labels
* Status names
* Error messages
* Empty states
* Confirmation language
* Helper text
* System notifications

### Required content

*

---

## Responsive behavior

What should change across screen sizes?

Define behavior rather than exact pixel values unless those values are meaningful requirements.

Consider:

* Layout changes
* Stacking
* Navigation
* Tables
* Overflow
* Touch interaction
* Content priority
* Persistent actions

### Requirements

*

---

## Accessibility requirements

Define accessibility behavior that implementation should preserve.

Consider:

* Semantic structure
* Keyboard access
* Focus order
* Focus management
* Screen-reader labels
* Error association
* Dynamic announcements
* Touch targets
* Reduced motion
* Non-color indicators

### Requirements

*

---

## Dependencies

What must already exist or be resolved?

Consider:

* APIs
* Data structures
* Authentication
* Permissions
* Existing components
* Other features
* Third-party services
* Content
* Product decisions

### Dependencies

*

---

## Preserve

What existing behavior, system, component, or design pattern should **not** be changed as part of this work?

This is especially useful when working inside an existing product or using AI-assisted development.

*

---

## Out of scope

What should implementation intentionally leave alone?

*

---

## Acceptance criteria

Describe what must be true for the work to be considered complete.

Use observable behavior rather than implementation details.

* [ ]
* [ ]
* [ ]
* [ ]

---

## QA scenarios

What should be explicitly tested before shipping?

### Primary path

* [ ]

### Alternate states

* [ ]

### Edge cases

* [ ]

### Responsive

* [ ]

### Accessibility

* [ ]

---

## Open implementation questions

Questions discovered during build should be surfaced rather than silently resolved when they affect product behavior.

| Question | Product decision needed? | Resolution |
| -------- | ------------------------ | ---------- |
|          | Yes / No                 |            |
|          | Yes / No                 |            |

Technical implementation choices that don't change the experience can remain engineering decisions.

---

## Build principle

Implementation inevitably reveals details that weren't obvious during design.

That is useful.

The goal isn't to eliminate every question before development begins.

It is to distinguish between:

**implementation decisions** — how something should be built

and

**product decisions** — how something should behave

When implementation uncovers a product decision, bring it back into the decision-making process rather than allowing the product to change accidentally.

**Design intent should survive the build, even when the implementation evolves.**
