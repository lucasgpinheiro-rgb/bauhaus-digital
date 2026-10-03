---
name: bauhaus-digital
description: Use when designing or reviewing a digital product (interface, dashboard, landing page, design system, slide deck) in a Bauhaus, Swiss/International, modernist, geometric or constructivist language, or "in the style of Itten, Albers or Müller-Brockmann". Also use when defining a product's contrast system, visual hierarchy, tonal scale, palette and color tokens, proportions, type scale or layout grid, even if Bauhaus is never mentioned. It applies Itten's Basic Course, Müller-Brockmann's grid systems and Albers' Interaction of Color as a method of controlled contrast, not as a retro look of primary colors and geometric shapes.
---

# Bauhaus Digital: controlled contrast for digital products

## Premise

Three teachers, one method:

- **Johannes Itten**, *Design and Form*. The Basic Course, which governs what happens **inside** a field: contrast, tone, form character, accent, rhythm.
- **Josef Müller-Brockmann**, *Grid Systems in Graphic Design*. The grid **is** the field: where things may sit, and the units everything is measured in.
- **Josef Albers**, *Interaction of Color*. Color is relative. Judge it in context, measure lightness, test against the real neighbors.

Itten built his teaching on a general theory of contrast. Chiaroscuro, texture, form, rhythm, color and expression were all taught through their contrast effect (Itten p.12). He also said the exercises were not exercises in a formalistic style (p.62). So a "Bauhaus" product is **not** one with red, yellow and blue circles, squares and triangles. It is one where **every visual decision serves a declared contrast**, and everything else stays quiet so that contrast can be read.

The smallest demonstration of the whole method is Itten's first light–dark exercise (p.16, 18). A white circle outlined on white paper does not read as a white shape until a tone surrounds it, and a light, delicate gray is enough. Nothing means anything alone; only relations do. Albers reaches the same conclusion for color: it is the most relative medium in art (Albers, Introduction and ch. IV).

## How claims are labeled

Keep two kinds of rule apart, here and when explaining your work to the user:

- **Source rules** carry a citation: (Itten p.N), (M-B p.N), (Albers ch. N). They paraphrase what the books say.
- **Heuristics** are this skill's conversions into numbers for screens: 12 columns, 45–75 characters, 4/8 px units, OKLCH, 95/4/1 color quantities, 2–3 card widths. They are marked *heuristic*. They are defensible defaults, not the authors' words. Never present one to the user as "Itten says…".

Editions, page conventions and known translation slips are listed in `references/sources.md`. Go deeper with `references/contrasts.md` (Itten's full contrast list, form and accent), `references/grid-and-type.md` (Müller-Brockmann's units, type and consistency rules) and `references/color.md` (Albers, operationalized for screens).

## Workflow

For new work, follow the steps in order. To review an existing design, run the checklist at the end first and use the steps to diagnose what failed.

### 0. Content and brief first

- **Inventory the content before choosing a grid.** Müller-Brockmann will not set a type area until he knows how much text and how many pictures, of what kind and what priority (M-B p.49, 55). His order is content and priorities, then type size and line height, then the grid (p.61–62, 92). Do not pick "12 columns" before you know what goes in them.
- **Phrase the brief as the experience to produce.** Itten contrasts two briefs: "The Tiger" would yield decoratively striped animals, "The Roaring Tiger" fear-inspiring postures. How the task is set shapes the result (Itten p.125). Write "a monitoring screen that calms an on-call engineer at 3 a.m.", not "a dashboard".

### 1. Declare the contrasts

Itten lists about 24 contrast pairs plus the seven color contrasts (p.12). The full list and its digital mapping are in `references/contrasts.md`. The ones that matter most in product work:

| Contrast (Itten) | Where it lives in a digital product (*mapping is heuristic*) |
|---|---|
| light–dark | tonal scale, surfaces and elevation, dark mode |
| large–small | type scale, card hierarchy |
| much–little | data density vs. breathing room |
| area–line | filled surface vs. border, divider, outline icon |
| straight–curved, pointed–blunt | corner radius, icon terminals |
| broad–narrow, thick–thin | column widths, bar and stroke weights |
| hard–soft | edge sharpness, shadow blur, focus rings |
| horizontal–vertical | reading direction vs. column rhythm |
| diagonal–circular | tension (trend, error, emphasis) vs. continuity (progress, avatar) |
| smooth–rough | flat surface vs. grain, noise, texture |
| transparent–opaque | overlay, scrim, blur, modal layer |
| still–moving | static state vs. transition and animation |
| continuous–intermittent | solid vs. dashed, determinate vs. indeterminate progress |
| light–heavy | font weight, color density |

Choose **one dominant contrast and at most two subordinate ones** (*heuristic*). Itten sets no number. He requires that the chosen pair produce a definite expression (p.16), and says that combining several forms or contrasts needs a strong feeling for form to balance them (p.72). The cap is how this skill enforces that.

A contrast is a scale, not a switch. Itten located the life of the contrast world in the gradations between the poles (p.12). Decide where on the scale each element sits.

Write the declaration into your output, for example:

```
Dominant contrast: area–line
Subordinate: large–small, much–little
Color: quantity only (one action hue, never a competing hue)
```

### 2. Choose a form character, and carry it through every scale

Itten typifies the three basic forms by direction (p.62):

- **Square:** horizontal and vertical. Its repeated right angles produce a tense movement from corner to corner.
- **Triangle:** diagonal. All angles are represented in it.
- **Circle:** an evenly curved, continuously moving line.

Product roles (*heuristic*):

- **Square:** the default character of software, in tables, cards, fields and grids.
- **Triangle:** used sparingly, for direction, change and warning (trend arrows, error states).
- **Circle:** continuity and identity (avatars, status dots, progress, toggles).

**One form character runs through every scale.** With a team of students, Itten set out to design a whole room in one form character (p.65). One piece of it is a door with wood relief whose lock metalwork, by the student Naum Slutzky (Weimar, 1921), was developed from the square and the cube (p.65–66). His students also wrote letters in the character of a given form (p.68).

With a square base, that means:

- corner radius of 0 or nearly 0;
- icons drawn on an orthogonal grid;
- square avatars;
- bar loaders, not spinners.

Define a **base character plus one accent character**, and reserve the accent for a single meaning. For example: base square, with the circle reserved for people and identity. Mixing characters without a hierarchy is the most common failure.

**To build families** (icons, illustrations, component variants), use Itten's motif-and-variation exercises (p.62, 80, 82):

1. Fix one motif.
2. Fix an explicit list of allowed transformations: shift, rotate, reflect, invert, rescale, lighten or darken.
3. Generate the variants systematically.
4. Keep the simplest and clearest.

His positive–negative forms (p.63, 82) tile the plane without gaps; the book shows them as textile designs. Use them for patterns, mosaic and tile layouts, and interlocking shapes.

### 3. Grid and units (Müller-Brockmann)

The division of labour (*heuristic*, consistent with M-B p.75, who says a grid guarantees nothing without a sense of composition): **the grid decides where things may sit; Itten decides how they relate.**

**The grid.** A grid divides a plane into fields (or a space into compartments). Field width equals column width. Field depth is a fixed number of text lines. Fields are separated by whole empty lines (M-B p.11). The smallest picture equals the smallest field, and every picture takes a **whole number of fields: 1, 2, 3, 4 or more**. The German original says "or more"; the English translation drops it, and the plates run up to 16 fields and full pages. In CSS terms this is `grid-column: span n`. He first sketched the idea briefly in a 1961 book and codified it in *Grid Systems* in 1981 (p.7–8).

**Columns** (p.57):

- 1 column leaves too little freedom to vary picture sizes.
- 2 columns allow text and picture side by side, or stacked, and subdivide into 4.
- 3 columns give good variety and subdivide into 6. The narrow lines may force smaller type, depending on the task.
- 4 columns suit much text with many pictures. They subdivide into 8, 16 and more, which is convenient for statistics.

Column systems can be combined: 2 with 3 or 4, and 4 with 8 (p.52–53).

On screens (*heuristic*):

- Use 12 columns, because 12 divides by 2, 3, 4 and 6. This is his subdivisibility argument, not his number.
- Use 16 or 24 columns only for genuinely dense dashboards, and carry his warning with them. Fine meshes demand more self-discipline; without it they slide into confusion (p.87, 92, 129–130).

**Few sizes.** The fewer distinct picture sizes, the quieter the design (p.11). He also uses size contrast for tension (p.70). So use few sizes, deliberately contrasted (*heuristic*: 2–3 card widths per screen).

**One vertical unit.** This is the part of the baseline grid that survives responsive layout:

- The line heights of every type size are multiples of one unit. In his examples, 7/1, 10/2 and 20/4 pt all fit 24 pt. His own book is set so that 3 caption lines equal 2 text lines (p.34, 59, 66, 87).
- Gaps are whole units, never halves (p.64, 80, 134).
- Row gap and column gap may differ. The row gap is sized for the caption beneath (p.63).

The token version (*heuristic*):

- a base unit of 4 or 8 px;
- line heights, spacing and component heights as multiples of the base unit;
- `row-gap` and `column-gap` as separate tokens.

**What does not transfer:**

- Computing field depth in lines (his worked example: 57 − 3 = 54; 54 ÷ 4 = 13.5; round down to 13 lines per field, so the column becomes 55 lines; p.58–59) does not survive text that reflows.
- Neither does cross-column baseline registration.
- **Exception:** fixed formats get his full method. That means slides, printable reports, fixed dashboard tiles and social images.

**Margins.** The binding and trimming reasons do not transfer. The visual rules do, for any fixed frame (slides, hero sections, dialogs, cards):

- Too little margin feels overfull; too much feels extravagant (p.40).
- A type area set too high seems to fly away; set too low, it seems to drop out (p.40–41, 51).
- Equal margins all round look indecisive and dull (p.41).

**Panels.** For any filled container, decide whether the **text** or the **panel edge** sits on the grid line (p.101–103). Irregular images sit on a grid-sized panel (p.97–100).

**Ethics.** The grid compels honesty in the use of design means, forces analysis of the problem (p.11) and fosters analytical thinking (p.12). A 12-column grid with everything placed off it has the cost of a grid and none of the benefit. He calls the belief that the grid restricts creativity a widespread misconception (p.104).

Type rules (measure, hierarchy, leading, reversed text) and the full consistency list are in `references/grid-and-type.md`. Step 4 has the minimum.

### 4. Type, at minimum

- **Hierarchy.** Size steps must be clearly recognizable. Weight works as a gray value. Never pair two faces of the same style, such as two similar grotesques (M-B p.45–47). In dense UI, mark headings with space or weight before size (*heuristic*).
- **Measure.** Müller-Brockmann gives about 7 words per line (p.30, 53, 64), and elsewhere about 10 (p.31). Lines that are too long tire the eye, which has to hold the horizontal. Lines that are too short tire it too, by forcing constant line changes. Both reduce memorability (p.30–31). On screens, count characters instead: **45–75** (*heuristic*, after Bringhurst, not M-B).
- **Size follows reading distance and measure.** He sizes type for a 30–35 cm reading distance (p.30), which is about where a phone is held. Desktop sits further away, so use larger type (*heuristic*). Kiosks, TV dashboards and projected slides need a stated viewing distance before you choose sizes. Wider columns need larger type to keep the same rhythm (p.31–32, 53–54), so use `clamp()` or container query units.
- **Reversed text.** Light-on-dark text should be short and generously leaded (p.129). In dark mode, add a little line height and avoid long reversed passages.
- **Albers' dissent** (ch. II): all-caps is the hardest reading, and a simpler letterform does not mean simpler reading. Do not set body text in geometric all-caps because it "looks Bauhaus".

### 5. Tone before hue

- **Block out in tonal masses, not outlines.** Itten says light–dark compositions are never begun in outline, because the patches are set by the intensity of light and dark (p.16, 26). Students who began color work with outlines attended to the form and not the color (p.32).
  - Lo-fi frames are therefore filled gray masses at their intended tone, not bordered boxes.
  - Combine this with Müller-Brockmann's sketches, which are small but **accurate**: real type sizes and real copy length, at the target proportion (M-B p.49, 94–95). Narrow them to 2–3, build those at 1:1 in the real viewport, and start again if the margins fail (p.58, 60).
- **The tonal scale.** Itten's tone value scale uses single-tone steps with no lines between them; gifted students reached 44 steps between black and white (p.16–17).
  - Product scale (*heuristic*): 7–12 steps, with **equal ΔL in a perceptual space** (OKLab or OKLCH L, or CIE L\*).
  - Do not use a geometric progression of L. Albers' Weber–Fechner chapter says equal *perceived* steps need geometric *physical* increments (ch. XX). Perceptual L already includes that correction, so equal L steps are the equal perceived steps.
  - Hex interpolation does fail, but mainly on hue and chroma (a muddy middle between distant hues) and on uneven lightness across hues.
- **Judge a ramp as a contiguous strip with no gaps or borders.** It passes when every adjacent boundary looks equally distinct (Albers ch. V, XX).
- **Size and tone.** Areas of different size need tones of different strength (Itten p.16, 20). *Heuristic:* large areas stay quiet and small elements carry the strong tone. That keeps a dashboard from looking heavy.
- **Tone groups.** Identical tones attract and different tones repel (Itten p.30). A shared surface tone makes a group; a tonal step separates.
- **Minimum sufficient contrast.** Use the smallest tonal step that makes an edge appear (Itten p.16) before adding borders or shadows. Where the boundary carries meaning, it must still meet WCAG non-text contrast of 3:1.
- **Measure lightness; don't eyeball it.** Year after year, most of Albers' students misjudged which of two colors was darker (ch. V). Grayscale checks use perceptual L, never HSL desaturation. Saturated colors still look lighter than computed (the Helmholtz–Kohlrausch effect, *not Albers*), so confirm by eye.
- **The gray-reduction check.** This is Itten's Goya exercise: a painting is squared off and translated into grays only (p.21). Downsample a screenshot into a coarse mosaic of perceptual-L grays, then judge the tonal distribution and where the accents fall.
- **Dark mode is transposition, not inversion.**
  - Itten's reversal: in a light scheme the darks stand out, and in a dark scheme the lights (p.16, 26).
  - Albers: a set of colors keeps its character in a higher or lower key if its intervals are kept, and the extremes leave no headroom (ch. XIV).
  - Keep the ΔL intervals between surface, raised surface, border, text and accent.
  - Don't anchor the light theme at pure #FFF/#000 if it must transpose.
  - Test by inlaying a dark-theme component into the light theme, and the reverse, then compare edge strengths.

### 6. Color

**Itten's seven color contrasts** (p.32–33) are useful vocabulary: hue, light–dark, cold–warm, complementary, simultaneous, saturation, and extension (quantity). His 12-part circle and color star (1921) belong to the RYB pigment tradition, and screens emit RGB light, so work in perceptual spaces.

**What Albers actually rejects** is harmony recipes, not color systems; he teaches systems at the end of his course (ch. XXIV). He calls the rules of thumb for complementary, split, triad and tetrad harmonies worn out (ch. XVI). His reason: harmonies are illustrated in equal quantities, and they change once applied. No mechanical system can precalculate:

- quantity, form and recurrence;
- changing light, and several lights at once;
- reflections of light and of other colors;
- the direction and sequence of reading;
- materials;
- the objects placed alongside.

He also distrusts "tuned", failure-proof color sets (ch. III). So do not derive palettes from color-wheel geometry (*heuristic extrapolation*).

**Albers, operationalized.** In each item the bold lead states what Albers shows; the bullets beneath are this skill's conversion for screens (*heuristic*). Details and screen notes are in `references/color.md`.

1. **Relativity.** The same color on two grounds reads as two colors; two different colors can be made to look alike. The ground subtracts its own hue and lightness from what sits on it. The effect is strongest when a small figure sits on a large ground (ch. IV, VI, VII).
   - A color token has no meaning on its own. Define it as a pair: color plus the surface it sits on.
   - Keep a **surface × foreground** matrix, and test every status token on every surface at its real size.
   - A chip or divider that straddles two surfaces will look like two different tokens (ch. VI, XV).
2. **Quantity is area *and* recurrence.** Any color can work with any other if the quantities are right, and Albers says there are no comprehensive rules for finding them (ch. XVI).
   - *Heuristic:* start from about 95% neutral, 4% support and 1% action; the action color stays under about 5% of the area.
   - Count occurrences as well as area. An accent covering 1% of the area, repeated on 30 badges, dominates.
   - The same hues in different proportions make a different product, so a palette spec includes role proportions.
3. **Bezold effect / optical mixture** (ch. XII–XIII). Fine, evenly distributed elements merge toward each other. In a student plate he reproduces, swapping white mortar for black changes every brick.
   - Gridlines, hairlines, dividers, thin strokes and dense heatmap cells re-tint the whole screen. Before changing a primary, try the fine structural color.
   - Thin chart lines will not match their legend swatches. Choose series colors at the rendered stroke width.
4. **Vibrating boundaries** (ch. XXII). Strongly contrasting hues at similar light intensity produce a doubled, flickering edge. It is exciting at first, then aggressive; Albers notes that, outside loud advertising, it is seldom used.
   - *Diagnosis:* adjacent elements differ in hue but barely in L. Fix the lightness, not the hue.
5. **Vanishing boundaries** (ch. XXIII). At truly equal light intensity, *neighboring* hues lose their boundary. So at equal L, distant hues vibrate and near hues vanish.
   - The product consequence comes from accessibility, not from Albers. A state distinguished only by hue fails color-blind users and dim screens.
   - Every pair of states (active/inactive, success/error) needs a ΔL or a non-color cue.
6. **Transparency, film and space** (ch. IX, XI, XVII).
   - A believable overlap color lies between its parents. Whichever parent dominates it appears to be on top.
   - Hard boundaries signal separation and distance; soft boundaries signal nearness.
   - Hover, pressed and selected layers must shift every underlying color by the same *perceived* amount.
   - Stacked scrims darken with diminishing returns. Two 40% black layers make 64%, not 80% (*derived*).

**Method, not anti-method.** Albers puts practice before theory and refuses prescriptive rules, but he is methodical: step by step, precise and comparative (ch. IV, XXV). He likens coloring to cooking: follow the recipe, but keep tasting (ch. XVI). Treat everything above as diagnostics, and verify on real screens: white point, Night Shift or True Tone, brightness, glare, gamut, and OLED vs. LCD blacks.

**This is not accessibility.** WCAG is checked separately: 4.5:1 for body text, 3:1 for large text and for meaningful non-text UI. Perceptual effects and contrast ratios are different tests, and a pair can pass one and fail the other.

### 7. Proportion

Itten names the series 1:2:4:8:16:32 and 1:3:9:27:81, the golden section and the harmonic triangle, without guidance on using them (p.62).

Heuristics:

- **One ratio for type and spacing.** The type scale and the spacing scale share one ratio and one unit.
- **Hard ratios (1:2, 1:3)** give few, unmistakable levels, which suits products.
- **Soft ratios (golden section, minor third)** give more levels, which suits editorial work. In dense UI their adjacent steps blur, which breaks M-B's rule that steps be clearly recognizable (p.45).

**Perceived proportion is not measured proportion.** A long form beside a short one looks longer than it is (Itten p.62). Itten *exploits* the distortion for expressive dynamism. Products more often *compensate* for it: optical alignment of icons, circles overshooting squares, border weight on HiDPI screens. Say which one you are doing.

### 8. Accents and visual paths

How the accents are distributed decides the effect. The lines between accents are visual paths (Itten p.63, 90–93). Itten describes **two legitimate modes**:

- **One main accent gives stillness.** The gaze keeps returning to it.
- **Several equal accents give movement.** The eye travels between them.

Declare the mode for each screen:

- **Stillness:** reading, deciding, forms, checkout, detail pages. One main accent, which means one primary action.
- **Scanning:** monitoring and overview dashboards. Several equal accents on purpose. Nothing else may compete, and an alert becomes the one break.

**Exercise.** Reduce the screen to black discs sized by visual weight (*heuristic*), and draw the network of paths between them (Itten p.90). Count the dominant discs and compare the count with the declared mode.

Müller-Brockmann adds two points:

- Placement and accentuation steer the eye (M-B p.76).
- White space around a title gives it a rest zone that emphasizes it (p.69).

### 9. Space

Itten opened his students' first exhibition with Lao-Tse (p.13). The wheel, the pot and the house are useful through their emptiness: matter is the usefulness, non-matter the essence.

Müller-Brockmann makes the same point in layout terms:

- The unprinted ground is a design element on a par with the others (M-B p.20).
- Space around a title is a rest zone (p.69).
- Separation between images helps the reader understand the content (p.82).

So spacing defines grouping. Before adding dividers, borders or cards, try space first, then tone (step 5), and lines last.

### 10. Rhythm and motion

Itten distinguishes regular, mechanical repetition from free, flowing movement (p.98). When a march was stopped and resumed at irregular intervals, his students found the interruption almost painful. His forms develop through intermediate forms so that the rhythm is not broken (p.98, 106).

For products:

- **Spatial rhythm is mostly mechanical:** the unit, the grid, lists.
- **Breaks are costly.** Allow them only where they carry meaning, at the main accent, and keep them few (*heuristic*: at most one structural break per screen).
- **State changes need intermediate forms:** transitions, skeletons, morphs. An abrupt jump reads as broken rhythm.

**Texture is secondary to form** (Itten p.39). Grain, blur, glass and noise are at most a subordinate contrast and never carry hierarchy.

### 11. Explore, then converge

- **Diverge before constraining.** Itten worked from free perception before construction (p.16). He also had students render a subject three ways (expressively, constructively and impressionistically) and then seek a synthesis (p.132–133). Produce three directions before converging, and notice which one is your default.
- **Variants, not variety** (Albers, "Variants versus variety"). Show whole-screen variants within one scheme, side by side and in context. Reject any change made "for variety".
- **Analyze references one principle at a time.** Itten's students studied masterpieces for the principle just taught, and he warned against academic copying (p.13, 109–110). Extract the accent structure, the tonal map and the rhythm, never the surface style.
- **Judge the palette twice.** First as equal swatches in a chessboard, free of form associations (Itten p.32). Then in context (Albers).
- **Test the timbre.** Itten's students painted themes such as Night, Funeral and Fairground to find each one's color timbre (p.33). Test the palette against the product's states: incident, all clear, onboarding, empty.

### 12. Systematize

Müller-Brockmann's corporate-identity list (M-B p.134) works almost unchanged as a design-system review: same title size and position, same distances, same caption-to-image relation, one grid everywhere, images only in field sizes, the same colors for the same kind of content, the same leading for the same size, whole empty lines. Add his requirement that the system handle uses that only appear in the future (p.133). Test it by asking: can a component nobody has designed yet be placed using only the existing tokens? Design the landing page on the product grid; designing the cover apart from the inside breaks the system (p.135).

## Deliverable format

When producing a design, lead with a spec block, then the design, then the checklist results:

```
Brief:          <the experience to produce>
Contrast:       dominant <pair>; subordinate <pair>, <pair>
Accent mode:    stillness | scanning (main accent: <element>)
Form character: base <square|circle|triangle>; accent <…> reserved for <meaning>
Grid:           <n> columns, gutter <x>, base unit <u>; row-gap <…>; max width <…>
Type:           <faces>; scale <steps> at ratio <r>; line heights in <u>; measure <45–75 ch>
Tone:           <n>-step ramp, equal ΔL (OKLCH); dark mode = transposed intervals
Color:          action <token> ≤<x>% area and ≤<n> occurrences; status = ΔL + hue + icon
```

## Review checklist

Structure
- [ ] Is the dominant contrast declared and readable within 2 seconds?
- [ ] Does every element occupy a whole number of grid fields?
- [ ] Are there few distinct card or picture sizes (2–3), deliberately contrasted?
- [ ] Is the accent mode declared, and does the disc-and-path reduction match it?
- [ ] Does the form character hold from icon to layout, with the accent character reserved for one meaning?
- [ ] Could any divider or border be replaced by space or by a tonal step?

Tone and color
- [ ] Does the hierarchy survive the gray-reduction check (perceptual L, not HSL)?
- [ ] Is the ramp equal in ΔL, with equally distinct boundaries in a contiguous strip?
- [ ] Does the action color stay small in **area and count** (≲5% area)?
- [ ] Does any adjacent pair differ in hue but not in lightness (vibration or vanishing)?
- [ ] Is every state distinguishable without hue?
- [ ] Have tokens been checked on every surface they land on (the surface × foreground matrix)?
- [ ] Does dark mode transpose the intervals rather than invert them?
- [ ] Does the design pass WCAG separately (4.5:1 text, 3:1 large text and non-text)?

Type and units
- [ ] Is the measure 45–75 characters, with type sized for the real viewing distance?
- [ ] Are line heights, spacing and component heights multiples of one unit, and are gaps whole units?
- [ ] Do the type and spacing scales share one ratio, with clearly distinguishable steps?
- [ ] Is reversed text short and given extra line height?

System
- [ ] Do the same kinds of content get the same position, size and color everywhere?
- [ ] Could a new, undesigned component be placed with the existing tokens alone?

## What this skill does not cover

Say so to the user when a request falls outside it, rather than forcing the sources.

- **Accessibility compliance.** WCAG contrast, focus, motion and target size are separate checks.
- **Interaction design, information architecture and usability research.** These books are about perception and composition.
- **Type design and type selection.** Müller-Brockmann covers setting and hierarchy (pp.17–47). For the typographic Bauhaus, look to Herbert Bayer and Joost Schmidt, and to Tschichold's *Die neue Typographie*, which Müller-Brockmann cites (p.7).
- **Industrial functionalism.** Itten left the Bauhaus in 1923 after a conflict with Gropius. He did not believe the "Art and Technology" slogan could solve the problems of the time (Itten p.9, 13). If the user wants functionalism, meaning the later, industry-facing Bauhaus (general history, not these books), these sources are the wrong anchor.
- **Paper-specific technique.** Paper versus screen is covered in `references/color.md` and `references/grid-and-type.md`.

Itten's course is legitimate ground for product design. He taught it from 1917 to 1960, from Vienna to Zurich (p.15), and he judged its texture studies of value to future architects, industrial designers and commercial artists, and gave texture exercises even to textile merchants and managers (p.34). But it is a course in perception, not a product process. The workflow above is this skill's conversion of it.

## The main trap: pastiche

"Bauhaus" is sold today as primary colors, basic geometry and a geometric sans. Itten wrote that superficial imitation of his example lacked the spark he saw in his best students (p.6). He said it about students copying their teacher, and pastiche is the same failure at a larger scale.

If the result looks like a 1923 poster wrapped around a 2026 SaaS product, the skill has been used as a filter instead of a method. The method is: declare the contrast, solve the hierarchy in tone, keep one form character, and let everything else stay quiet.
