# Visual Grammar

Logograph uses a consistent visual language so dense arguments can be read without flattening their semantic structure.

Visual distinctions encode meaning. Aesthetic beauty is secondary to readability, navigability, and semantic precision.

## Core Principles

- **Semantic precision first.** Shape, placement, color, and arrows should show what a node does in the argument.
- **YAML as source of truth.** Diagrams should reflect `book-map.nodes.yaml` and `book-map.edges.yaml`.
- **Consistency across chapters.** Once a visual convention is chosen for a book, keep it stable.
- **Authorial neutrality.** Visual emphasis should clarify the author's argument, not evaluate it.
- **Quotes as anchors.** Quotes support structure; they do not replace claims, grounds, or responses.

## Node Colors

Suggested defaults:

| Node type | Color |
| --- | --- |
| `question` | Blue |
| `meta_thesis` | Dark green with strongest emphasis |
| `diagnostic_claim` | Amber or muted orange |
| `major_claim` | Dark green |
| `supporting_argument` | Light green |
| `biblical_basis` | Gold |
| `historical_support` | Purple |
| `quote` | Document/callout styling |
| `counterpoint_against_author` | Orange/red |
| `counterpoint_for_author` | Orange/red with distinct label or accent |
| `response` | Teal |
| `assumption` | Grey |
| `definition` | Cyan |
| `implication` | Brown |
| `fact_context` | Neutral/light grey |
| `critique_of_existing_solutions` | Orange/red with critique label |

## Node Shapes

| Node type | Visual treatment |
| --- | --- |
| `question` | Rounded rectangle |
| `meta_thesis` | Strong rectangle with heaviest border |
| `diagnostic_claim` | Diagnosis node, visually distinct from constructive claims |
| `major_claim` | Strong rectangle with heavier border |
| `supporting_argument` | Standard rectangle |
| `biblical_basis` | Upward grounding node below or beneath the claim it grounds |
| `historical_support` | Historical support node, visually distinct from biblical basis |
| `quote` | Callout or document-style node |
| `counterpoint_against_author` | Downward node showing objection, tension, or pressure against the author's argument |
| `counterpoint_for_author` | Downward node showing a tension or counterpoint that ultimately strengthens the author's argument |
| `response` | Node placed near the counterpoint it addresses |
| `assumption` | Grey hexagon or similar visually distinct shape |
| `definition` | Clarifying node with distinct outline or label marker |
| `implication` | Downstream consequence/application node |
| `fact_context` | Neutral context node |
| `critique_of_existing_solutions` | Critique node near the solution/framework being assessed |

## Placement Grammar

- Place the central thesis flow horizontally where possible.
- Place `question` nodes near the top or opening side of the relevant section.
- Place `meta_thesis` nodes where the governing book-level purpose can orient the map.
- Place `diagnostic_claim` nodes near the felt problem or context they diagnose.
- Place `major_claim` nodes in the main argument path.
- Place `supporting_argument` nodes adjacent to the major claim they support.
- Place `biblical_basis` nodes as upward grounding nodes feeding into claims.
- Place `historical_support` nodes as side branches near the claim or context they illuminate.
- Place `critique_of_existing_solutions` nodes near the solution or framework being critiqued.
- Place `fact_context` nodes neutrally, without making them look like claims.
- Place `counterpoint_against_author` and `counterpoint_for_author` nodes downward from the main path to show tension or pressure.
- Place `response` nodes near the counterpoints they address.
- Place `assumption` nodes as grey hexagons or similar shapes, connected to the claims that depend on them.
- Place `quote` nodes as callout/document-style nodes attached to the structure they support.
- Preserve cross-section linkages where later material depends on, responds to, retrieves, or clarifies earlier material.

## Whole-Book Layout

The eventual graph should reflect section-level architecture, not merely chapter sequence. For _A Heart Aflame for God_, the four major parts should probably become visual territories, swimlanes, or clusters:

1. Foundations
2. The Reformation Triangle
3. Widening Our Scope
4. Challenges

The likely high-level flow is:

```txt
FOUNDATIONS
  -> REFORMATION TRIANGLE
  -> WIDENING OUR SCOPE
  -> CHALLENGES
```

Part 2, "The Reformation Triangle," appears to be the conceptual nucleus of the whole book and should likely occupy the visual center of the eventual map. Do not implement this final layout until the cumulative source model has enough reviewed content.

Avoid excessive crossing lines, over-stacking text, and purely aesthetic positioning without semantic meaning.

## Arrow Styles

Arrow style communicates the explicitness and role of a relationship:

| Style | Meaning |
| --- | --- |
| Solid | Explicit relationship |
| Dotted | Implied relationship |
| Bold | Major structural dependency |
| Dashed | Tension or contrast |
| Double arrow | Reciprocal relationship |

Prefer labelled arrows. A label such as `grounds`, `responds_to`, or `clarifies` should make the relation readable even when the layout changes.

## Edge Language

Use these edge types:

| Edge type | Use |
| --- | --- |
| `therefore` | Strong logical consequence |
| `supports` | Provides evidence or reinforcement |
| `grounds` | Provides foundational basis |
| `responds_to` | Addresses an objection or tension |
| `assumes` | Depends on a prior premise |
| `leads_to` | Represents causal or developmental flow |
| `clarifies` | Defines or sharpens meaning |
| `contrasts_with` | Represents tension or opposition |
| `flows_into` | Used for conceptual progression where strict causality is too strong |
| `misunderstands` | Represents critique of a framework or diagnosis |
| `retrieves` | Represents recovery of an older or neglected framework/tradition |

Do not flatten all relationships into `supports`. Semantic precision in arrows is part of the map.

## Draw.io Compatibility

When generating diagrams, output valid draw.io-compatible XML in `.drawio` files. The canonical current diagram is `book-map.drawio`. Keep node IDs and edge labels traceable to the cumulative YAML source files whenever possible.
