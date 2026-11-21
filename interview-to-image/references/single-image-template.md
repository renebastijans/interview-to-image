# Single-image prompt template

For any image that is not a four-panel comic page: a storyboard panel, a single illustration, a themes scene, a table or infographic. Only the section between `PROMPT START` and `PROMPT END` is pasted into the image generator. Everything else is for the author. Keep source details, interviewer wording and timestamps out of the pasted section.

```
---
date_created:
purpose: one sentence, what this image shows
source: file(s) or interview(s), with timestamps where they exist
intake:
  source: transcript / summary / profile / notes / analysis report
  privacy: paraphrase or verbatim; what was removed
  consent: on record? for what use?
  licence_credit: licence and the credit line to place outside the image, or "none"
  image_type:
  audience:
  destination: e.g. web page, 4:3
  text_in_image: none / headline / headline and quote / full labels
alt_text: "one or two sentences for screen readers (fill in after rendering; keep it in quotes)"
reference_images: (attach in this order, or "none")
sibling_images: how this relates to the others in the set
status: draft for review
note: anonymisation status
---

# Prompt, image N: <title>

PROMPT START

<style block: medium, palette (name colours, and any colour to avoid), line style, aspect ratio from the intake>

Recurring character, if any: age (say "visibly an adult in their mid-30s" if age matters), build, hair, skin tone, clothing including trousers and shoes, expression. Identical in every image of a set. "Appearance is deliberately generic. Do not base on any real person."

Scene: who is in frame with exact counts ("only one person appears; do not repeat or duplicate them"), where they are, what they hold, what the screens show ("abstract shapes only, no legible writing"), mood. Simple uncluttered background with few objects. Say what is absent as precisely as what is present.

Text in the image, hand-lettered in a bold, upright (non-italic) comic font of uniform weight (no bold or italic emphasis on any word), spelled exactly as written:
1. <caption or heading, exact, with the punctuation you want>
2. <speech bubble or label, exact>
No other text, letters or numbers anywhere in the image.
(If the image has no text: "No text, letters, numbers or logos anywhere in the image.")

What this image must not say:
- facts, numbers, names, results or causes the source does not support
- anything the interviewer raised first
- identifying detail the intake removed

PROMPT END

## For the author
| Line | Status (verbatim + timestamp / condensed / written for the image) |
Credit line and caveats to place outside the image (licence, counts are minimums, sample, year).
Open points for the user's call.
```
