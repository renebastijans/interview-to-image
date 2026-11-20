# Contributing

Thanks for helping. This is a small, free skill, so the process is light.

## Most useful contributions

- **Notes from other image generators.** What worked, what broke (lettering, layout drift, edits), and which prompt changes helped. Say which generator, mode and plan you used.
- **Other image types.** Single illustrations, sketchnotes, storyboards, chart restyles: what the intake should ask and what the prompt needs.
- **Fixes to the skill or references.** Unclear steps, contradictions, missing cases, typos.
- **Examples.** Invented only (see below).

## Privacy rule: no real interview data

Do not put real interview transcripts, profiles, quotes, names, employers, products or images generated from them in an issue, pull request or example. Invent your material or paraphrase it so nobody can be identified. If you are unsure, leave it out.

If you find real personal data or an unsafe instruction in this repository, do not open a public issue. Follow [SECURITY.md](SECURITY.md).

## Opening an issue

For generator results, use the "Generator feedback" issue template. Otherwise, say what you tried, what you expected and what happened. For a generator problem, include the prompt section you pasted (anonymised) and a short description of the image. Do not attach images that show real people's words.

## Opening a pull request

The pull request template has a checklist that repeats these points.

1. Keep it small and focused: one change per pull request.
2. Keep the skill short. Detail goes in `interview-to-image/references/`, not in `SKILL.md`.
3. If you change the skill, keep the manual kit in `manual/manual-kit.md` and the README consistent with it.
4. Say what you tested and on which generator. Untested changes are fine if you mark them as untested.
5. Check YAML frontmatter still parses: quote any value that contains a colon followed by a space.

## Style

British English, plain wording, no jargon. Short sentences. Examples must be invented.

## Licence

By contributing you agree your work is released under the repository's [MIT licence](LICENSE).
