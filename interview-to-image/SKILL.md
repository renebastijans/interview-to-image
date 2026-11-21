---
name: interview-to-image
description: Turn interview transcripts, summaries or profiles into image-generation prompts, by default a multi-page hand-drawn research comic, plus a QA checklist. Use when the user wants a comic, illustrated story, storyboard or image set from interview or user-research findings, or says "comic prompt", "page prompt", "illustrate this interview". Starts with an intake interview. Writes prompts and checks results; does not itself call an image API.
---

# Interview to image

You write prompts, anonymise the material as the intake dictates, and help check the returned images. By default the user pastes the prompts into an image generator themselves. You do not generate images or call an image API yourself. If you can drive a browser and the user asks you to, you may paste a finished prompt into the generator, with the user logged in themselves and permission given; never handle their password. Then QA the result. The paid-plan tests were run this way; offer it, do not assume it.

Tested styles: a four-panel hand-drawn research comic (Gemini's image creator, Nano Banana, "Pro" mode, paid plan; one free-tier run in "Auto" mode), and, on free Claude chat plus free Gemini, a flat-colour comic storyboard, an illustration and a table infographic. Other generators are untested; say so when the user picks one.

## Workflow

### 1. Intake (before drafting anything)

Ask in short rounds (two or three questions at a time, not one long form). Skip anything the user has already answered. Do not draft until round 2 is answered.

**Round 1: source and privacy**
- What is the source: transcript, summary, profile, notes, survey free text, or an analysis report of findings? Which language? One interview or a set? If several files overlap (for example transcripts and an analysis of them), which is the source of truth? Files must be attached; a chat assistant cannot read folders on the user's computer.
- Is the image for public use (portfolio, blog, conference, shared deck) or internal/client use? May this text go into an LLM and a third-party image generator at all? Is consent on record for this use?
- Verbatim quotes allowed in the output, or paraphrase only?
- What must be removed (names, employer, role, location, products, amounts)? Ask this as its own question: in testing it was skipped when bundled. For internal or client use, with consent and data rules allowing it, real names and details may stay; ask, do not assume.
- Does the source licence require credit (for example CC BY)? If so, get the credit line; it goes outside the image.
- Default to paraphrase and full anonymisation for public use, or when the user is unsure. Say that default out loud.

**Round 2: image and audience**
- Image type: comic (the default), storyboard strip, single illustration, sketchnote, table or infographic, chart restyle, other? House style or brand constraints? Reference image to attach?
- Audience: who sees it, what should they take away, how much do they already know?
- Where will it be used (Google Slides, PowerPoint, Keynote, HTML page, document, print, social)? This sets the **aspect ratio**, the resolution, whether **alt text** is needed, and whether the output is one image or a set. Never hardcode 16:9; set it from this answer.

- **Text in the image:** none, a headline only, a headline plus a quote, or full labels? Ask up front; deciding it per image later cost a round in testing. Short exact text renders reliably; dense tables do not.

Number the questions. If any are unanswered, list the numbers and ask again before moving on. Say the answers back in one line each and let the user correct them. Record them in the `intake` block of every prompt file. If the scope changes later (new audience, new image, new takeaway), run a short extra round for what changed rather than carrying on with old answers.

### 2. Moments (transcript to candidate list)

Image prompts never contain the transcript. They contain one scene. Compress the source first:

- **Transcript:** read it, fix speech-to-text errors (names rendered several ways, misheard words), then list candidate moments: exact quote, speaker, whether the interviewer prompted it, timestamp. Flag and fix transcription errors before quoting.
- **Long transcripts:** make a first pass that lists topics, then extract moments per topic. Do not try to turn a 40-minute transcript into a comic in one step.
- **Analysis report of findings (themes, recommendations):** nothing to extract; propose the images, and carry the report's caveats (counts are minimums, sample, year, one coder) into the credit line outside the image.
- **Profile or summary:** already compressed. Mark lines "paraphrase, no timestamp" and point to the transcript for later verification.
- **Prompted versus unprompted:** keep the marker. Anything the interviewer raised first is stated intent, not behaviour; it goes in "must not say" for story pages. A line that only answers a yes/no or leading question ("were you angry?" "yes") counts as prompted; a line that adds something the question did not ask for is unprompted.
- Show the candidates with frequency where there are several interviews (e.g. "6 of 11"), then let the user choose.

### 3. Pick the arc

Default for a comic: one story page per chosen moment, plus an optional data page and an optional answers page when there is corpus-level evidence. With one interview, write one story page and flag "one interview, not a pattern". Offer a shorter version before a longer one. For other image types, propose the set of images. Say the plan back in one line per image, including which text appears inside each, and **wait for the user's approval before writing prompts**.

### 4. Write one prompt file per page

Name files `prompt-page-N-<slug>.md`. For comic pages use `references/page-template.md`; for any other image type use `references/single-image-template.md` (and `references/devices-and-page-types.md` for tables and infographics). Use the style block in `references/style-block.md` (set the aspect ratio from the intake) and the reliability rules in it, and read `references/devices-and-page-types.md` for the page type and structural device. Anonymise per the intake. Keep quoted lines short; image models spell short lines far better than long ones.

Every prompt includes a **lettering block**: only the listed lettering appears, no title, one bubble per speaker per panel, screens show grey bars only, no logos, no other text.

### 5. Hand over

Give the user these steps, in plain words:
1. Open the image generator; start a new chat for each page.
2. Paste only the text between PROMPT START and PROMPT END. Attach any reference image first. After the first accepted image of a set, attach it as a reference for the rest to keep the character consistent.
3. Zoom in and read every word against the prompt, using `references/qa-checklist.md`.
4. To fix something, reply in the same chat with an edit instruction (template in the qa-checklist); do not rerun the whole prompt.
5. Save at full size, name the file for the page, add alt text (the template has an `alt_text` field), note accepted blemishes.

### 6. QA returned images

Ask the user to paste each returned image back. If your product can read images, check it with `references/qa-checklist.md` and give one same-chat edit instruction per problem. Otherwise give them the checklist. Log accepted blemishes; do not reopen them. Every image needs a human read; treat the first render as a draft.

## Rules that carry across pages

- **One structural device per page:** the idea is made visible by an absence or a constraint. Say it in the prompt. Check sibling pages so no two repeat one.
- **Every bubble is exact:** line in bold, in quotes, "saying exactly". Mark each line verbatim, condensed or written-for-the-page in the table at the end of the file.
- **Wordless panels are allowed.** Quotes said afterwards about a moment cannot be speech in the scene. If none qualifies, draw that panel without dialogue, or put the quote outside the panels as an unattributed line. Not every panel needs a bubble.
- **Adapt the style block to the scene.** If a scene has no screen, drop or reword the "screens are the only cool light" line rather than contradicting it.
- **"What this page must not say"** on every page (this section is pasted, so write it as constraints on the drawing, not as notes about the source): facts, quotes, numbers, names and implied causes that belong elsewhere or that the data does not support.
- **Nobody is a villain.** No humour, no exaggeration.
- **Explicit counts:** panel count and group size ("exactly four colleagues"), or the generator invents.
- **Keep characters identical** across panels: restate age, hair, skin tone, clothing, build. Fix seats (left, middle, right) when panels are one conversation.
- **Data pages are restyles:** build the exact chart yourself (script or SVG), attach it, say "restyle, not redesign", add a check table (bar count, labels, ratios). Counts as "n of N", no percentages for small samples, "direction, not rates", no arrows or funnel between rows.
- **Do not show results the source does not have** (replies, ticks, tallies, typing dots).
- **Identifying detail:** names, employers, products, locations, job titles, amounts, specialty-adjacent words stay out unless the intake says internal or client use with consent. Follow the intake answer.

## Output

Each prompt file starts with frontmatter (date, purpose, source, intake answers, reference images, status) and ends with a source table and open points for the user. Prose in the user's language and spelling; keep it concise, observations separate from recommendations.
