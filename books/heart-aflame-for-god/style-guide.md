# Style Guide

This style guide defines book-specific conventions for mapping Matthew C. Bingham's _A Heart Aflame for God: A Reformed Approach to Spiritual Formation_.

## Interpretive Posture

Begin with authorial neutrality. The map should represent Bingham's argument as fairly as possible before any assessment of its theological, historical, or practical adequacy.

Avoid turning the diagram into agreement, disagreement, critique, or devotional application. Those may be separate layers later, but the initial map should focus on what the book argues.

## Node Priorities

Give special attention to:

- Driving questions about spiritual formation.
- Definitions and distinctions that shape the Reformed approach.
- Meta-thesis statements that govern the whole book.
- Diagnostic claims about what has gone wrong.
- Major constructive claims about theological foundations.
- Supporting arguments about practices, affections, habits, or formation.
- Biblical basis nodes where Scripture is functioning as grounding.
- Historical support nodes where older figures, movements, or traditions are being retrieved or illustrated.
- Critiques of existing solutions where Bingham treats attempted answers as insufficient or misaligned.
- Counterpoints or alternative approaches Bingham addresses.
- Responses that clarify, retrieve, or rebut.
- Assumptions that carry major argumentative weight.
- Implications for spiritual formation, ministry, and practice.

## Identifier Scheme

Use stable IDs:

- `intro-q001` for introduction `question` nodes.
- `ch01-q001` for Chapter 1 `question` nodes.
- `intro-mt001` for introduction `meta_thesis` nodes.
- `ch01-mt001` for Chapter 1 `meta_thesis` nodes, if needed.
- `ch01-dc001` for `diagnostic_claim`.
- `ch01-mc001` for `major_claim`.
- `ch01-sa001` for `supporting_argument`.
- `ch01-bb001` for `biblical_basis`.
- `ch01-hs001` for `historical_support`.
- `ch01-qt001` for `quote`.
- `ch01-ca001` for `counterpoint_against_author`.
- `ch01-cf001` for `counterpoint_for_author`.
- `ch01-r001` for `response`.
- `ch01-a001` for `assumption`.
- `ch01-d001` for `definition`.
- `ch01-i001` for `implication`.
- `ch01-f001` for `fact_context`.
- `ch01-ces001` for `critique_of_existing_solutions`.
- `ch01-edge-001` for edges.

## Book Architecture

The book's four-part outline is semantically important and should inform the eventual whole-book layout:

1. Foundations
2. The Reformation Triangle
3. Widening Our Scope
4. Challenges

Working hypothesis: "The Reformation Triangle" is the conceptual nucleus of the book and should likely occupy the visual center. Treat this as layout guidance, not a final diagram decision.

## Visual Emphasis

The book map should distinguish doctrinal, biblical, historical, contextual, and practical movement where the chapter structure requires it. Do not force those categories onto every node, but use them when they clarify the author's argument.

Follow the shared visual grammar in `docs/visual-grammar.md`. The canonical diagram is the root-level `book-map.drawio`; chapter folders are source modules only.

## Cross-Section Linkages

Cross-section dependencies are first-class. Later chapters may ground, answer, clarify, retrieve, or complicate questions and claims introduced earlier, including in the introduction. Represent these relationships in `book-map.edges.yaml` rather than duplicating nodes in source-local files.

## Quotes

Quotes should be brief and tied to a structural purpose. A quote can anchor a definition, confirm a claim, illustrate a historical example, or show how a counterpoint is framed. It should not stand in for the node itself.
