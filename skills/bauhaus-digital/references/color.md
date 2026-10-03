# Albers and Itten on color, operationalized for screens

Reference for steps 5 and 6 of `SKILL.md`. Sources:

- Josef Albers, *Interaction of Color*, cited by chapter number, which is stable across editions. Page numbers are given for the 50th anniversary edition (Yale, 2013).
- Itten, *Design and Form*, p.32–33.

Under each chapter, the first bullets report what the book says. Every **Rules** bullet is this skill's conversion for screens (*heuristic*), not Albers, and anything marked *not Albers* or *derived* goes beyond the book.

## Terms

- **Light intensity / lightness.** Albers' word for what painters call "value"; he drops "value" because it was misused. On screens, use perceptual lightness: OKLab or OKLCH L, or CIE L\*.
- **Brightness / color intensity.** In Albers this means hue purity, "the reddest red", which is close to chroma. It does **not** mean luminance. Avoid the word unless you define it.
- **Other Albers terms:**
  - interaction
  - subtraction of color
  - vibrating / vanishing boundaries
  - film color
  - volume color
  - middle mixture
  - intersecting colors
  - color intervals and transformation
  - "psychological engineering" (presenting a study so it cannot be misread)
  - factual vs. actual facts

## Itten's color material (*Design and Form* p.32–33)

- **The seven contrasts.** Hue; light–dark; cold–warm; complementary; simultaneous; saturation (quality); extension (quantity: colored areas of different size).
- **The color wheel.** A 12-part circle built on yellow, red and blue, and a color star that Itten dates to 1921 at the Bauhaus. This is the RYB pigment tradition, so on screens use perceptual spaces instead.
- **The chessboard.** Harmonies were studied on a chessboard, free of form associations (p.32).
- **Expressive themes.** Night, Christening, Funeral, Fairground and the Seasons, to find each theme's color timbre (p.33).
- **Further reading.** Itten refers to *The Art of Color* and *The Elements of Color* for detail.

## Albers, chapter by chapter

### Memory and names (ch. I, p.3)
- **Recall varies.** Say "red" to fifty people and they picture fifty different reds, even for a famous brand red.
- **Names are scarce.** There are only about thirty everyday color names.
- **Rule:** never review color from memory or by name. Compare side by side against the reference token, in the same context. Name tokens by role.

### Tuned sets (ch. III, p.6)
- **The least desirable color papers** are "tuned" sets that claim to be failure-proof.
- **Rule:** be suspicious of palette generators. Choose and judge in context.

### Relativity (ch. IV, p.8–11)
- **One color, many faces.** One color can be made to appear as two.
- **Light and hue at once.** A ground pushes a color in lightness and in hue, at varying strength.
- **Influence runs one way.** Some colors mostly influence and others are mostly influenced.
- **Strongest case:** a small figure on a large ground.
- **Tiles cancel it.** Tile or checkerboard presentations cancel the effect. Present comparisons as pairs.

### Lightness: measure it (ch. V, p.12–17)
- **The eye misjudges.** Asked which of two colors is darker, students, painters included, were mostly wrong, year after year.
- **Photographs distort.** Black-and-white photographs make lights lighter and darks darker, and lose the middle grays.
- **Ramps without gaps.** Lines or gaps between gradation steps defeat comparison.
- **Rules:**
  - Every color token carries a numeric perceptual L.
  - "Works in grayscale" means converted by perceptual L, never by HSL desaturation or an RGB average.
  - Saturated colors look lighter than their computed L (the Helmholtz–Kohlrausch effect, *not Albers*), so confirm by eye.

### One color as two; two colors as one (ch. VI–VII, p.18–21)
- **Subtraction.** A ground subtracts its own hue and lightness from what sits on it.
- **Rule:** keep a **surface × foreground** test matrix. Test every status and semantic token at its real size on every surface it can land on: tinted dark-mode backgrounds, brand-tinted cards, selected rows.

### Transparency and space illusion (ch. IX, XI, p.24–32)
- **Believable mixtures.** A believable mixture lies between its two parents.
- **Dominance reads as on top.** The parent that dominates the overlap appears to be on top.
- **Boundaries read as distance.** Hard boundaries signal separation and distance; soft ones signal connection and nearness.
- **Middle mixture.** An exact middle mixture reads flat and frontal.
- **Rules:**
  - An overlay reads as "above" when the overlap color leans toward the overlay.
  - Boundary hardness carries layering, not only shadow.
  - Precomputed opaque tokens can simulate translucency, more cheaply than backdrop blur and more stably across themes (*heuristic*).
  - Alpha compositing happens in gamma-encoded sRGB, so check that the result looks plausible.

### Optical mixture and the Bezold effect (ch. XII–XIII, p.33; plates XIII-1 to 3)
- **Bezold's goal.** Wilhelm von Bezold, a meteorologist who designed rugs as a hobby, looked for a way to change the whole color effect of a design by adding or changing one color only.
- **Mechanism.** It works by **optical mixture**: fine, evenly distributed colors merge toward one another. That is the opposite of simultaneous contrast, and it depends on size and viewing distance.
- **The brick plate** (a student study). The same red bricks look much lighter with white mortar than with black mortar.
- **Rules:**
  - Gridlines, hairline borders, dividers, thin strokes, small markers and dense heatmap cells re-tint the whole view. Before changing a primary, try changing the fine structural color.
  - A large background works by contrast instead, and pushes the other way.
  - Thin chart lines will not match their legend swatches. Choose series colors at the rendered stroke width. Anti-aliasing makes thin strokes a literal optical mixture (*not Albers*).

### Intervals and transformation (ch. XIV, p.34–36)
- **Transposition.** A set of colors keeps its character when transposed to a higher or lower key, if its intervals and boundaries are kept.
- **Adjust first.** The original set often has to be adjusted before it can transpose.
- **No headroom.** The darkest and lightest sets leave no room to move.
- **Albers' check.** He verifies by inlaying a piece of one group into the other and comparing the boundaries.
- **Rules (dark mode and themes):**
  - Transpose the ΔL intervals between surface, raised surface, border, text and accent.
  - Don't anchor the light theme at pure white and black if it must transpose.
  - Test by insetting a dark-theme component into the light theme, and the reverse.

### Intersecting colors (ch. XV, p.37–38)
- **Fluting.** Contiguous swatches produce fluting at their shared edges.
- **Two looks at once.** A color between two grounds looks different against each.
- **Rules:**
  - A chip, divider or neutral that straddles sidebar and main, or header and body, will look like two tokens. Keep shared elements on one surface, or accept the shift deliberately.
  - Judge ramps both as a contiguous strip and isolated on mid-gray.

### Harmony and quantity (ch. XVI, p.39–44; plates XVI)
- **Recipes wear out.**
  - Harmony sets are illustrated with every color in equal quantity, shape and number, and they change once applied.
  - The rules of thumb for complementary, split, triad and tetrad harmonies can be forgotten for a while; they are worn out.
  - The skill's ban on wheel-geometry palette generators is an extrapolation from this (*heuristic*).
- **The factors no mechanical system can precalculate:**
  - quantity, form and recurrence;
  - changing light, and several lights at once;
  - reflections of light and of colors;
  - the direction and sequence of reading;
  - the materials used;
  - the related and unrelated objects alongside.
- **Cooking.** Good coloring is like good cooking. Even a good recipe needs tasting and repeated tasting while it is followed.
- **Harmony is not discarded.**
  - Albers gives up the *preference* for harmony and accepts dissonance as being as desirable as consonance.
  - Besides balance through harmony, he describes an equilibrium of color tensions, related to a more dynamic asymmetry.
  - He offers quantity, intensity and weight as principles of study.
- **Quantity.**
  - Any color can work with any other if their quantities are appropriate, and there are no comprehensive rules for finding them.
  - Quantity includes **recurrence**: weight in space and weight in time.
  - The same four colors become four different "casts" through quantity, dominance, recurrence and placement.
- **The link to Itten.** Albers' discussion of quantity overlaps only **in part** with Itten's contrast of extension, through Schopenhauer's quantity-weighted circle.
- **Rules:**
  - Budget the accent color by area **and** count.
  - A palette spec includes role proportions, because the same hues in different proportions give a different product character.
  - The 95/4/1 starting point (neutral/support/action) is a *heuristic*, not Albers.

### Film color and volume color (ch. XVII, p.45–46)
- **Film color.** A small, uniform shift applied across several colors reads as a thin transparent veil: cast shadow or cast light. Albers' check is that the shift must look equal on every color.
- **Rule for state layers.** Hover, pressed, selected and disabled layers must shift every underlying color by the same *perceived* amount. Test each layer over every surface and accent.
- **Stacking.** Stacked translucent layers darken with diminishing returns: two 40% black layers make 64%, not 80%. Watch nested modals and stacked shadows (*derived*).

### Weber–Fechner: the measure in mixture (ch. XX, p.54–58)
- **The law.** To be seen as equal steps, a series has to grow geometrically in physical terms (1, 2, 4, 8…). Equal added layers or quantities do not look like equal steps, and the steps flatten toward saturation.
- **Albers' test.**
  - In an arithmetic physical series, the boundaries between steps grow softer as the series goes on.
  - In a geometric physical series, they stay equally distinct.
  - The relativity of color deflects the law. Broad steps flute.
- **Rules:**
  - Use **equal ΔL in a perceptual space**. Perceptual L already builds in the compressive response, so a geometric progression *of L* double-corrects.
  - A scale passes when every adjacent boundary looks equally distinct in a contiguous strip.
  - Hex interpolation between distant hues fails mainly on hue and chroma (a muddy midpoint), and on uneven lightness across hues.

### Warm and cool (ch. XXI, p.59–60)
- **Relative temperature.** Warm blues and cool reds exist.
- **Divergent readings.** Judgments diverge once neutrals, green or violet are involved.
- **Unreliable depth.** That warm advances and cool recedes is not reliable perception.
- **Rules:**
  - Don't encode elevation or meaning in temperature alone.
  - Check "warm gray" neutrals against the accents they will sit beside.

### Vibrating boundaries (ch. XXII, p.61)
- **The condition.** Hues that contrast strongly but have similar light intensity.
- **The effect.**
  - A doubled or tripled edge, with shadow on one side and glow on the other.
  - Exciting at first, then aggressive and often uncomfortable.
  - It varies between viewers and with figure-to-ground quantity.
  - Its mechanism is unexplained.
  - Outside loud advertising it is seldom used, and it is widely disliked.
- **Rule:** if adjacent elements differ in hue but barely in L, fix the lightness, not the hue.

### Vanishing boundaries (ch. XXIII, p.62–64)
- **The condition.** Truly equal light intensity, between **neighboring** hues. It is not possible between strongly contrasting hues.
- **Rarity.** Very few people, including many colorists, have ever seen it.
- **Albers' view.** He called it the most exciting color phenomenon. It was usually the last exercise of his course.
- **Summary.** At equal L, distant hues vibrate and near hues vanish.
- **Rules (accessibility, *not Albers*):**
  - States distinguished only by hue fail color-blind users and dim or glare-washed screens.
  - Every pair of states needs a ΔL or a non-color cue.

### Color systems (ch. XXIV, p.65–67)
- **Systems come last.** Albers presents color systems at the **end** of the course. He calls an RYB equilateral triangle probably the most condensed and clear system (plate XXIV-1).
- **Primaries differ by discipline.** The colorist, the physicist and the psychologist count different primaries.
- **Harmony is not the only goal.** Harmonies are not the only desirable relationship.

### Method (ch. IV, XXV, XXVI and "Variants versus variety")
- **Practice before theory.** Albers puts practice first and calls his book the result of search, not research (ch. XXVI).
- **Methodical, not prescriptive.** He refuses prescriptive rules but works step by step, precisely and comparatively, by trial and error, with trials compared side by side.
- **Variants versus variety.** "For variety's sake" is a warning sign. A variant redoes the whole within one scheme.
- **"Which is best?"** The question is meaningless without a cause and a purpose.
- **Fewer means.** Restricted palettes are endorsed, with fewer means aimed at more action.

### Typography aside (ch. II, p.4)
- **Simple forms, harder reading.** Albers rejects the constructivist belief that the simpler the letterform, the simpler the reading.
- **Hardest cases.** He found all-caps the hardest reading, and long sans-serif text uneasy.
- **Status of the claim.** It is a 1963 opinion. Present-day evidence supports the all-caps point and is mixed on serif versus sans on screen (*not Albers*).

## Screens are not paper

- **Emitted light.** Screens emit light, which Albers calls "direct color" (ch. X). Pigment-mixing rules do not apply.
- **Blend modes:**
  - Alpha blending is an average.
  - "Screen" and "plus-lighter" gain light.
  - "Multiply" behaves subtractively.
- **Viewing conditions.** Albers' changing-light factor becomes:
  - display white point;
  - Night Shift and True Tone;
  - brightness setting;
  - ambient glare;
  - gamut (sRGB vs. P3);
  - OLED vs. LCD blacks.
- **After-images.** Albers' explanation of after-images (a retina tuned to three primaries) is presented as one theory and is outdated, so don't cite it. The phenomenon is real, and strong with saturated colors on dark backgrounds.
- **Paper technique.** Intarsia mounting, paper thickness, torn edges and day-glow papers don't transfer. The principle that does: remove incidental edges, shadows and borders when judging color.
- **WCAG is a separate test.** It needs 4.5:1 for body text, and 3:1 for large text and meaningful non-text UI.
