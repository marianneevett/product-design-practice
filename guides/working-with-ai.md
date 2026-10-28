# Working with AI coding tools

AI-assisted implementation needs the same product clarity as human collaboration. The framework documents describe what the product should do and why. Project instructions explain where that context lives, how to work within it, and how to verify a change.

Use this guide when applying the framework to a product repository. The example instructions below are teaching material, not instructions governing this documentation repository.

## Give each document a job

| Layer | Purpose | Keep elsewhere |
| --- | --- | --- |
| Product brief, principles, and experience model | Establish the problem, constraints, and experience structure | Tool setup commands |
| Decision log | Explain accepted tradeoffs and changes in direction | A duplicate current specification |
| Feature definition | Own intended behavior and unresolved product questions | Repeated implementation task lists |
| Build brief | Scope an increment and record verification | Copied feature requirements |
| AGENTS.md or a tool's supported instruction file | Locate authoritative context and define working conventions | The full product specification |
| DESIGN.md or existing design documentation | Explain visual and interaction conventions and reference components and tokens | A second copy of token values |
| A reusable skill | Define a repeated task's inputs, procedure, and expected output | General project history |

These are responsibilities, not a required set of filenames. Reuse existing documentation when it already serves the purpose.

## Start with the project

Before writing instructions, inspect the repository and identify:

- Where product requirements and accepted decisions live.
- Which design references, components, and tokens are authoritative.
- Which commands actually build, check, and test the project.
- How the team distinguishes implemented, proposed, and unresolved behavior.

Record verified paths and commands. An instruction such as “use the design system” is incomplete if the agent cannot locate it.

## A minimal project instruction example

Adapt this text to a real repository. Replace the illustrative paths with verified paths before using it.

```markdown
# Working in this project

## Context
- Read docs/product/README.md for the product documentation index.
- Before changing behavior, read its feature definition and accepted decisions.
- Before UI work, read docs/design/README.md and inspect the referenced components and tokens.
- Use the current build brief to identify this increment's scope and checks.

## Changes
- Reuse existing components and established patterns.
- Keep product behavior in its feature definition; link to it from build work.
- Resolve contradictions between requirements, designs, and implementation before changing affected behavior.
- Surface unanswered product questions; record agreed changes in the specification and decision log.
- Make implementation choices within the agreed behavior and scope.

## Verification
- Use the project commands documented in CONTRIBUTING.md.
- Check the affected states, recovery paths, permissions, and accessibility requirements.
- Report what changed, what was checked, actual results, and any checks not performed.
- Update affected documentation alongside implementation changes.
```

The referenced files in that snippet are illustrative; they are not files in this repository.

## Design context should be actionable

A design guide can explain hierarchy, layout behavior, component selection, content conventions, focus behavior, and responsive changes. Link to actual component and token definitions rather than copying their values.

For example, “keep the confirmation summary above the action on narrow screens” describes a decision that can be checked. “Make it modern” does not specify a result.

If a Figma reference and implemented component disagree, identify the conflict and establish the intended behavior. Do not silently choose whichever is easiest to access.

## Use tool-specific files only where needed

Instruction discovery varies by tool and version. Check the tool's documentation and verify that the expected files are loaded. An arbitrary Markdown filename does not guarantee automatic loading.

If a tool needs a dedicated entry file, keep it short and point to shared instructions using the mechanism it supports. Avoid maintaining separate copies of the same rules.

Official references:

- [AGENTS.md](https://agents.md/)
- [Claude Code project instructions](https://code.claude.com/docs/en/memory)
- [Claude Code skills](https://code.claude.com/docs/en/skills)

## Add a skill after a workflow proves useful

A repeatable requirement review could take a feature definition and proposed build brief as inputs, check for missing states and conflicting requirements, and return a list of gaps linked to their source sections.

Before packaging that workflow, establish:

- When it should run and which inputs it needs.
- Which steps produce a useful result.
- What the output must contain.
- Which decisions require human judgment.
- How you will assess whether it found meaningful issues.

A skill should refer to the project's requirements. It should not invent business rules to fill blanks or claim checks passed without evidence. Use the supported skill format and location for the chosen tool.

## Keep context current

When implementation reveals a product question:

1. Record the finding and its user-visible consequence.
2. Resolve the product decision with the responsible collaborator.
3. Update the authoritative requirement and link the decision.
4. Update the build scope and verification checks.
5. Record actual implementation and verification results separately.

The [workshop booking example](../examples/workshop-booking/README.md) follows this sequence for an uncertain booking result.

Evaluate the approach through real changes: were important questions surfaced sooner, were existing rules preserved, and did the output satisfy the specified behavior? More files alone do not establish better results.
