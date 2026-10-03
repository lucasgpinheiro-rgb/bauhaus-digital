# Sources, editions and how they were checked

## The three books

| Short | Book | Edition used for page numbers |
|---|---|---|
| Itten | Johannes Itten, *Design and Form: The Basic Course at the Bauhaus and Later* (German original: *Mein Vorkurs am Bauhaus: Gestaltungs- und Formenlehre*, 1963) | Revised edition, 1975 (Van Nostrand Reinhold; later John Wiley & Sons reprint). Printed page numbers. |
| M-B | Josef Müller-Brockmann, *Grid Systems in Graphic Design / Rastersysteme für die visuelle Gestaltung* | Niggli, 1981 (first edition; US edition Hastings House). Later printings, including the 1996 4th revised edition, appear to keep 176 pages, but their pagination was not checked. |
| Albers | Josef Albers, *Interaction of Color* | 50th anniversary edition, Yale University Press, 2013. Chapters are cited by Roman numeral, which is stable across editions; page numbers refer to this edition. |

Other works mentioned: Robert Bringhurst, *The Elements of Typographic Style* (the 45–75 character measure), and Jan Tschichold, *Die neue Typographie* (1928).

## How the skill was checked

Before its 1.0.0 release, this text was audited against all three books, with every page read. Each claim was marked as confirmed, wrong or not in the book, and the wrong ones were corrected. Corrections that matter if you are comparing with older material on Itten and Müller-Brockmann:

- **The Weimar door lock** (Itten p.66). The metalwork is by the student Naum Slutzky, in a project Itten set up with his students to design a room in one form character (p.65–66), not by Itten.
- **Itten "expelled".** By his own account he chose to leave in 1923, after Gropius said he could no longer answer for Itten's methods (p.13).
- **The form characters.** Itten calls the square's movement *tense* (p.62). Associations such as "static", "alert" or "identity" are product heuristics, not Itten.
- **One accent versus several.** Itten describes several equal accents as *movement*, a valid choice, not as failure (p.63).
- **The grid's date.** *Grid Systems* dates from 1981. The 1961 book is *The Graphic Artist and His Design Problems*.
- **Line length.** Müller-Brockmann gives about 7 words per line and also about 10. The 30–35 cm distance he cites governs type size, not line length (p.30–31). The 45–75 character range comes from Bringhurst.
- **Sketches.** Müller-Brockmann's sketches are small but **accurate** (p.49, 94–95), not low-fidelity.
- **Albers on color systems.** Albers rejects harmony *recipes*, not color systems or RYB as such (ch. XVI, XXIV).
- **Weber–Fechner.** The equal perceived steps that Albers' law aims at are equal ΔL in a perceptual space, not a geometric progression of L.
- **The Bezold effect.** It is optical mixture of fine, evenly distributed elements, which is the opposite of contrast (ch. XIII).

## Translation slips inside Müller-Brockmann's English text

- **p.11.** The English reads "1, 2, 3 or 4 grid fields"; the German says "1, 2, 3, 4 oder mehr" (or more).
- **p.11.** The English reads "the fewer the differences in the size"; the German means the fewer *distinct sizes*.
- **p.59.** The English reads "the 20 lines of 10 points"; the German says 2 lines, and only 2 makes the arithmetic work.

## Heuristics in this skill (not from the books)

- **Numbers:**
  - 1 dominant + ≤2 subordinate contrasts;
  - 12 / 16 / 24 columns;
  - 2–3 card widths;
  - 4/8 px base unit;
  - 45–75 characters (Bringhurst);
  - 7–12 tonal steps;
  - OKLCH;
  - 95/4/1 color quantities (neutral/support/action), with the action color under ~5% of the area;
  - "at most one structural break per screen".
  - the viewing-distance conversion (text height ≈ 0.007 × distance);
  - the alert cap ("+N") and "normal states carry no hue".
- **Mappings:** the product meanings given to square, triangle and circle, and the digital column of the contrast table.
- **Accessibility rules:** WCAG, color-blindness, and dim screens.
- **Product translations:** every **Rules** bullet in `color.md`, the accent modes mapped to screen types, the disc-and-path sizing, token pairs and the surface × foreground matrix, the dark-mode inset test, intermediate forms as motion design, and the three-directions exercise as a design process.
- **The deliverable format** and the checklist wording.

## Quotations

The skill paraphrases the books and cites pages; it does not reproduce them. To quote an author to the user, check the wording in the book itself.
