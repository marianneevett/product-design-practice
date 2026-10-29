# Product Design Practice

Working documents and examples for moving from ambiguous product problems to implementation and learning.

This repository documents how I approach product work: connecting customer needs, business rules, technical constraints, and experience decisions so a team can design and build with shared understanding.

It is intended for designers and engineering collaborators who want to understand or apply that approach. The framework covers product strategy and experience definition as well as implementation. AI-assisted workflows are one part of the practice.

## Start here

- **See the practice applied:** Follow the [fictional workshop booking example](examples/workshop-booking/README.md) from a constraint through a decision, feature requirements, and a scoped build.
- **Prepare implementation work:** Start with the [feature definition](framework/05-feature-definition.md) and [build brief](framework/06-build-brief.md).
- **Use AI coding tools:** Read [Working with AI](guides/working-with-ai.md) for how project instructions should refer to product and design context.

## The framework

| Document | Question it helps answer |
| --- | --- |
| [Product brief](framework/01-product-brief.md) | What problem are we addressing, for whom, and within which constraints? |
| [Experience principles](framework/02-experience-principles.md) | What should guide decisions when reasonable options conflict? |
| [Experience model](framework/03-experience-model.md) | How do people, capabilities, states, and dependencies connect? |
| [Decision log](framework/04-decision-log.md) | What did we decide, why, and when should we revisit it? |
| [Feature definition](framework/05-feature-definition.md) | How should the feature behave, including rules and exceptions? |
| [Build brief](framework/06-build-brief.md) | Which part are we implementing now, and how will we verify it? |
| [Learning log](framework/07-learning-log.md) | What did we observe, and which decisions should change? |

The documents support a recurring cycle: understanding the problem, defining the experience, making decisions, building, and learning. Work can return to an earlier question whenever new evidence warrants it.

## Choose the amount of documentation

Use the sections that help someone make or verify a decision. These are working templates, not seven required deliverables for every change.

| Situation | Useful starting point |
| --- | --- |
| Small UI correction with agreed behavior | A scoped issue or build brief with the expected behavior and verification steps. |
| New behavior in an existing product | A feature definition, linked decisions where needed, and a build brief for the next increment. |
| New product or substantial workflow change | A product brief and experience model; add principles, decisions, and feature definitions as questions become concrete. |
| A shipped change produces new evidence | A learning log linked to the decisions and requirements it affects. |

## Keep requirements in one place

The feature definition owns product behavior. The build brief links to that definition and selects an implementation increment; it adds delivery constraints and checks without copying the specification.

A decision log preserves the rationale for a change. When a decision changes behavior, update the feature definition in the same change and reference the decision. If implementation and documentation disagree, record the mismatch before treating either as the intended behavior.

Technical choices that preserve the agreed experience belong with engineering. Questions that change the experience return to the product decision process.

## Examples and evidence

The workshop booking example is fictional. Its constraints and simulated implementation finding illustrate the method; they are not research findings, shipped functionality, or measured outcomes. Examples do not expose private project documentation.

This repository currently contains documentation, not an application or a component library.

More about my work at [mariannematilda.com](https://mariannematilda.com).
