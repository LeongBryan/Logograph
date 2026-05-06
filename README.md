# Logograph

**Visual argument maps for dense books.**

Logograph is a framework for transforming dense books into one cumulative whole-book Draw.io argument map.

The goal is not merely summarisation. The goal is to expose the structure of the author's reasoning, preserve the flow of questions and answers, reveal dependencies between concepts, distinguish claims from evidence and objections, and help readers retain and navigate complex works over long periods of study.

Visualisations should prioritise:

1. semantic clarity,
2. navigability,
3. argument structure,
4. and consistency across chapters and books.

Aesthetic beauty is secondary to readability and meaning.

## Purpose

Dense books are often difficult because readers cannot easily see:

- what question is currently being answered,
- why a chapter exists,
- how claims depend on previous claims,
- which assumptions are foundational,
- and whether a statement is descriptive, argumentative, historical, biblical, or evaluative.

Logograph externalises that architecture visually in a cumulative whole-book map progressively revealed section by section, beginning with the introduction.

The framework helps readers ask:

- What question or tension is driving this section?
- What core claim answers that question?
- What supporting claims expand or defend it?
- What biblical, historical, factual, or conceptual basis is being used?
- What counterpoints or alternative frameworks are being addressed?
- What assumptions are doing hidden work?
- What implications follow?
- How do later chapters depend on, retrieve, answer, or complicate earlier material?

## Core Philosophy

Logograph is built around these commitments:

- **One canonical book map.** A book project has one current whole-book diagram: `book-map.drawio`.
- **Cumulative source of truth.** `book-map.nodes.yaml` and `book-map.edges.yaml` are the structured source of truth for the whole map.
- **Chapters as source modules.** Chapter folders are input/source material, not independent final diagrams.
- **Cross-section linkages.** Later chapters may depend on questions from the introduction. Chapter 3 may answer tensions raised in Chapter 1. Part 4 may revisit unresolved assumptions from Part 1. Cross-section references are a first-class feature.
- **Semantic precision without premature rigidity.** The ontology should preserve meaningful distinctions while staying flexible as the book's structure is discovered.
- **Authorial neutrality.** The first task is mapping, not persuasion. Represent the author's argument before evaluating whether it succeeds.
- **Structure over extraction.** Quotations support the map, but they do not replace interpretation of the argument's structure.
- **Progressive revelation.** The whole-book map is progressively revealed section by section, beginning with the introduction.
- **Explicit relations.** Nodes matter because of how they relate to one another. Label arrows whenever reasonably possible.

## Questions vs Claims vs Facts

These must remain distinct.

**Questions** create narrative momentum. They drive structure, argument direction, and reader tension. Questions are often more important than conclusions because they explain why a section exists.

**Claims** are assertions the author is attempting to establish. Claims require grounding, support, explanation, or defense.

**Facts / context** provide framing or historical setup but are not necessarily functioning argumentatively.

## Node Types

Each node type represents a different semantic category. These distinctions are important and should remain visually consistent across all books.

- `question`: Explicit questions, implicit driving tensions, or unresolved problems.
- `meta_thesis`: The governing purpose or thesis of the whole book. Usually very few of these exist.
- `diagnostic_claim`: Claims about what has gone wrong, such as perceived spiritual shallowness or thinness.
- `major_claim`: Primary constructive assertions the book seeks to defend.
- `supporting_argument`: Reasoning that supports or develops a major claim.
- `biblical_basis`: Scripture passages, theological grounding, or explicit biblical appeals.
- `historical_support`: Historical examples or diagnoses functioning argumentatively.
- `quote`: A concise quotation that anchors, illustrates, or confirms part of the structure.
- `counterpoint_against_author`: Objections, tensions, critiques, or competing explanations that press against the author's argument.
- `counterpoint_for_author`: A counterpoint, tension, or alternative observation that ultimately strengthens or motivates the author's argument.
- `response`: Rebuttals, retrieval arguments, clarifications, or responses to counterpoints.
- `assumption`: Implied premises, worldview commitments, anthropological assumptions, epistemological assumptions, or unstated dependencies.
- `definition`: Clarification of terms, distinctions, or semantic precision.
- `implication`: Practical outcomes, ministry implications, applications, or consequences flowing from claims.
- `fact_context`: Historical context, biographical setup, stated background facts, or framing information.
- `critique_of_existing_solutions`: Critiques of attempted answers or frameworks the author regards as insufficient or misaligned.

Books contain multiple rhetorical layers. Not everything is argument. Some content functions as framing, diagnosis, persuasion, clarification, qualification, anticipation, contextualization, or caveat.

## Edge Types

Edges and arrows must be labelled whenever reasonably possible. Arrow labels are semantically important.

- `therefore`: Strong logical consequence.
- `supports`: Provides evidence or reinforcement.
- `grounds`: Provides foundational basis.
- `responds_to`: Addresses an objection or tension.
- `assumes`: Depends on a prior premise.
- `leads_to`: Represents causal or developmental flow.
- `clarifies`: Defines or sharpens meaning.
- `contrasts_with`: Represents tension or opposition.
- `flows_into`: Used for conceptual progression where strict causality is too strong.
- `misunderstands`: Represents critique of a framework or diagnosis.
- `retrieves`: Represents recovery of an older or neglected framework or tradition.

Do not flatten all support into `supports`. Use the most precise relation available.

## Visual Grammar

Visual distinctions encode meaning. More detail lives in [docs/visual-grammar.md](docs/visual-grammar.md).

Suggested node colors:

- Questions: blue
- Meta-theses: dark green with strongest emphasis
- Diagnostic claims: amber or muted orange
- Major claims: dark green
- Supporting arguments: light green
- Biblical basis: gold
- Historical support: purple
- Critiques of existing solutions: orange/red
- Counterpoints: orange/red
- Responses: teal
- Assumptions: grey
- Definitions: cyan
- Implications/applications: brown
- Facts/context: neutral/light grey
- Quotes: callout/document styling

Suggested layout:

- central horizontal thesis flow,
- upward grounding/basis,
- downward objections/tensions,
- side branches for examples or elaborations,
- visible cross-section links where later material depends on earlier material.

The book outline itself is semantically important and should influence eventual layout. _A Heart Aflame for God_ is organised into four major parts:

1. Foundations
2. The Reformation Triangle
3. Widening Our Scope
4. Challenges

The eventual graph should probably not be flat. Consider section-based territories, swimlanes, or clusters. Part 2, "The Reformation Triangle," appears to be the conceptual nucleus of the whole book and should likely occupy the visual center of the eventual map.

## Quotations

Quotations should support structure, not replace structure.

The diagram should remain understandable even if quotations are removed. Quotes are best used for memorable phrasing, representative examples, emotionally resonant statements, or concise formulations.

## Authorial Neutrality

The primary purpose is mapping, not persuasion.

Visualisations should distinguish:

- what the author claims,
- what critics claim,
- what assumptions exist,
- and where tensions remain unresolved.

The framework should remain reusable across books with differing viewpoints.

## Progressive Workflow

Logograph produces a cumulative whole-book map progressively revealed section by section, starting with the introduction.

Each source folder contains raw input notes. Those notes are interpreted into cumulative book-level YAML:

- `book-map.nodes.yaml`: all current nodes for the whole book.
- `book-map.edges.yaml`: all current edges for the whole book.
- `book-map.drawio`: the canonical current whole-book diagram.

Snapshots capture the state of the whole-book map after each source section:

- `snapshots/after-introduction`: whole-book map state after the introduction has been added.
- Later snapshots follow the same pattern, such as `snapshots/after-ch01` after Chapter 1 has been added.

This lets a study group watch the same book map grow over time while preserving cross-section dependencies.

More detail lives in [docs/workflow.md](docs/workflow.md).

## Repository Structure

```txt
logograph/
  README.md
  AGENTS.md
  docs/
    visual-grammar.md
    workflow.md
  books/
    heart-aflame-for-god/
      README.md
      book-meta.yaml
      style-guide.md
      book-map.drawio
      book-map.nodes.yaml
      book-map.edges.yaml
      chapters/
        introduction/
          notes.md
        ch01/
          notes.md
        ch02/
          notes.md
      snapshots/
        after-introduction/
          README.md
          book-map.drawio
          exports/
            README.md
        after-ch01/
          README.md
          book-map.drawio
          exports/
            README.md
        after-ch02/
          README.md
          book-map.drawio
          exports/
            README.md
```

## First Book Project

The first Logograph workspace is:

**Matthew C. Bingham, _A Heart Aflame for God: A Reformed Approach to Spiritual Formation_**

Its files live in [books/heart-aflame-for-god](books/heart-aflame-for-god).

The initial workspace includes the canonical whole-book map files, an introduction source-notes folder, and a snapshot folder for the state of the whole-book map after the introduction is added. No full argument map has been generated yet.

## Adding Future Books

To add a future book:

1. Create a new folder under `books/` using a stable slug.
2. Add `README.md`, `book-meta.yaml`, and `style-guide.md`.
3. Add canonical `book-map.drawio`, `book-map.nodes.yaml`, and `book-map.edges.yaml` files.
4. Create source note folders under `chapters/`, starting with `introduction` when the book has one.
5. Add snapshot folders as the whole-book map grows.
6. Keep quotes short and purposeful: they should support the structure, not replace it.

Every book should preserve the core Logograph discipline: map the author's argument first, then evaluate it later if evaluation is part of the project.
