# Design Audit Checklist

Review the rendered interface, not only the source code. Record concrete failures and correct them before completion.

## Product Clarity

- Can the user identify the page, current state, and primary action within three seconds?
- Does each control perform or communicate a real function?
- Are IDs, labels, logs, metrics, timestamps, and status values derived from real product data?
- Does the page remain understandable when imagery is removed?
- Is content density appropriate for the workflow?

## Visual System

- Does every accent-colored element have a semantic reason?
- Is there one clear primary accent rather than several competing brand colors?
- Are success, warning, danger, and information colors used consistently?
- Does typography create hierarchy instead of relying on boxes and color?
- Are metadata, state labels, borders, radii, spacing, and surfaces consistent?
- Does the interface feel like one coherent system?

## Layout and Components

- Are major regions aligned to a deliberate grid?
- Are cards limited to distinct repeated objects or framed tools?
- Are controls, toolbars, rails, and status labels dimensionally stable?
- Do long text, real data, empty states, errors, and loading states fit without overlap?
- Are dense panels calm enough to scan repeatedly?
- Are mobile layouts intentionally recomposed rather than merely squeezed?

## Interaction and Accessibility

- Is the primary workflow fully operable by keyboard?
- Are focus, hover, active, selected, disabled, loading, and error states visible?
- Are touch targets large enough even when controls look compact?
- Are icons labeled for assistive technology, with tooltips where meaning is unfamiliar?
- Is no state communicated by color alone?
- Is contrast sufficient and essential text readable?
- Does reduced-motion mode remove nonessential animation?

## Drift Detection

- Remove any decorative element that cannot explain its function.
- Remove generic SaaS softness: oversized radii, floating sections, excessive cards, and vague shadows.
- Remove cheap cyberpunk cues: random neon, glow, glitch, grids, fake coordinates, and unreadable microtext.
- Remove theatrical system language that does not belong to the product.
- Reduce style intensity where it harms forms, tables, logs, or reading.
- Replace any recognizable commercial logo, symbol, font treatment, or copied layout.

## Implementation Quality

- Reuse existing project components and tokens where appropriate.
- Use semantic HTML and state names.
- Avoid magic numbers, one-off inline styles, and unnecessary absolute positioning.
- Verify desktop and mobile rendering visually.
- Exercise the primary interaction and representative edge states.
- Check the browser console and fix relevant errors or warnings.

## Final Test

The interface should be graphic but not noisy, futuristic but believable, stylish but usable, and designed rather than decorated.
