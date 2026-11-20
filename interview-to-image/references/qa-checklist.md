# QA checklist (per returned image)

Read every line of lettering at full resolution and compare it with the prompt's exact lines. Treat the first render as a draft.

- [ ] Every bubble, label, heading and notebook line matches the prompt word for word, including punctuation
- [ ] Every word of every bubble is present (a dropped word, e.g. "when can." for "when you can.", is a lettering error)
- [ ] No other lettering (charts, walls, badges, mugs). Garbled incidental text: regenerate or log as an accepted blemish
- [ ] No unprompted title or caption above the panels
- [ ] No company, person, product, provider or place name anywhere
- [ ] Panel count correct; panels not split unprompted; layout as requested (row versus grid)
- [ ] Exact head counts match ("exactly four colleagues")
- [ ] Same character across panels (face, hair, skin tone, clothing); same people and seats in consecutive panels of one scene
- [ ] Each bubble's tail points to the right speaker; one bubble per speaker per panel; no repeated or garbled copy of a line; no third speaker
- [ ] Hands and arms connect to bodies and sleeves, nothing cropped between
- [ ] Screens: no QR-like squares, codes, logos or legible text where the prompt says none
- [ ] "Must not say" list respected: no numbers, rewards, results, answers not asked for
- [ ] The absence device holds (e.g. blank screen, no product shown, key object missing from the last screen)
- [ ] Redaction bars sit exactly where the prompt lists them; no invented name replaces one
- [ ] Role or rank signal present in every panel for the person it applies to, and nobody else has it
- [ ] Panel headings in the same position as the sibling pages
- [ ] Recurring props match the earlier page they echo; log differences
- [ ] Data pages: bar count, labels, order, ratios and flat bands match the check table (measure in pixels); solid and dashed counts per row; one accent colour; counts and footnotes exact
- [ ] No result shown where none is known (replies, ticks, tallies, typing dots)

## Fix loop

To fix one problem, reply **in the same chat** with an edit instruction rather than re-running the whole prompt, which redraws the faces:

> Regenerate this exact image and change nothing else, with one correction: in panel N the text currently reads "…". It must read exactly "…". Keep every face, seat, layout, bubble and line of lettering exactly as it is.

In testing this held on the first try. Edits can still undo earlier fixes or cover text when a hand is moved, and can change other panels (clothing, framing). Name the panel to change, say what must stay in frame, fix an empty area by cropping rather than repositioning one element, and recheck every panel after each edit. If the generator distorts a chart, place the exact chart (SVG) over its paper and figures.

Log accepted blemishes (page, what, why accepted) in a notes file and do not reopen them.

## PDF build (only when asked)

Full resolution: an HTML wrapper with one page image per page, printed with headless Chrome using `--print-to-pdf --no-pdf-header-footer`, with the page size matching the aspect ratio. Light copy for email: resize with `sips -Z 2000` (macOS), JPEG quality about 72, then the same print step. Rebuild both if any image changes.

## Before sharing

Re-confirm interviewee consent, whether quotes are paraphrased, and whether real figures may be shown.
