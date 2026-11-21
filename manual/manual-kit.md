# Manual kit: copy and paste, no coding tool needed

Use this with any chat assistant (Claude, ChatGPT, Gemini, others) and any image generator. You paste **one prompt**, answer its questions, then render. The assistant does the rest in the same chat: intake, plan, prompts, and a check of each image you send back.

**Privacy first.** Anything you paste goes to a third-party service. For public use, anonymise before pasting (names, employer, role, location, products, amounts) and check you have consent. For internal or client use, real names and details are fine only if consent and your data rules allow it. When unsure, paraphrase.

**Attach files, do not give paths.** A chat assistant cannot read folders on your computer. Attach your source files (transcripts, summaries, an analysis report, a licence or source note) to the chat.

## The one paste

Paste this into a new chat, then answer its questions.

```
You are helping me turn research material (interview transcripts, summaries, profiles, notes, or an analysis report of findings) into prompts for an image generator. You write prompts and check images; you do not make images. Work in the stages below and do not skip ahead.

STAGE 1, INTAKE. Interview me in short rounds and wait for my answers. Ask the nine numbered questions below in this order and in these groups: 1 to 3, then 4 on its own, then 5, then 6 to 8, then 9. Do not write any prompt until all nine are answered. Start your first message by saying you have the attached file(s). If I answer ahead, accept it. If I skip a question, list the unanswered numbers and ask again before moving on.

Source and privacy:
1. What is my source (transcript, summary, profile, notes, survey free text, or an analysis report of findings)? In which language? One interview or several? Which attached file is the source of truth if files overlap?
2. Is the image for public use or internal/client use? May this text go into an LLM and a third-party image generator? Is consent on record for this use?
3. Are verbatim quotes allowed in the image, or paraphrase only?
4. What must be removed (names, employer, role, location, products, amounts)? Ask this on its own. Remove every listed category unless I say it may stay.
5. Is the source under a licence that needs credit (for example CC BY)? If yes, what credit line should appear outside the image?
Default to paraphrase and full anonymisation for public use or if I am unsure; for internal/client use with consent, real details may stay. Say this default once, in your first message. Only the categories I name in question 4 are mandatory removals; apply the rest of the default unless I say they may stay.

Image and use:
6. Image type (comic page, storyboard strip, single illustration, sketchnote, table or infographic, chart restyle, other)? House style or brand limits? Reference image to attach?
7. Audience, and what should they take away?
8. Where will it be used (slide deck, web page, document, print, social)? From that, propose the aspect ratio (widescreen slide deck 16:9, older slide deck 4:3, web page 4:3 or 16:9, document page 3:4 or 4:3, social square 1:1 or portrait 4:5) and ask me to confirm it. Say whether I need alt text (yes for anything published or shared) and ask which language the alt text and any text in the image should be in.
9. Text in the image: none, a headline only, a headline plus a quote, or full labels? (Short exact text renders reliably; dense tables do not.) If quotes are paraphrase-only, you write any headline yourself, as a short phrase of at most three words reused from the source, and mark it written for the image.

Then repeat my answers back in one line each, including the aspect ratio to confirm, and let me correct them. If the source has no description of the people (age, hair, clothing), propose a generic invented character (choose gender neutrally unless the source says) and say it is invented. If a file header mentions interviews you cannot see (for example "4 of 9"), count only the files attached and say so. If my scope changes later (new audience, new image), run a short extra round for what changed.

STAGE 2, PLAN. If the source is a long transcript (a file of more than about 3,000 words), list topics first; for a short one, go straight to moments. List candidate moments: exact quote (under 15 words if possible), speaker, whether the interviewer prompted it, a timestamp if there is one, and how many interviews show it. Fix obvious speech-to-text errors and tell me what you changed. For a profile, summary or analysis report, propose the images instead. Then propose the set of images (one line each, with what each shows and which text appears inside it) and wait for me to approve or change it. One interview is not a pattern: say so, and challenge any takeaway of mine that generalises from one interview.

STAGE 3, PROMPTS. Write one prompt per image, one at a time, each between the lines PROMPT START and PROMPT END, with these parts:
- a style block with the aspect ratio from my intake, and the same character description repeated in every image (age, hair, skin tone, clothing; say "visibly adult" if it matters);
- the scene, where the text sits (for example "in the empty space at the top"), what any screen shows (blank grey or abstract blocks only), objects that would carry writing (paper, screens, signs) shown as lines or blocks only, with exact counts ("only one person appears; do not duplicate them"), a simple uncluttered background with few objects, and a named palette with any colour to avoid, and "no logos or brand marks on any object, including laptops and phones";
- the text that appears in the image, each line in quotes, "spelled exactly as written", with the capitalisation and punctuation I want stated (for example "capitals, no full stop"), in an upright, uniform-weight font, followed by "No other text, letters or numbers anywhere in the image". Keep lines short;
- a short "What this image must not say" list: facts, numbers, names, results or causes the source does not support, and anything the interviewer raised first;
- for tables: at most four rows per image, per-row counts written out ("exactly three filled and two empty"), negative rules for anything that went wrong before, and tags or labels in an empty margin, not over cells.
After each prompt, give a table marking every line as verbatim (with timestamp), condensed, or written for the page, plus a draft alt text (in the language of my audience) and the credit line to place outside the image, or "none" if there is none. Put any source caveats (counts are minimums, sample, year) outside the image too.

STAGE 4, CHECK. I will paste each image back. If you cannot see images, ask me to read out every word and describe every figure instead. Check it word by word against the prompt: spelling, punctuation, capitalisation, font style (upright, uniform weight), logos on objects, dropped or repeated words, extra text, duplicated people, age and clothing drift, palette, background clutter, counts, and anything on the "must not say" list. Say what is wrong and give one same-chat edit instruction per problem, in this form: "Regenerate this exact image and change nothing else, with one correction: ... Keep everything else exactly as it is, including any blemish I have accepted." If a problem involves two duplicated people, ask me which one to keep, and in the same message send the corrections that do not depend on my answer. Send one correction at a time, in this order: people and objects first, lettering last, and I will paste the result back after each. If I describe the image only partly, ask for the rest before you call it fine. Ask me which blemishes I accept, name them in later corrections, and do not reopen them. Keep a count of attempts at each correction; after the third failed attempt at the same one, suggest fixing it in an image editor, and when I paste the edited image back, check it once more. When all is done, end with a final recap: the accepted image(s), alt text, credit line (or "none") and caveats to place outside the image.
```

## After the prompt

1. Open your image generator and start a new chat for each image.
2. Paste only the text between `PROMPT START` and `PROMPT END`. Attach any reference image first. After the first accepted image, attach it as a reference for the rest to keep the character consistent.
3. Paste each result back into the chat assistant for the check, then use its edit instruction in the same generator chat. See "After the prompt: render and check" in the main README.

## Optional: more control

The one paste is enough for most work. If you want the exact templates, paste these into the same chat after the intake and before Stage 3, in this order, and say "use these templates":

- `interview-to-image/references/style-block.md`
- `interview-to-image/references/page-template.md` (comic pages) or `interview-to-image/references/single-image-template.md` (any other image)
- `interview-to-image/references/devices-and-page-types.md`

To check images against the full list, paste `interview-to-image/references/qa-checklist.md` before Stage 4.
