# Industrial Graphic Realism UI

An agent skill for designing and implementing grounded, hard-edged,
production-ready technical interfaces.

The skill turns an industrial graphic design language into executable rules for
AI coding agents. It combines operational product logic, strong typography,
modular layouts, restrained materials, semantic status language, and deliberate
use of color without sacrificing usability.

## What It Is For

Use this skill for:

- AI agent dashboards and control consoles
- developer tools and research systems
- experiment tracking and data-heavy products
- robotics, hardware, aviation, and simulation interfaces
- photography, logging, and technical workflow applications
- technical product pages and artifact-focused presentations
- design audits for generic SaaS or decorative cyberpunk drift

It is intentionally less suitable for medical services, government forms,
neutral financial workflows, reading-first pages, and soft consumer products
unless the visual direction is explicitly requested.

## Design Principles

- Build around real user goals, system states, and domain data.
- Use hard modular layouts, strong alignment, and limited materials.
- Reserve one primary accent color for meaningful actions and states.
- Treat typography, metadata, and status labels as interface architecture.
- Make every graphic detail explain its function.
- Keep forms, logs, tables, and dense content calm and readable.
- Preserve accessibility, keyboard navigation, responsive behavior, and
  conventional controls.
- Avoid generic rounded SaaS cards, fake telemetry, random neon, excessive
  glow, glassmorphism, decorative grids, and unreadable microtext.

## Installation

### Codex

Clone the repository into the Codex skills directory:

```bash
git clone https://github.com/Huangmr0719/industrial-graphic-realism-ui.git \
  ~/.codex/skills/industrial-graphic-realism-ui
```

Restart or open a new Codex session so the skill can be discovered.

### Other Agents

The core instructions use the portable `SKILL.md` convention and do not depend
on Codex-only tools. Place the repository in the skills directory supported by
your agent, or reference `SKILL.md` directly from its project instructions.

`agents/openai.yaml` only provides optional Codex interface metadata. The design
workflow and references remain usable without it.

## Usage

Invoke the skill explicitly:

```text
$industrial-graphic-realism-ui design and implement an experiment monitoring dashboard.
```

It can also be used for revision and review:

```text
Use $industrial-graphic-realism-ui to audit this interface, remove generic SaaS
styling, and preserve all existing workflows.
```

The agent should:

1. Inspect the product, codebase, and existing design system.
2. Identify the real user goal, page state, primary action, and metadata.
3. Define a restrained visual system and responsive component plan.
4. Implement the usable interface using the existing framework.
5. Render, exercise, and audit the result against the bundled checklist.

## Repository Structure

```text
industrial-graphic-realism-ui/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── audit-checklist.md
│   └── design-system.md
├── LICENSE
└── README.md
```

- `SKILL.md` contains the trigger description, workflow, and decision rules.
- `references/design-system.md` defines the visual language, component patterns,
  interaction rules, tokens, and anti-patterns.
- `references/audit-checklist.md` provides a rendered-interface review process.

## Copyright Boundary

This skill describes abstract design principles. It must not reproduce or
closely imitate protected screenshots, layouts, logos, symbols, fonts,
characters, faction marks, or branded visual identities from commercial work.

Use the system to create an original interface appropriate to the product.

## License

Released under the [MIT License](LICENSE).
