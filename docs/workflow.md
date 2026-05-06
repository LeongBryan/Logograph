# Workflow

Logograph builds one cumulative whole-book map progressively revealed section by section, starting with the introduction.

Do not treat chapters or the introduction as separate final diagrams. Source folders are input/source material. The canonical output is the current whole-book map.

## Canonical Files

Each book workspace contains:

- `book-map.drawio`: The canonical current whole-book Draw.io diagram.
- `book-map.nodes.yaml`: The cumulative node source of truth.
- `book-map.edges.yaml`: The cumulative edge source of truth.
- `chapters/introduction/notes.md`: Raw introduction notes and source observations.
- `chapters/chXX/notes.md`: Raw chapter notes and source observations.
- `snapshots/after-introduction/`: Exported state of the whole-book map after the introduction has been incorporated.
- `snapshots/after-chXX/`: Exported state of the whole-book map after a chapter has been incorporated.

## Basic Rhythm

1. Read or receive notes for the next source section, beginning with the introduction.
2. Add new source material to `chapters/introduction/notes.md` or `chapters/chXX/notes.md`.
3. Extract semantically precise nodes into `book-map.nodes.yaml`.
4. Extract semantically precise edges into `book-map.edges.yaml`.
5. Add cross-section references where later material depends on, answers, retrieves, or complicates earlier material.
6. Update `book-map.drawio` from the cumulative YAML.
7. Save a snapshot under `snapshots/after-introduction/` or `snapshots/after-chXX/`.

## Source Folders

Source folders are source modules. They should contain raw notes, quotes, unresolved questions, and observations from the introduction or chapter.

They should not contain separate diagram outputs or separate node/edge source-of-truth files. Nodes and edges belong in the cumulative `book-map.nodes.yaml` and `book-map.edges.yaml` files.

## Cross-Section Linkages

Cross-section linkages are a first-class feature.

Examples:

- A Chapter 1 claim may `grounds` a tension introduced in the introduction.
- A Chapter 3 response may `responds_to` a counterpoint introduced in Chapter 1.
- A Chapter 4 definition may `clarifies` a term used earlier.
- A later historical example may `retrieves` a tradition introduced earlier.

Every node should record its source section. Edges may connect nodes from different sections.

## Snapshots

Snapshots capture the state of the whole-book map after each source section.

For example:

- `snapshots/after-introduction/` stores the whole-book map after the introduction has been added.
- Later snapshots follow the same pattern, such as `snapshots/after-ch01/` after Chapter 1 has been added.

Snapshots are historical exports, not separate source models. The current canonical source remains at the book root.

## Review Checklist

Before updating the canonical map or saving a snapshot, check:

- Does every major node have a clear semantic role?
- Does every node identify its source section?
- Are cross-section dependencies represented where needed?
- Are edge labels specific enough to explain the relationship?
- Are quotations brief and structurally useful?
- Does the map distinguish the author's argument from the mapper's evaluation?
- Does the visual hierarchy make the whole-book argument navigable?
