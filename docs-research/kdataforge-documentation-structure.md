# Research: KDataForge documentation structure

## Research question

How should KDataForge documentation serve players, pack authors, and developers without hiding or deleting the existing technical information?

## Findings from official guidance

### Separate pages by the reader's need

Diátaxis identifies four documentation needs with different jobs:

- A tutorial teaches through a controlled, repeatable task.
- A how-to guide helps a reader complete a real goal.
- Reference describes the system accurately and completely.
- Explanation gives context and answers why the system behaves as it does.

Mixing these jobs makes pages harder to use. A tutorial should keep alternatives and extended background out of the main path. Reference should follow the structure of the product and use stable, consistent patterns. Explanation can carry the design context that would interrupt a procedure.

Sources: [Diátaxis: start here](https://diataxis.fr/start-here/), [tutorials and how-to guides](https://diataxis.fr/tutorials-how-to/), [reference](https://diataxis.fr/reference/), [reference and explanation](https://diataxis.fr/reference-explanation/).

### Define each audience before writing

Google's technical-writing guidance recommends defining the reader's role, existing knowledge, goal, and expected result. One page should address a consistent audience. Vocabulary and assumed knowledge should match that audience.

For KDataForge, this produces three useful entry points:

1. Players who install or troubleshoot packs. They should not need YAML, Unreal, or mod-development knowledge.
2. Pack authors who create and maintain YAML packs. They can be expected to edit files, but the first tutorial should teach the KDataForge workflow and vocabulary.
3. Mod developers who integrate custom classes, handlers, editor support, or APIs. Their pages can assume Unreal and SML knowledge when stated.

Sources: [Google Technical Writing: audience](https://developers.google.com/tech-writing/one/audience), [Google Technical Writing: documents](https://developers.google.com/tech-writing/one/documents), [Google style: second person and audience consistency](https://developers.google.com/style/person).

### Put the action and result first

Microsoft recommends leading with the information readers need most, making long pages navigable, and using predictable patterns. Procedures should use numbered, imperative steps and include the action that completes the task. Google likewise recommends putting critical information first in each paragraph and using descriptive, hierarchical headings.

Applied to KDataForge:

- Landing page starts with a role choice and a direct next step.
- Player pages begin with install, enable, update, remove, and diagnose tasks.
- Author pages state the expected file, command, or in-game result before background.
- Long schema and feature pages use a repeated order so readers know where to look.
- Each procedure includes a verification step and the relevant error path.

Sources: [Microsoft: scannable content](https://learn.microsoft.com/en-us/style-guide/scannable-content/), [Microsoft: procedures and instructions](https://learn.microsoft.com/en-us/style-guide/checklists/procedures-and-instructions-checklist), [Google style: paragraph structure](https://developers.google.com/style/paragraph-structure), [Google style: headings and titles](https://developers.google.com/style/headings).

### Use plain language without removing precision

Official Google and Microsoft guidance favors active voice, second person, common words, short sentences, and clear attribution of actions. Technical terms remain when they are the correct product terms, but unfamiliar terms need a definition near first use. Concision should remove repetition and filler, not required conditions or edge cases.

Applied to KDataForge:

- Say what the player does and what KDataForge does.
- Use the same term for the same concept throughout the docs.
- Define pack, document, target, selector, operation, condition, handler, CDO, and reflection before relying on them.
- Keep code identifiers, YAML keys, paths, defaults, limits, load order, and failure behavior exact.
- Move implementation background away from player procedures instead of deleting it.

Sources: [Google style highlights](https://developers.google.com/style/highlights), [Google style: active voice](https://developers.google.com/style/voice), [Microsoft Learn style quick start](https://learn.microsoft.com/en-us/contribute/content/style-quick-start), [Microsoft: word choice checklist](https://learn.microsoft.com/en-us/style-guide/checklists/word-choice-checklist).

## Recommended information architecture

The current tree already contains substantial tutorials, examples, feature pages, reference pages, and background articles. Preserve their facts while routing readers through a simpler top level.

```text
KDataForge
├── Start here
│   ├── Choose your path
│   ├── Player guide
│   ├── Create your first pack
│   └── Core concepts and glossary
├── Player guide
│   ├── Install a pack
│   ├── Update or remove a pack
│   ├── Understand compatibility and load order
│   └── Troubleshoot a pack
├── Pack author tutorials
│   ├── First working pack
│   ├── Edit an existing object
│   ├── Add an item, recipe, and schematic
│   └── Publish and maintain a pack
├── How-to guides
│   ├── Target and patch content
│   ├── Create content
│   ├── Configure conditions and dependencies
│   ├── Localize a pack
│   ├── Work with unlocks and research
│   ├── Place resources and sublevels
│   └── Diagnose validation and runtime failures
├── Examples
│   └── Complete, copyable cases grouped by goal
├── Reference
│   ├── Pack and document schema
│   ├── Operations and property types
│   ├── Expressions, selectors, and conditions
│   ├── Content-type reference
│   ├── Classes, handlers, and extension API
│   └── Tools, reflection export, and editor integration
└── Concepts
    ├── Processing model and load order
    ├── Architecture and module structure
    ├── Targets, identity, and safe renames
    └── Compatibility strategy
```

`KDataForgeJS` and `LoadBalancers` stay outside this work.

## Page patterns

### Player task

1. One-sentence outcome.
2. Prerequisites.
3. Numbered steps.
4. What success looks like.
5. Common failure and recovery.
6. Links to the next player task.

### Pack-author how-to

1. Goal and when to use it.
2. Required pack state and source paths.
3. Minimal working YAML.
4. Exact steps.
5. Expected validation or runtime result.
6. Variants and edge cases.
7. Links to relevant schema reference.

### Reference page

1. Scope.
2. Syntax or data shape.
3. Field table with type, requirement, default, and behavior.
4. Valid values and constraints.
5. Processing and error behavior.
6. Small valid examples.
7. Related operations and types.

### Concept page

1. The question the page answers.
2. Mental model.
3. Lifecycle or data flow.
4. Design consequences and tradeoffs.
5. Links to tasks and reference.

## Content-preservation method

A restructure can lose details even when every old file still exists. Use a coverage matrix before deleting, merging, or renaming pages. Record each existing heading, factual claim, code sample, field, default, caveat, error, and local link. Map every entry to a destination in the new tree.

Count content as preserved only when the destination retains the same meaning and scope. Duplication can be removed after one canonical destination exists and all inbound links point to it. Redirects or stable compatibility pages should cover renamed routes if the site supports them.

## Acceptance checks

- Landing page gives players and authors different next steps.
- A player can install and diagnose a pack without reading author reference.
- A new author can build and verify one small pack on a single guided path.
- Task pages do not bury steps under architecture discussion.
- Reference retains every supported field, value, default, constraint, and failure mode.
- Terms and code identifiers remain consistent across pages.
- Every old information unit appears in the coverage matrix.
- Every local link resolves after moves or renames.
- Headings use sentence case and a valid hierarchy.
- Procedures use numbered imperative steps and end with verification.
- Final prose uses active voice, second person where appropriate, and plain language.
