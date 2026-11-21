# Style block (paste at the top of every comic page prompt)

Set the last line from the intake (where the image will be used). Adjust or replace the whole block if the user wants another style or has a house style.

Create a new four-panel research comic using the following aesthetic and presentation criteria:

- hand-drawn ink illustration with a soft, muted colour wash: watercolour or coloured pencil laid over a visible pen line, never flat digital fill
- a restrained, desaturated palette: warm greys, ochres, muted browns, soft natural skin tones, with plenty of bare paper left showing through
- **screens are the only cool light in the comic**: a phone or laptop glows a pale blue-grey against the warm surroundings, so the reader's eye lands on it without needing to be directed there
- colour should stay quiet enough that the ink line still carries the drawing; if in doubt, use less
- realistic rather than cartoonish characters
- fine cross-hatching and sketch shading, still visible through the colour
- expressive faces and body language
- clean bordered comic panels
- hand-lettered comic text
- slightly imperfect, wrinkled white paper resting on a wooden surface
- minimal dialogue
- strong visual storytelling
- the final panel should carry the greatest emotional weight
- the image should be <ASPECT RATIO FROM INTAKE, e.g. widescreen 16:9 for a slide, 4:3 for a document page, square for social>

## Lettering block (add to every prompt)

- The only lettering in the image is the panel headings and the lines given below, spelled exactly as given.
- No title above the panels. No captions other than those listed.
- Only one speech bubble per speaker in each panel, and nobody else speaks. The bubble tail points to the speaker.
- Screens show grey bars only: no squares, codes, icons or legible text.
- No logos, brand names, wall charts with lettering, badges or labels.
- Four panels in one row, left to right (say this if the single row matters; otherwise the generator may use a 2x2 grid).

## Variants

- **Data or restyle page:** drop the characters, bubbles and "final panel" lines; add "This is a restyle, not a redesign: keep the layout, every bar, every number and every word exactly as in the attached image."
- **Answers or recommendations page:** "no speech bubbles or thought bubbles anywhere"; proposals as grey pencil on cream, no colour wash, so they read as not yet real.
- **Later pages of a set:** "Create a new page for the same hand-drawn research comic as the attached image(s)" and attach earlier pages.

Panel headings: a small icon and a hand-lettered "N. TITLE" inside the frame at the top, consistent across pages.

## Reliability rules (any style)

These fixed real defects in testing on Gemini (Nano Banana), including a free-tier run. Add the ones that apply.

- **Exact text:** put each line in quotes, say "spelled exactly as written", then "No other text, letters or numbers anywhere in the image". Short lines came back correct every time.
- **Lettering style:** ask for an upright (non-italic) font of uniform weight, with "no bold or italic emphasis on any word". Without it, one word came back bold and a caption came back italic. Write the caption with the punctuation you want: a stray full stop appeared after a caption in one render.
- **One person only:** "Only one person appears; do not repeat or duplicate them." A character was drawn twice until this was added.
- **Age:** "visibly an adult in their mid-30s". "Mid-30s" alone drew a face that looked younger.
- **Background:** "simple uncluttered background with few objects". Name the palette and add "avoid brown" (or the colour that crept in).
- **Small details drift** (trousers colour, laptop open or closed, grille badge, a tiny icon too small to read at web size). State them explicitly, make key icons large, and accept small ones as blemishes.
- **Logos and plates:** "no logos, no brand marks, no licence plate text, grille and badge blank".
- **Consistency across a set:** repeat the identical character description in every prompt, and attach the first accepted image as a reference for the rest.
- **Each regeneration can change something else.** After every re-run, recheck the whole image, not only the part you fixed.
