# A Heart Aflame for God

This Logograph workspace maps Matthew C. Bingham's _A Heart Aflame for God: A Reformed Approach to Spiritual Formation_ as one cumulative whole-book argument map.

The goal is to represent the book's argument with authorial neutrality before offering any evaluation. The map should help readers see the questions Bingham is answering, the claims he advances, the theological and historical grounds he uses, and how later chapters depend on, answer, retrieve, or complicate material introduced earlier, including in the introduction.

## Workspace Status

- Canonical whole-book map: initialized placeholder
- Cumulative node source: initialized placeholder
- Cumulative edge source: initialized placeholder
- Source folders: initialized for the introduction, Chapter 1, and Chapter 2
- Snapshots: initialized for after the introduction, Chapter 1, and Chapter 2
- Full argument map: not generated

## Canonical Files

- `book-map.drawio`: Current whole-book diagram.
- `book-map.nodes.yaml`: Cumulative node source of truth.
- `book-map.edges.yaml`: Cumulative edge source of truth.
- `book-meta.yaml`: Bibliographic and project metadata.
- `style-guide.md`: Book-specific mapping and visual conventions.

## Source Modules

- `chapters/introduction/notes.md`: Raw introduction notes.
- `chapters/ch01/notes.md`: Raw Chapter 1 notes.
- `chapters/ch02/notes.md`: Raw Chapter 2 notes.

Source folders are input/source material. They are not independent final diagrams.

## Snapshots

- `snapshots/after-introduction/`: State of the whole-book map after the introduction is incorporated.
- `snapshots/after-ch01/`: Frozen state of the whole-book map after Chapter 1 is incorporated.
- `snapshots/after-ch02/`: Frozen state of the whole-book map after Chapter 2 is incorporated.

Snapshots capture historical states of the same cumulative map.

## Mapping Commitments

- Map Bingham's argument before evaluating it.
- Treat cross-section linkages as a first-class feature.
- Keep doctrinal, biblical, historical, contextual, and practical claims distinct when possible.
- Use quotations sparingly and structurally.
- Treat root-level YAML as the source of truth for the canonical book map.

## Book Architecture

The book is organised into four major parts:

1. Foundations
2. The Reformation Triangle
3. Widening Our Scope
4. Challenges

The eventual graph should probably use section-level territories, swimlanes, or clusters. The Reformation Triangle appears to be the conceptual nucleus of the book and should likely occupy the visual center when the map is eventually generated.
