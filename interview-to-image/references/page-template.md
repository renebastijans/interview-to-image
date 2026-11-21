# Page prompt template

Only the section between `PROMPT START` and `PROMPT END` is pasted into the image generator, headings included. Everything else (frontmatter, the table at the end) is for the author. Keep source details, interviewer wording and timestamps out of the pasted section. A panel may have no dialogue.

```
---
date_created:
purpose: one sentence, what this page shows
source: transcript or profile file(s), with timestamps where they exist
intake:
  source: transcript / summary / profile / notes
  privacy: paraphrase or verbatim; what was removed
  consent: on record? for what use?
  licence_credit: licence and credit line to place outside the image, or "none"
  image_type:
  audience:
  destination: e.g. slide deck, 16:9
alt_text: "one or two sentences describing the finished image for screen readers (fill in after rendering; keep it in quotes)"
reference_images: (attach in this order, or "none")
sibling_pages:
status: draft for review
note: anonymisation status
---

# Prompt, page N: <title>

PROMPT START

<style block, with aspect ratio set>

The comic should illustrate **<the finding, one sentence>.**

**Underlying research finding:** <3 to 5 sentences, plain facts, no judgement>

**The structural device of this page is <absence or constraint>.** <what must never appear, and what the reader should notice without being told>

## The character
Age, role, manner, clothing. Keep visually identical across all panels. "Appearance is deliberately generic. Do not base on any real person. No place or organisation names."

## PANEL 1: <TITLE>
Heading with icon: **1. TITLE**
Setting, who is in frame (exact counts), expression.
Speech bubble: **"exact line"**

## PANEL 2, 3
(time-transition gutter if needed: vertical hand-lettered text, e.g. ON / THE / DRIVE / HOME...)

## PANEL 4: <TITLE>
The quiet emotional centre. Say what is absent as precisely as what is present.

## Storytelling requirements
Same character throughout, no humour, no villain, no narration. Arc as one line with arrows. "Above all, make Panel 4 quietly powerful."

## Lettering block
<from style-block.md>

## What this page must not say
- facts or quotes that belong elsewhere in the source (and why)
- numbers, names, titles, rewards, personal details not to appear
- causes the data does not support
- anything the interviewer raised first (prompted lines)

PROMPT END

## For the author
| Line | Status (verbatim + timestamp / paraphrase, no timestamp / condensed / written for the page) |
Open points for the user's call (consent, compressed timelines, weak claims, unknown outcomes).
```
