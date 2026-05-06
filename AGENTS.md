# AGENTS.md

Operating instructions for future Codex runs in Logograph.

Logograph is a framework for visualising dense books as structured argument maps. The work is semantic before it is visual: understand the role each idea plays, encode that role in cumulative book-level YAML, then generate the canonical whole-book Draw.io map from the structured source.

## Core Operating Rules

- Be semantically precise, but do not overformalise while the book structure is still being discovered.
- Preserve authorial neutrality. Map the author's argument before evaluating it.
- Do not invent claims that are not present in the user's notes or supplied source material.
- Do not summarise chapters from memory.
- Do not overquote. Quotes should support the structure, not replace it.
- Treat YAML files as the structured source of truth.
- Treat `book-map.nodes.yaml` and `book-map.edges.yaml` as the cumulative source of truth.
- Keep `book-map.drawio` aligned with `book-map.nodes.yaml` and `book-map.edges.yaml`.
- Treat introduction and chapter folders as input/source material, not independent final diagrams.
- Treat snapshots as historical states of the whole-book map after each source section.
- Support cross-section references as a first-class feature, including links from later chapters back to the introduction.
- Output draw.io-compatible diagrams when asked.
- Keep visual grammar consistent across chapters.
- Prefer labelled arrows.

## Preserve Semantic Distinctions

Do not flatten all support into one category. Preserve distinctions between:

- questions
- meta-theses
- diagnostic claims
- major claims
- supporting arguments
- facts
- biblical basis
- historical support
- critiques of existing solutions
- assumptions
- counterpoints
- responses
- definitions
- implications
- quotes

When a relationship is unclear, leave it marked as provisional rather than forcing it into a generic support relation.

## Node Types

Use these node types unless a book-specific style guide explicitly adds a type:

- `question`
- `meta_thesis`
- `diagnostic_claim`
- `major_claim`
- `supporting_argument`
- `biblical_basis`
- `historical_support`
- `quote`
- `counterpoint_against_author`
- `counterpoint_for_author`
- `response`
- `assumption`
- `definition`
- `implication`
- `fact_context`
- `critique_of_existing_solutions`

## Edge Types

Use these edge types unless a book-specific style guide explicitly adds a type:

- `therefore`
- `supports`
- `grounds`
- `responds_to`
- `assumes`
- `leads_to`
- `clarifies`
- `contrasts_with`
- `flows_into`
- `misunderstands`
- `retrieves`

## File Conventions

- `chapters/introduction/notes.md` and `chapters/chXX/notes.md` contain user-provided or source-derived notes, headings, quotations, and open questions.
- `book-map.nodes.yaml` contains cumulative structured argument nodes and is the source of truth for visual nodes.
- `book-map.edges.yaml` contains cumulative typed relationships and is the source of truth for visual arrows.
- `book-map.drawio` contains the canonical current whole-book diagram.
- `snapshots/after-chXX/` contains historical exports of the whole-book map after a chapter is incorporated.

## YAML Example

```yaml
nodes:
  - id: ch01-q001
    source_section: introduction
    type: question
    label: "Placeholder question"
    summary: "Replace with a user-supplied or source-derived question."
    source:
      kind: notes
      ref: null
    status: placeholder
```

```yaml
edges:
  - id: edge-001
    type: grounds
    from: ch01-bb001
    to: intro-mt001
    label: "grounds"
    style: bold
    source_section: ch01
    cross_section: true
    status: placeholder
```

## Diagram Discipline

When asked to generate diagrams:

- Generate draw.io-compatible XML.
- Use the root-level book-map YAML as the source of truth.
- Use labelled arrows wherever possible.
- Preserve the visual grammar defined in `docs/visual-grammar.md`.
- Preserve cross-section linkages.
- Keep responses close to the counterpoints they address.
- Keep biblical basis visually distinct from generic support.
- Keep facts/context visually distinct from claims.
- Keep assumptions visually distinct from stated claims.
- Keep diagnostic claims distinct from constructive major claims.
- Keep critiques of existing solutions distinct from counterpoints and responses.
- Consider section-level territories or clusters when the whole-book diagram is eventually generated.

## Arrow Style Conventions

- Solid arrow: explicit relationship.
- Dotted arrow: implied relationship.
- Bold arrow: major structural dependency.
- Dashed arrow: tension or contrast.
- Double arrow: reciprocal relationship.
