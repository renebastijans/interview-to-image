# Manual kit: copy and paste, no coding tool needed

Use this with any chat assistant (Claude, ChatGPT, Gemini, others) and any image generator. You do three pastes, then render.

**Privacy first.** Anything you paste goes to a third-party service. For public use, anonymise before pasting (names, employer, role, location, products, amounts) and check you have consent. For internal or client use, real names and details are fine only if consent and your data rules allow it. When unsure, paraphrase.

## Step 1: intake (paste into your chat assistant)

```
You are helping me turn interview material into prompts for an image generator. Interview me first, in short rounds of two or three questions, and wait for my answers. Do not write any prompt until I have answered rounds 1 and 2.

Round 1: What is my source (transcript, summary, profile, notes, survey free text), in which language, one interview or several? Is the image for public use or internal/client use? May this text go into an LLM and a third-party image generator? Is consent on record? Are verbatim quotes allowed in the output or paraphrase only? What must be removed (names, employer, role, location, products, amounts)? Default to paraphrase and full anonymisation for public use or if I am unsure; for internal/client use with consent, real names and details may stay.

Round 2: Image type (comic, single illustration, storyboard strip, sketchnote, chart restyle, other), house style or brand limits, reference image? Audience, and what should they take away? Where will it be used (Google Slides, PowerPoint, Keynote, web page, document, print, social)? From that, tell me the aspect ratio to use and whether I need alt text.

Then repeat my answers back in one line each.
```

## Step 2: moments (paste your source after this)

```
Here is my source material, already anonymised as agreed. 

1. If it is a transcript, fix obvious speech-to-text errors (names spelled several ways, misheard words) and tell me what you changed.
2. List 5 to 8 candidate moments. For each: the exact quote (short: under 15 words if possible), who said it, whether the interviewer prompted it, and a timestamp if there is one. If there are several interviews, say how many of them show the same moment.
3. Do not choose yet. Wait for me to pick.

[PASTE SOURCE HERE]
```

For a long transcript, ask first for "a list of topics only", then run step 2 on one topic at a time.

## Step 3: write the page prompt (after you have picked a moment)

Open these files from this repo and paste their contents into the same chat first, in this order: `interview-to-image/references/style-block.md`, `interview-to-image/references/page-template.md`, `interview-to-image/references/devices-and-page-types.md`. Then paste:

```
Write one page prompt for the moment I chose, following page-template.md, with the style block (aspect ratio from my intake) and the lettering block. Rules: one structural device for the page, every bubble exact and in bold, a "What this page must not say" section, nothing the interviewer prompted shown as behaviour, no names or identifying detail, no results the source does not report. Keep every quoted line short. Mark each line verbatim, condensed or written-for-the-page in a table after the prompt. Mark where the prompt starts and ends with PROMPT START and PROMPT END.
```

## Step 4: render and check

Follow "After the prompt" in the main README. Use `interview-to-image/references/qa-checklist.md` to check the image and the fix-loop wording to correct it.
