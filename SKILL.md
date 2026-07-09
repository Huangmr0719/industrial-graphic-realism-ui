---
name: industrial-graphic-realism-ui
description: >-
  Design, implement, revise, or audit production frontend interfaces in an
  industrial graphic realism style: grounded operational logic, hard modular
  layouts, strong typography, restrained materials, semantic status language,
  and one deliberate accent color. Use for technical dashboards, AI agent
  consoles, developer tools, research and experiment systems, data-heavy
  products, hardware, robotics, aviation, simulation, photography, logging,
  and technical product pages. Trigger when the user asks for an industrial,
  operational, instrument-like, hard-edged, technical, productized sci-fi, or
  non-generic SaaS interface, or asks to make a UI feel like a real working
  system. Also use when reviewing such a design for generic SaaS drift,
  decorative cyberpunk effects, accessibility, or implementation quality. Do
  not use to imitate a named game, studio, brand, artist, or copyrighted visual
  identity.
---

# Industrial Graphic Realism UI

Create interfaces that feel like real operational systems with a strong graphic identity. Make every visual detail functional, preserve conventional interaction behavior, and let usability win whenever style conflicts with clarity.

## Load References

- Read [design-system.md](references/design-system.md) before designing or implementing a page. It defines the visual language, components, tokens, interactions, and anti-patterns.
- Read [audit-checklist.md](references/audit-checklist.md) before reviewing an existing interface or before the final verification pass of an implementation.

## Workflow

### 1. Establish Operational Reality

Inspect the existing product, codebase, and design system before making decisions. Identify:

- product type and target user
- user's immediate goal
- current page state
- primary action
- important real metadata
- required content density
- existing components, tokens, and framework constraints
- risk of visual overload

Do not invent fake telemetry, IDs, warnings, coordinates, logs, or controls merely to create atmosphere. Derive system language from real domain data and behavior.

### 2. Define the Visual System

Before implementation, form a compact internal plan for:

- page hierarchy and responsive layout
- component roles and state model
- neutral base palette and one primary accent
- typography roles for display, body, metadata, and code
- spacing, border, radius, and motion tokens
- keyboard, focus, contrast, reduced-motion, and mobile behavior

Use the host application's established design system when one exists. Adapt the style through tokens and composition instead of replacing working conventions wholesale.

### 3. Build the Interface

Implement the actual usable screen, not a style guide or marketing explanation.

- Use semantic HTML and reusable components.
- Use CSS variables or the project's token mechanism.
- Prefer grid and flex layouts over absolute positioning.
- Use thin borders, hard edges, and flat surfaces to establish hierarchy.
- Keep controls conventional and clearly interactive.
- Use icons from the project's icon library; add accessible labels and tooltips where needed.
- Use status text or symbols in addition to color.
- Keep logs, forms, tables, and dense content calm and legible.
- Respect responsive constraints and prevent text, controls, and metadata from overlapping.
- Keep motion fast, small, and purposeful; honor reduced-motion preferences.

Do not place style labels, design rationale, component names, or usage instructions in the visible product UI unless they are real domain content.

### 4. Audit and Correct

Render and inspect the result at representative desktop and mobile widths. Exercise primary interactions, loading, empty, error, disabled, selected, focus, and overflow states when they exist.

Apply [audit-checklist.md](references/audit-checklist.md), then fix failures before finishing. In particular, remove:

- meaningless decoration
- excess accent color
- soft generic SaaS card treatment
- cheap cyberpunk effects
- unreadable microtext
- fabricated system metadata
- style that obscures hierarchy or interaction

## Decision Rules

- Use one primary accent unless established product semantics require more.
- Reserve semantic colors for success, warning, danger, and informational states.
- Use cards only for distinct repeated objects or genuinely framed tools; do not turn every section into a floating card.
- Reduce style intensity in forms, tables, logs, and long reading areas.
- Keep body text in normal case. Reserve uppercase for compact labels, states, and IDs.
- Use imagery only when it reveals the real product, artifact, environment, or data.
- Avoid this style for medical service flows, government public-service pages, high-neutrality financial forms, reading-first pages, and soft consumer experiences unless the user explicitly requests it.

## Copyright Boundary

Translate abstract principles, never protected identity. Do not reproduce or closely imitate specific commercial screenshots, layouts, logos, symbols, faction marks, fonts, characters, or branded visual systems. Do not mention the source inspiration in the final interface. If the request names a copyrighted work, extract high-level traits and create a distinct system appropriate to the user's product.

## Completion Standard

Finish only when the interface:

- communicates page identity, current state, and primary action within seconds
- feels coherent without decorative effects
- remains usable with images removed
- preserves accessibility and responsive behavior
- looks engineered and productized rather than themed
