# VISTA — Agent Instructions

This file guides AI agents working in the VISTA repository. Follow these rules for all generated content: documentation, diagrams, commit messages, and review feedback.

---

## Voice and Tone

VISTA documentation is **principled, systematic, and grounded**. It reads like foundational rules for a decision-making system, not like a blog post or sales pitch.

### Rules

- **State, don't suggest.** Write assertions as principles, not opinions. Say "Output is not outcome" — not "We believe output isn't the same as outcome."
- **Third-person, systemic perspective.** Speak from the organizational level. Avoid first person ("I/we believe") and direct address ("you should") except in forcing questions.
- **Short declarative sentences layered with structured explanation.** Lead with a stark statement, then unpack it with lists, tables, or short paragraphs.
- **Define terms immediately.** Technical vocabulary (blast radius, activation burden, cost of delay) is fine — but every new term gets an explanatory sentence or bullet nearby.
- **Contrast, don't just describe.** Use "X is / X is not" pairs. Frame choices comparatively: "not just... but also," "the harder question is."
- **Connect to consequences.** Every concept should link to a real outcome: what breaks, what drifts, what gets missed.
- **No rhetorical flourish.** No appeals to emotion, no exclamation marks, no superlatives. Professional distance throughout.
- **Be direct, not dismissive.** Confidence without condescension. Acknowledge complexity rather than waving it away.

### Characteristic phrasing

These patterns recur across VISTA documentation. Match them:

- **Definitional clarity:** "Value asks: Did this work create meaningful user or business benefit?"
- **Principle assertions:** "Speed without direction is waste." "Risk gates value."
- **Comparative framing:** "Weights decide preference. Gates decide permissibility."
- **Functional consequences:** "If this breaks, how hard is it to undo?"

---

## Formatting

- **Bold** for key terms, definitions, and questions.
- **Headers** to create scannable sections (Definition, Why it matters, Questions X should force).
- **Bullet lists** for alternatives, signals, and enumerated points.
- **Tables** for comparisons and structured data.
- **Concrete examples** near the end of sections, specific and testable.
- No italic for emphasis — reserve italic for titles of external works only.
- No emoji in documentation.

---

## The Five Dimensions

Every VISTA dimension has a named color. Use these consistently in all references, diagrams, and visual materials.

| Dimension  | Color Name |
|------------|------------|
| Value      | Blue       |
| Impact     | Yellow     |
| Safety     | Green      |
| Timing     | Red        |
| Adaptation | Magenta    |

---

## Diagrams and Images

All SVG diagrams must follow the visual style guide at [`images/image-style-guidelines.md`](images/image-style-guidelines.md). That file contains:

- Hex codes for all five dimension colors (accent, background, title text, body text)
- Neutral and structural color palette
- Typography scale (font family, weights, sizes)
- Layout and spacing rules (canvas size, margins, corner radii)
- Component patterns (dimension cards, panels, dark boxes, chips, connectors)

Key principles for diagrams:

1. **Subtle, not loud.** Muted colors, near-white backgrounds, no saturated primaries.
2. **Consistent palette.** Never introduce new hues for VISTA dimensions.
3. **Hierarchy through weight, not color.** Font weight and size create hierarchy; color carries semantic meaning.
4. **No decorative elements.** No icons, illustrations, or extra gradients. Clean, informational, flat.
5. **Wrap text explicitly.** SVG does not auto-wrap — split long strings into multiple `<text>` elements.
6. **Accessibility.** Include `<title>` and `<desc>` on every SVG root. Maintain readable contrast ratios.

---

## Repository Structure

- `docs/` — Detailed documentation for each VISTA concept.
- `principles/` — The ten principles, one per file, plus an overview.
- `images/` — SVG diagrams and the image style guide.
- `README.md` — Top-level overview and entry point.

Do not create new top-level directories without discussion. New documentation goes in `docs/`. New principle files go in `principles/` with the next sequential number prefix.

---

## Commit Messages

- Imperative mood, lowercase after prefix: `docs: add scoring rubric for Layer 2`
- Prefix with scope: `docs:`, `images:`, `principles:`, `meta:`
- One logical change per commit. Do not bundle unrelated edits.
