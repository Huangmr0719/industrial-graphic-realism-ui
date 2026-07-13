# Design System

## Contents

1. Design thesis
2. Materials and color
3. Typography
4. Layout
5. Component patterns
6. Interaction and accessibility
7. Implementation guidance
8. Anti-patterns

## Design Thesis

Combine three forms of logic:

- **Product logic:** Make components engineered, modular, and purposeful.
- **Graphic logic:** Use typography, contrast, labels, codes, symbols, and composition to create identity.
- **Realism logic:** Keep the interface believable, legible, and operational.

The interface should feel assembled around real work, not decorated with a science-fiction skin.

## Materials and Color

Use a deliberately small material vocabulary:

- base surface: black, off-black, white, cold gray, or off-white
- panel surface: flat fill, thin border, minimal or no shadow
- active surface: high-contrast accent tied to a meaningful state
- data surface: table, log, grid, metadata strip, or fixed-width block
- media surface: framed image, chart, code, paper, or generated artifact

Use approximately 80-90% base neutral, 8-15% secondary neutral, and 3-8% total accent in dark archive or terminal compositions. Product screens with more semantic states may use a broader distribution. Pick one primary signal such as acid yellow-green, safety orange, electric blue, or cold cyan. A second accent is permitted only when it has a distinct structural job, such as chapter transition or archive indexing.

Use the accent for primary action, current navigation, selected content, active process, live state, or a key metric. Do not scatter it as decoration.

Avoid excessive gradients, blur, glow, glassmorphism, shadows, ornamental textures, and fake holographic effects.

Example starting tokens:

```css
:root {
  --surface-base: #0b0c0d;
  --surface-panel: #121417;
  --surface-elevated: #181b1f;
  --text-primary: #f2f2ee;
  --text-secondary: #a8adaf;
  --text-muted: #6f767a;
  --accent-primary: #d7ff3f;
  --danger: #ff3b30;
  --warning: #ff9f0a;
  --success: #36f57f;
  --border-subtle: rgb(255 255 255 / 12%);
  --border-strong: rgb(255 255 255 / 32%);
  --radius-panel: 2px;
  --radius-control: 2px;
  --font-display: system-ui, sans-serif;
  --font-body: system-ui, sans-serif;
  --font-mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
}
```

Treat these values as a starting structure, not a mandatory palette.

## Typography

Use typography as interface architecture:

- display: bold condensed, geometric, or grotesk sans-serif for true page identity
- section title: compact and strong, optionally uppercase
- body: highly readable sans-serif
- metadata and IDs: monospaced
- code and logs: monospaced

Keep display type proportional to its container. Do not use hero-scale text inside compact panels. Do not make all text uppercase. Never depend on tiny decorative text for essential information.

Treat real font metrics as part of layout. Similar-looking families can have radically different width, x-height, and line box behavior. After changing fonts, recalibrate navigation gaps, headline wrapping, vertical rails, and compact labels from screenshots. Use uppercase for navigation, codes, and terse labels; keep paragraphs and long publication titles readable.

## Layout

Order information by:

1. page identity
2. current state
3. primary action
4. primary content
5. metadata
6. secondary actions
7. atmosphere, only when it has a legitimate role

Prefer hard-edged rectangular zones, strong alignment, compact metadata rails, section numbers, fixed-width data blocks, and controlled asymmetry.

### Section Rail System

A rail is a structural edge, not a reusable decoration. It may carry identity, state, indexing, or navigation, but its position, width, and density should respond to the chapter. One section may use a wide right identity rail, another a thin left signal line, another a year axis, and another no rail at all. Repeating the same colored sidebar across every section turns a system into a template.

Let rails touch the frame when the composition calls for an edge condition. Avoid accidental inset gaps, isolated color strips, and labels whose orientation or spacing is unrelated to the rail geometry.

### Identity and Archive Composition

- Hero: one dominant image field, one identity event, and one concise information panel.
- Research: one large statement plus a restrained academic trace; avoid equal-weight cards.
- News: a paged transmission log with a small visible batch, not an endlessly widening carousel.
- Publications: full-width archive records with code, title, author, venue, and access; avoid database headers unless sorting is real.
- Projects: engineering artifacts with a single identity line and external destination; visuals should carry more weight than metadata.
- Notes: fragments or transmissions with title, date, and source; never default to blog cards and summaries.
- Footer: terminal exit and contact directory; do not repeat the biography, position, and research scope already stated above.

For dashboards, keep the upper region state-oriented, place primary actions near the current state, and put logs and details below.

For landing pages, allow a visually assertive hero while keeping the product and offer immediately clear. Frame real screenshots or outputs as artifacts.

For forms, reduce visual intensity and keep labels, validation, input states, and actions conventional.

## Component Patterns

Adapt these roles to the product's vocabulary. Do not expose the pattern names in the UI unless they are valid domain terms.

### Mission Header

Use for page identity:

- compact metadata label
- clear page title
- short contextual subtitle
- current status
- optional timestamp or version

Keep page identity dominant without turning every internal page into a marketing hero.

### Status Strip

Use for states such as active, idle, running, locked, failed, synced, pending, archived, degraded, or read only.

Use a compact rectangle, strong contrast, optional indicator block, and short text. Pair color with a label or symbol.

### Signal Card

Use for a repeated task, project, experiment, image, or data summary:

- metadata row
- title and concise description
- state and key metric
- timestamp
- relevant action

Make it feel like an object in a real system, not a generic content card.

### Operator Panel

Use for a control area:

- panel title and status
- primary and secondary controls
- metric, output, or log area

Keep it calm, dense, and legible.

### Artifact Frame

Use for images, code, papers, logs, charts, screenshots, or generated outputs:

- title and source/type
- actual preview content
- metadata footer
- relevant actions

### Identity Badge

Use to identify an agent, module, project, dataset, model, team, source, environment, airport, camera, or task type. Name it according to the domain. Do not default to fictional group language.

### Run Log

Use monospaced text, a neutral panel, timestamps, status tokens, collapsible entries, and restrained error or warning highlights. Preserve selection, copying, wrapping, and horizontal overflow behavior.

### Data Rail

Use a narrow horizontal or vertical strip for real metadata such as run ID, model, environment, status, updated time, version, or permission state.

For identity archives, decorative glyphs may replace numeric IDs when the marks are clearly ornamental. Do not label abstract marks as readings or statuses.

## Interaction and Accessibility

Make interactions precise:

- sharp hover state
- border or background activation
- small purposeful movement
- fast transitions
- visible focus ring
- explicit disabled, loading, and selected states

Avoid bouncy motion, slow cinematic transitions, excessive glow, hidden controls, ambiguous hover effects, and decorative loaders that obscure progress.

Maintain sufficient contrast, full keyboard navigation, semantic markup, readable body text, labeled icons, and reduced-motion behavior. Do not encode state by color alone or place critical text over noisy media.

## Implementation Guidance

- Use the project's component and icon libraries.
- Use design tokens and semantic state classes.
- Keep spacing on a consistent scale.
- Use borders and surface changes before shadows.
- Set stable dimensions for compact controls, status tokens, rails, and toolbars.
- Let long labels wrap or truncate intentionally with an accessible full value.
- Preserve touch target sizes even when the visual treatment is compact.
- Avoid one-off inline styles, magic numbers, and overuse of absolute positioning.
- For art-directed vertical compositions, size internal assets relative to their rail (`cqw`, percentages, or intrinsic aspect ratio) so barcodes and marks maintain edge contact across widths.
- Reserve stable face-safe areas when media and overlays share a frame.
- Use `100dvh` minus the actual header for full-screen heroes and verify that browser chrome and mobile dynamic viewports do not reveal the next section.

## Anti-Patterns

Reject:

- generic rounded SaaS cards everywhere
- random neon lines, grids, arrows, coordinates, or warning stripes
- decorative blobs and gradient atmospheres
- excessive glow, glitch, glass, blur, or chromatic effects
- fake logs, telemetry, permissions, or system alerts
- unreadable microtext
- accent color without semantic purpose
- visual density that hides the primary action
- direct imitation of a commercial game's or brand's identity
- identical colored sidebars repeated on every section
- project and note sections reduced to generic portfolio or blog cards
- large accent rectangles used to compensate for weak hierarchy
- portrait overlays that cover eyes, mouth, or the intended focal area
- endless CSS calibration layers that override one another
