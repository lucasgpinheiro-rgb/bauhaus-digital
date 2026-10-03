# Müller-Brockmann: grid, units, type, consistency

Reference for steps 0, 3, 4, 5 and 12 of `SKILL.md`. Source: Josef Müller-Brockmann, *Grid Systems in Graphic Design / Raster­systeme für die visuelle Gestaltung* (Niggli, 1981). Page numbers are the printed pages of that edition. Anything marked *heuristic* is this skill's conversion.

## Definition (p.11)

- **What a grid divides.** A grid divides a two-dimensional plane into fields, or a three-dimensional space into compartments.
- **Field width** equals the column width.
- **Field depth** is a fixed number of text lines.
- **Field spacing:** fields are separated by 1, 2 or more empty lines.
- **Smallest unit:** the smallest illustration corresponds to the smallest field.
- **Illustrations as fields.** Illustrations, tables and statistics are treated like grid fields: 1, 2, 3, 4 **or more** fields. The English translation drops "or more"; the German has it, and the plates run up to 16 fields (p.122) and full pages (p.113).
- **Combined fields** must still align their edges with text lines (p.60).
- **The quiet rule.** The **fewer distinct sizes** of illustration, the quieter the impression (p.11). The rule is about the number of distinct sizes, not how far apart they are.
- **The opposing pull.** Size contrast between pictures creates tension (p.70), and finer grids allow more complex rhythms (p.87). Use few sizes, contrasted on purpose.
- **History.** He first set out the grid briefly in *Gestaltungsprobleme des Grafikers / The Graphic Artist and His Design Problems* (1961), with 28 examples. *Grid Systems* (1981) codifies it. Grid-designed printed matter first appeared in Switzerland in the late 1940s (p.7–8).

## Order of work

1. **Study the problem:** format, text, illustrations, captions, typeface, printing method, paper (p.49, 55).
2. **Inventory the content.** How many columns? Footnotes? How many pictures, how many large and how many small (p.55)? For complex grids, start with a rough draft of the priorities (p.92).
3. **Choose type size and leading.** Then adjust field depth to whole lines (second method, p.61–62).
4. **Sketch.** Make small sketches in the final proportion. Try 2, 3 and 4 columns at several type sizes (p.57–58).
5. **Narrow down.** Reduce to 2–3 sketches and enlarge them to 1:1 (p.58).
6. **Choose one.** Sketch the real type lines, overlay the grid, fit the lines to the fields and calculate.
7. **Check the margins**, and start again from the beginning if they fail (p.60).

**Accurate, not low-fidelity.** A good sketch can look like a reduced print. Drawing vague, heavy lines for text is a very common mistake, because the text then does not fit at 1:1 (p.49, 94–95). The digital version is small but faithful: real type sizes and real copy length, at the target aspect ratio.

His remark that the final solution is rarely found at the first attempt (p.58) refers to fitting text lines into fields. The spirit carries over to the whole process, which may have to start again from the beginning (p.60).

## Columns and fields

- **Column options** (p.57):
  - 1 column leaves too little freedom for picture sizes.
  - 2 columns subdivide into 4.
  - 3 columns subdivide into 6, and their narrow lines may need smaller type, depending on the task.
  - 4 columns suit much text with many pictures, and subdivide into 8, 16 or more, which is convenient for statistics.
- **One column still needs skill.** A one-column page needs the same skill and sensitivity as an 8-column one (p.53).
- **Combining systems:** 2 with 3 or 4; 4 with 8 (p.52–53).
- **Field counts follow line counts.** A 53-line column gives 9×5 or 6×8 fields; a 59-line column can be divided 5 ways (p.67). For fixed slides and tiles, choose heights whose unit count has useful divisors.
- **Fine grids need discipline.** Grids of 32 to 72 fields suit periodicals and catalogues, but demand more self-discipline and risk confusion (p.87, 92, 129–130).
- **12 columns is a screen convention**, not his (*heuristic*). His "12-part" examples mean 12 fields (p.108–110).

## The vertical unit (the part that survives responsive layout)

- **Matched leading.** With 3–4 type sizes, the leading of each size must be adjusted to the others (p.34).
- **Worked sets:**
  - 7/1, 10/2 and 20/4 pt all fit a 24 pt unit (p.66).
  - 6 pt captions set solid, 2 lines, equal one 10/2 text line (p.59). The English says "20 lines"; the German says 2, and only 2 adds up.
  - The book itself is set 9/3 text and 7/1 captions, so 3 caption lines equal 2 text lines, which equal 24 pt (p.87).
- **Whole lines only.** Gaps between blocks are whole empty lines, **never halves**, or adjacent columns stop aligning (p.64, 80, 106, 134).
- **Gaps by role.** Gaps between title and text, text and caption, or sections are one or more lines, or one grid unit (p.80).
- **Uneven gutters.** Vertical gaps between pictures are larger than horizontal ones when captions sit beneath (p.63).
- **Worked example** (p.58–59). It needs a fixed format:
  - The column has 57 lines, split into 4 fields with 1 empty line between them, so 3 empty lines.
  - 57 − 3 = 54, and 54 ÷ 4 = 13.5. There are no half lines, so round down to 52, giving 13 lines per field.
  - The column becomes 4 × 13 + 3 = 55 lines.

**On screens** (*heuristic*):

- one base unit (4 or 8 px);
- line heights, spacing and component heights as multiples of it;
- `row-gap` and `column-gap` as separate tokens, the row gap sized for whatever label sits beneath.

**What breaks:** field depth in lines, and exact baseline registration across reflowing columns. **Exception:** slides, printable reports, fixed dashboard tiles and social images get the full method.

## Type

- **Faces.** Medium-width faces read most easily (p.17). Keep condensed faces for labels and figures (*heuristic*).
- **Letterspacing.** Phototypesetting tended to set letters too tightly, which hurts legibility, so insist on normal spacing (p.19, 30). Do not track body text negatively (*heuristic*).
- **Measure.** By an empirical rule, about 7 words per line (p.30, 53, 64). In the same chapter he says a column reads easily at about 10 words (p.31).
  - Too long tires the eye, which must hold the horizontal over a long distance.
  - Too short tires it by forcing constant line changes.
  - Both reduce how much of the text is remembered (p.30–31).
  - On screens, count characters: 45–75 (*heuristic*, after Bringhurst). Words per line drift between languages.
- **Reading distance sets type size.** He calculates size for a 30–35 cm reading distance (p.30, 58). Phones are held at about that distance; desktops are further away. Kiosks, TV dashboards and projected slides need an explicit viewing distance before sizes are chosen. His 3D chapter works from eye height (about 170 cm) and the maximum readable distance (p.141–145).
- **Size follows measure.**
  - A 20 pt face needs a wide column and an 8 pt face a narrow one.
  - In mixed widths, wider columns need larger type to keep the same rhythm (p.31–32, 53–54).
  - Over one column, choose the width that suits the body text, and let large headings wrap.
  - On the web, use `clamp()` or container query units.
- **Leading.** Too tight, and the eye doubles lines while the page darkens. Too loose, and lines isolate and the text looks dead. Long texts need more leading **and** paragraph breaks: an empty line, an indent or an initial (p.34–37).
- **Hierarchy.**
  - Size steps must be clearly recognizable (p.45).
  - Medium, semibold and bold work as light, medium and deep gray (p.46).
  - Never mix faces of the same style: no two similar grotesques, no two similar romans (p.47).
  - Light weights suit small captions.
- **Titles.** He shows eight ways to set a title (p.45–47). They range from the same size set apart by white space (elegant and restrained) to bold, larger, italic or ruled.
- **Ragged or justified.** He does not prescribe ragged right. He shows ragged text with even word spacing and few hyphenations (p.64), and allows justified, ragged or centered lines (p.80).
- **Reversed text.** Light-on-dark text should be short and set with generous leading (p.129).

## Pictures and panels

- **Picture edges.** The top of a picture aligns with the cap height, and the bottom with the descender line (p.65). On the web, use `text-box-trim` or cap-height alignment.
- **Cut-outs and irregular illustrations** are stabilized on a tint or panel the size of a grid field. Line illustrations take the column width (p.97–100).
- **Edge-to-edge pictures** with no gap are justified only when they deliberately build an atmosphere together (p.69).
- **Text on a tint.** Text running right to the tint's edge is unsatisfactory. Either inset the text inside the tint, or extend the tint beyond the column so the text stays aligned. Neither is perfect, so choose which one sits on the grid (p.101–103). Color alone, without a panel, is another option (p.103).

## Space

- **Space as an element.** New typography treats the unprinted ground as an element of design, on a par with the others (p.20).
- **Rest zones.** Space between a title and its text creates a rest zone that emphasizes the title (p.69).
- **Activation.** Pictures should activate the unprinted space (p.70).
- **Separation aids reading.** Separation between images helps the reader recognize and understand the content (p.82).
- **Placement steers the eye.** The eye is guided by the placing and accentuation of elements (p.76).

## Margins (fixed frames: slides, hero sections, dialogs, cards)

- **Margin size.** Too small feels overfull; too large feels extravagant (p.40).
- **Type area position.** Set too high, it seems to fly away; set too low, it seems to drop out (p.40–41, 51).
- **Equal margins** on all sides look indecisive and dull (p.41).
- **Large type** in wide columns needs larger margins (p.33).
- **Persistent elements.** Page numbers, and by extension pagination, metadata and footers, sit on a text line, at the same distance as the column gap (p.42–44).

## Consistency list (corporate identity, p.133–136)

Use this as the design-system review:

- titles at the same size and in the **same position** on every page;
- subtitles at the same size, and the same distance from the text before and after;
- captions at the same size, and in the same relation to the image;
- the same grid on every page;
- pictures only in field sizes;
- one photographic approach;
- statistics in one consistent form;
- **the same colors for the same kinds of content**;
- the same leading for the same type size;
- whole empty lines only.

The system must also handle functions that will only become apparent in the future (p.133). Designing the cover apart from the inside breaks the system (p.135). A corporate identity cannot come from creativity that is purely emotional in origin (p.174).

## Attitude

- **The grid as attitude.** The grid expresses a mental attitude: the will to systematize, to clarify, to concentrate on essentials (p.10).
- **Honesty and analysis.** The grid compels honesty in the use of design means, and analysis of the problem (p.11). It fosters analytical thinking (p.12).
- **No guarantee.** A grid is no guarantee of success. It still needs a sense of composition (p.75).
- **Not a restriction.** The belief that the grid restricts creativity is a widespread misconception (p.104).
- **Caution.** On p.13 he calls it a scientifically proven fact that clearly structured information is better understood and remembered, without a citation. Do not repeat it as a proven claim.

## What does not transfer to responsive screens

- **Field depth as a line count, and cross-column baseline registration.** Text reflows with the viewport and the user's font size.
- **Binding margins, folding and trimming tolerances** (p.39–41, 51, 124). The nearest analogues are device safe areas (notches, rounded corners, TV overscan).
- **DIN paper sizes** (p.15–16). The idea of a few standard formats maps to a few breakpoints and slide ratios, but the values don't.
- **Ciceros and points, and the golden-section type area** (p.17–18, 51–52). What survives is one unit system for type and layout, stated exactly. On screens that means tokens.
- **Words per line as the metric.** Use characters.
- **Folio placement psychology** (p.42–44). It depends on turning physical pages.
