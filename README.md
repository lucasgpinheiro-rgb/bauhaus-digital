# Bauhaus Digital

A Claude skill that designs and reviews digital products (interfaces, dashboards, landing pages, design systems and slide decks) with the method of three Bauhaus-era and Swiss teachers:

- **Johannes Itten**, *Design and Form*: the Basic Course. Composition as controlled contrast, tone before color, one form character, accents and visual paths, rhythm.
- **Josef Müller-Brockmann**, *Grid Systems in Graphic Design*: fields, whole-unit gaps, one vertical unit for every type size, measure and hierarchy, design-system consistency.
- **Josef Albers**, *Interaction of Color*: color is relative. Measure lightness, define tokens as color-on-surface pairs, budget accents by area and recurrence, avoid vibrating and vanishing boundaries, and transpose (don't invert) for dark mode.

It is **not** a "retro Bauhaus look" generator. Primary colors, circles, squares and triangles in a geometric sans are exactly the pastiche the skill warns against. What it asks of every design:

- a declared contrast;
- a hierarchy that works in gray before any hue is added;
- one form character, carried from icon to layout;
- everything else kept quiet.

## What makes it different

- **Every source rule is cited to the page or chapter**, and **every heuristic is labeled as one**. The 12 columns, the 45–75 characters, the OKLCH ramps and the 95/4/1 color budget are the skill's conversions for screens, and it says so. It will not tell you "Itten says…" about something Itten didn't say.
- **Checked against the books.** The text was audited page by page against all three books, and the errors common in secondhand summaries were corrected. Itten did not design the Weimar door lock. *Grid Systems* is from 1981, not 1961. Albers rejects harmony recipes, not color systems. Equal perceived steps mean equal ΔL in a perceptual space, not a geometric progression of L. The full list is in [`references/sources.md`](skills/bauhaus-digital/references/sources.md).
- **It says what does not transfer from paper to screen**: baseline grids in reflowing text, binding margins, pigment mixing, and words-per-line as a measure.
- **It produces a spec, not only pixels.** Each design starts with a short declaration: contrast, accent mode, form character, grid and unit, type scale, tonal ramp, color budget. Each design ends with a review checklist.

## Install

### As a Claude Code plugin

```
/plugin marketplace add lucasgpinheiro-rgb/bauhaus-digital
/plugin install bauhaus-digital@bauhaus-digital
```

### As a plain skill

Copy `skills/bauhaus-digital/` into `~/.claude/skills/` (Claude Code), or upload the folder as a skill in Claude.ai.

## Use

The skill triggers on its own when you ask for a design in a Bauhaus, Swiss, modernist or constructivist language. It also triggers when you ask to define a contrast system, visual hierarchy, tonal scale, palette, color tokens, type scale or grid for a product. Examples:

- "Design the overview dashboard for our on-call tool, Swiss style."
- "Review this landing page: the hierarchy feels flat."
- "Build the color tokens and dark mode for our design system."
- "Set up a grid and type scale for a 16:9 deck."

## Structure

```
skills/bauhaus-digital/
├── SKILL.md                    # the method: 13 steps, deliverable format, checklist, limits
└── references/
    ├── contrasts.md            # Itten: all 24 contrast pairs, form, accent, rhythm, exercises
    ├── grid-and-type.md        # Müller-Brockmann: fields, units, type, margins, consistency list
    ├── color.md                # Albers chapter by chapter, translated to screens
    └── sources.md              # editions, page conventions, corrections, list of heuristics
```

## Sources

- Johannes Itten, *Design and Form: The Basic Course at the Bauhaus and Later*, rev. ed., 1975.
- Josef Müller-Brockmann, *Grid Systems in Graphic Design*, Niggli, 1981.
- Josef Albers, *Interaction of Color*, 50th anniversary ed., Yale University Press, 2013.

The skill paraphrases and cites these works; it does not reproduce them. Read the books: they are worth it.

## License

MIT, © 2026 Lucas Gonçalves Pinheiro. Written with Claude. Not affiliated with the authors' estates, their publishers, or the Bauhaus institutions.
