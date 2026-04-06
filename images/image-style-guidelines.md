# VISTA Image Style Guidelines

Use these guidelines when generating SVG diagrams for the VISTA project. Every new image should look like it belongs in the same family as the existing diagrams.

---

## Dimension Color Palette

Each VISTA dimension has a named color. Use the **accent** for circles, left-edge bars, and emphasis. Use the **background** for card fills and tinted regions. Use the **title** for heading text and the **body** for description text within that dimension's cards.

| Dimension   | Name    | Accent    | Background | Title text | Body text  |
|-------------|---------|-----------|------------|------------|------------|
| Value       | Blue    | `#5a8ab5` | `#edf3fb`  | `#3a6a95`  | `#4a6a85`  |
| Impact      | Yellow  | `#c4a240` | `#faf5e4`  | `#8a7020`  | `#6a5a30`  |
| Safety      | Green   | `#5a9a60` | `#ebf3eb`  | `#3a7a40`  | `#3a5a3e`  |
| Timing      | Red     | `#c07060` | `#fae8e6`  | `#8a4040`  | `#6a4a45`  |
| Adaptation  | Magenta | `#a060a0` | `#f2e8f4`  | `#7a3a7a`  | `#6a4a6a`  |

Colors are deliberately muted and subtle — no saturated primaries. The accent is the strongest use of color; backgrounds are very light tints.

---

## Neutral & Structural Colors

| Use                          | Hex         |
|------------------------------|-------------|
| Page background (top)        | `#f8f9fb`   |
| Page background (bottom)     | `#f0f2f6`   |
| Panel background             | `#ffffff`   |
| Panel border                 | `#e2e6ec`   |
| Dark box gradient start      | `#1a2332`   |
| Dark box gradient end        | `#2a3f55`   |
| Primary heading text         | `#1a2332`   |
| Secondary heading text       | `#556677`   |
| Body text                    | `#3a4a5c`   |
| Footer body text             | `#4a5a6b`   |
| Label / all-caps text        | `#7a8da0`   |
| Muted sub-label text         | `#6b7b8d`   |
| Arrow / connector stroke     | `#8899aa`   |
| Feedback arrow stroke        | `#6c8ebf`   |
| Chip pill text               | `#1a2332`   |
| Chip pill fill               | `#ffffff`   |
| Letter circle text (on fill) | `#ffffff`   |
| Dark-box heading text        | `#f0f4f8`   |
| Dark-box body text           | `#c5d3e0`   |
| Dark-box label               | `#8aa0b8`   |
| Drop-shadow color            | `#1a2332` at 6% opacity |

---

## Typography

All text uses `'Segoe UI', system-ui, sans-serif`.

| Role               | Weight | Size  | Notes                        |
|---------------------|--------|-------|------------------------------|
| Page title          | 700    | 42px  |                              |
| Page subtitle       | 400    | 18px  |                              |
| Panel title         | 700    | 22px  |                              |
| Panel body          | 400    | 15px  |                              |
| Section label       | 700    | 11px  | ALL CAPS, `letter-spacing: 2px` |
| Dark-box rule text  | 700    | 26px  |                              |
| Dark-box body       | 400    | 15px  |                              |
| Layer title         | 700    | 17px  |                              |
| Layer body          | 400    | 13px  |                              |
| Dimension title     | 700    | 18px  | Uses dimension title color   |
| Dimension body      | 400    | 13px  | Uses dimension body color    |
| Dimension letter    | 700    | 22px  | White, centered in circle    |
| Chip / pill label   | 600    | 11px  | `letter-spacing: 0.5px`     |
| Mini label          | 600    | 14px  |                              |
| Mini sub-label      | 400    | 12px  |                              |
| Footer title        | 700    | 18px  |                              |
| Footer body         | 400    | 14px  |                              |

---

## Layout & Spacing

- **Canvas**: 1800 × 1200 px is the standard size.
- **Outer margin**: 72px from all edges to content.
- **Panel corner radius**: `rx="20"` for outer panels.
- **Card corner radius**: `rx="16"` for inner content cards.
- **Pill / chip corner radius**: `rx="12"`.
- **Small box corner radius**: `rx="14"` (e.g., timing boxes).
- **Panel stroke**: 1.5px, `#e2e6ec`.
- **Gap between panels**: ~34px horizontal, ~30px vertical.
- **Internal padding**: ~28px from panel edge to content.

---

## Component Patterns

### Dimension Cards
- Background fill using the dimension's background color.
- 6px-wide left-edge accent bar (same `rx="3"`, full card height).
- Colored circle (r=20) with a white single-letter label, left-aligned.
- Title text (dimension title color) right of the circle.
- Description text (dimension body color) below the title, split across lines to avoid overflow. Keep lines under ~40 characters.
- Card height: 92px. Card width: matches panel inner width minus padding.

### Panels
- White fill, light border, subtle drop-shadow (`dy=4, stdDeviation=8, 6% opacity`).
- All-caps section label at top (`letter-spacing: 2px`, muted color).
- Bold panel title below the label.

### Dark Emphasis Box
- Linear gradient fill (`#1a2332` → `#2a3f55`), same drop-shadow.
- Light-colored text for headings and body. Muted label color for section label.

### Chip Pills
- White-filled rounded rect (`rx="12"`, 24px tall).
- Small bold text centered inside. Used for tags/categories within cards.

### Connectors & Arrows
- Solid lines: 2px stroke, `#8899aa`, with arrowhead marker.
- Feedback / loop arrows: dashed (`stroke-dasharray="6,4"`), `#6c8ebf`, 1.5–2px stroke.
- Arrow markers are simple filled triangles (10×10).

---

## General Principles

1. **Subtle, not loud.** Backgrounds are near-white tints. Accent colors are muted. Nothing should shout.
2. **Consistent palette.** Always use the five named dimension colors. Do not introduce new hues for VISTA dimensions.
3. **Hierarchy through weight, not color.** Use font weight and size to create hierarchy. Reserve color for semantic meaning (which dimension).
4. **Accessible contrast.** Title and body text on tinted backgrounds must remain comfortably readable. Dark text on light fills; light text on dark fills.
5. **Alignment.** Left-align body text. Center text in circles and pills. Use consistent x-coordinates within a panel.
6. **No decorative elements.** No icons, illustrations, or gradients beyond the single dark emphasis box. The style is clean, informational, and flat.
7. **Wrap text explicitly.** SVG does not auto-wrap. Always split long strings into multiple `<text>` elements on separate y-coordinates (~16–18px line spacing for body text).
8. **Use `<title>` and `<desc>`** for accessibility on every SVG root element.
