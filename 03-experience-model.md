# Experience Model

An experience model creates a shared view of how people, product behavior, and system capabilities connect.

It helps teams understand the experience as a system rather than a collection of screens or features.

The model should make it easier to answer:

* What is someone trying to accomplish?
* What needs to happen for them to succeed?
* What does the product need to support?
* What does the underlying system need to make possible?
* Where do dependencies, rules, and gaps exist?

---

## Start with people and intent

### People

Who participates in or influences the experience?

Consider:

* Customers
* Operators
* Internal teams
* Partners
* Administrators
* Other systems

| Person / role | What matters to them |
| ------------- | -------------------- |
|               |                      |
|               |                      |

---

### Goals

What are they ultimately trying to accomplish?

Focus on outcomes rather than features.

| Person / role | Goal |
| ------------- | ---- |
|               |      |
|               |      |

---

## Identify the behaviors

What does someone need to do or understand to reach the goal?

These might include:

* Discover
* Compare
* Decide
* Configure
* Request
* Confirm
* Track
* Change
* Resolve
* Return

### Core behaviors

*

---

## Map the experience

Organize the experience around meaningful stages rather than individual screens.

| Stage | User intent | What needs to happen | Key decisions |
| ----- | ----------- | -------------------- | ------------- |
|       |             |                      |               |
|       |             |                      |               |
|       |             |                      |               |

A stage should represent a meaningful shift in intent, understanding, or product state.

---

## Connect experience to capability

For each important experience behavior, identify what the product needs to make possible.

| Experience need | Product capability |
| --------------- | ------------------ |
|                 |                    |
|                 |                    |

Examples:

**Experience need**
A customer needs to understand whether something is available before committing.

**Product capability**
The system can determine availability and communicate it at the appropriate point in the experience.

---

## Connect capability to the system

Capabilities usually depend on rules, data, permissions, integrations, or operational processes.

| Product capability | System requirement / dependency |
| ------------------ | ------------------------------- |
|                    |                                 |
|                    |                                 |

Consider:

* Data
* State
* Permissions
* Business rules
* Inventory
* Pricing
* Integrations
* Notifications
* Operational workflows
* Content

---

## Model important states

Experiences often become complicated because the same thing can exist in multiple states.

Identify the states that materially change what someone can see or do.

| Object / process | State | What changes |
| ---------------- | ----- | ------------ |
|                  |       |              |
|                  |       |              |

Examples might include:

`draft → submitted → in review → approved → completed`

The goal isn't to document every database state.

Focus on states that change the experience.

---

## Identify relationships

What objects, people, or processes depend on one another?

For example:

```text
Person
  ↓
Project
  ↓
Request
  ↓
Items
  ↓
Proposal
  ↓
Confirmation
```

The exact model will vary by product.

Look for:

* One-to-many relationships
* Shared objects
* Dependencies
* Ownership
* Repeated information
* Places where one action affects another part of the experience

---

## Find the pressure points

Once the model exists, look for areas where complexity accumulates.

These often include:

* One action changing several states
* Multiple people controlling the same object
* Conflicting business and customer needs
* Information appearing at different times
* Rules users cannot see
* Dependencies between separate workflows
* Exceptions that significantly alter the normal path

### Pressure points

*

---

## Use the model to make decisions

The experience model should help answer questions like:

* Where should this capability live?
* Is this a new feature or part of an existing system?
* What information must persist?
* Who owns this decision?
* What happens when something changes?
* Which states need distinct experiences?
* What can be simplified without breaking the system?
* What needs to be defined before implementation?

---

## Keep the model at the right altitude

An experience model is not:

* A sitemap
* A database schema
* A user flow
* A journey map
* A screen inventory

It can inform all of them.

The goal is to create a shared representation of **how the experience works as a system** before deciding exactly how every part should be designed.

---

**Understand the relationships first. Design the interfaces second.**
