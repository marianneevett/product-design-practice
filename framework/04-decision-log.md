# Decision Log

A decision log captures important product decisions, the reasoning behind them, and what changes because of them.

It creates a lightweight record of **why the product works the way it does**.

The goal isn't to document every choice.

Use it for decisions that:

* Affect the experience or system beyond one screen
* Resolve meaningful ambiguity
* Introduce or change a product rule
* Involve a real tradeoff
* Are likely to be questioned again later
* Change the direction, scope, or behavior of the product

---

# Decision

## [Short decision title]

**Status:** Proposed / Accepted / Revisit
**Date:** YYYY-MM-DD

### Decision

State what was decided in one or two sentences.

Be specific enough that someone who wasn't part of the conversation can understand the outcome.

*

---

### Context

What created the need for this decision?

Include the relevant:

* User need
* Product behavior
* Business requirement
* Technical constraint
* Operational reality
* Research or evidence
* Previous decision

Focus on the information necessary to understand the decision rather than recreating the entire discussion.

*

---

### Options considered

#### Option A — [Name]

Describe the direction.

**Strengths**

*

**Tradeoffs**

*

#### Option B — [Name]

Describe the direction.

**Strengths**

*

**Tradeoffs**

*

Add additional options only when they were meaningfully considered.

---

### Why this direction

Why was this option chosen?

Explain which considerations mattered most and which tradeoffs were intentionally accepted.

*

---

### Implications

What changes because of this decision?

Consider:

* Experience behavior

* Product rules

* Scope

* Data

* States

* Content

* Operations

* Technical requirements

* Future decisions

*

---

### What this does not decide

Clarify adjacent questions that remain open so the decision isn't interpreted more broadly than intended.

*

---

### Revisit when

What new information or change in conditions would justify reopening this decision?

Examples:

* New research contradicts the assumption

* Usage behavior changes

* A technical constraint is removed

* The business model changes

* The decision creates unexpected downstream complexity

*

---

# Example

## Require confirmation before submitting consequential changes

**Status:** Accepted
**Date:** YYYY-MM-DD

### Decision

Changes that materially affect price, availability, timing, or another person's commitments require an explicit confirmation step before they are submitted.

### Context

Some actions appear lightweight in the interface but trigger consequences elsewhere in the system.

Making those actions immediate would reduce friction, but it could also create accidental changes that are difficult for customers or operators to reverse.

### Options considered

#### Option A — Apply changes immediately

**Strengths**

* Faster
* Fewer interaction steps
* Appropriate for low-risk changes

**Tradeoffs**

* Consequences may not be obvious
* Greater risk of accidental actions
* Recovery may require manual intervention

#### Option B — Require confirmation

**Strengths**

* Makes consequences visible
* Gives people a chance to verify their intent
* Reduces avoidable operational problems

**Tradeoffs**

* Adds a step
* Can create unnecessary friction if applied too broadly

### Why this direction

The cost of an accidental consequential change is higher than the cost of one additional confirmation step.

Confirmation should therefore be reserved for actions with meaningful downstream impact rather than applied universally.

### Implications

* The interface must clearly communicate what will change
* Confirmation language should describe consequences rather than repeat the action label
* Low-risk edits should continue to save without confirmation
* Recovery behavior should still be defined where possible

### What this does not decide

This does not define which individual product actions qualify as consequential.

Those should be evaluated based on their impact.

### Revisit when

Revisit if evidence shows the confirmation step creates meaningful abandonment or if the system gains reliable undo functionality.

---

## Using the log

Keep decisions short enough to scan.

Link to supporting research, designs, issues, or implementation work when useful instead of duplicating them.

If a decision changes, don't erase the previous reasoning.

Update its status and create a new entry explaining what changed.

The value of the log is not just knowing **what was decided**.

It's being able to understand **why that decision made sense at the time**.
