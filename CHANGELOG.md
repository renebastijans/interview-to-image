# Changelog

All notable changes to this project are listed here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow [Semantic Versioning](https://semver.org/).

## [Unreleased]

## [1.1.2] - 2026-11-21

Changes come from a scripted test of the one-paste kit in a simulated fresh chat.

### Changed
- Manual kit and `SKILL.md`: the question order is now explicit (1 to 3, then 4 alone, then 5, then 6 to 8, then 9), answering ahead is accepted, and removals default to "every listed category".
- Aspect ratio is proposed from a short mapping and must be confirmed; alt text is yes for anything published or shared.
- Headline rule for paraphrase-only sources, and an invented generic character when the source gives no description.
- Prompt rules: state capitalisation and punctuation for each text line, and "no logos or brand marks on any object, including laptops and phones".
- Check step: a text-only fallback (the user reads out the words), corrections ordered people and objects first and lettering last, a question about which duplicate to keep, a stop after three failed corrections, and an edit template that keeps accepted blemishes instead of "every face and line".
- Short transcripts skip the topic list (threshold about 20 minutes or 3,000 words).
- Alt text is written in the audience's language; "none" is written when there is no credit line.

## [1.1.1] - 2026-11-21

Documentation and examples only. The skill, references and manual kit are unchanged from 1.1.0.

### Added
- README: "Worked example on open data", with one panel made from a public CC BY 4.0 interview dataset, credited in full.
- `examples/open-data/`: the panel's prompt and a source note.
- Acknowledgements: the dataset's author and host.
- `CONTRIBUTING.md`: exception to the no-real-data rule for public, open-licence, credited material.

## [1.1.0] - 2026-11-21

Changes come from a test of the manual kit on free Claude chat and free Gemini.

### Changed
- Manual kit is now one paste that runs intake, plan approval, prompt writing and image checks in the same chat. The separate moments, page-writing and render steps, and the three reference files, are an optional appendix.
- Intake: numbered questions, an explicit list of unanswered ones, "what must be removed" asked on its own, and new questions on licence and credit, the source of truth when files overlap, and text inside the image (none, headline, quote, full labels).
- Intake: "analysis report of findings" is a source type, and a scope change triggers a short extra round.
- Plan approval before prompts are written is now an explicit step.
- Source caveats (counts are minimums, sample, year) and credit lines go outside the image.
- QA: paste each render back for a check; recheck the whole image after every edit.
- README: tested-on note, manual-kit steps, iteration tips and known limits updated.

### Added
- `references/single-image-template.md` for storyboard panels, illustrations and tables.
- Reliability rules in `references/style-block.md` (exact text, lettering style, one person, age, background, drift, consistency).
- Table or infographic, storyboard strip and themes scene guidance in `references/devices-and-page-types.md`.
- QA checklist items for lettering style, duplicated people, age and clothing, background and palette, and tables.

## [1.0.2] - 2026-11-20

Documentation only. The skill, references and manual kit are unchanged.

### Added
- README: "How to cite" section (APA and BibTeX) and a link to GitHub Discussions.

## [1.0.1] - 2026-11-20

Documentation and repository housekeeping only. The skill, references and manual kit are unchanged from 1.0.0.

### Added
- `CONTRIBUTING.md`, with the rule against posting real interview data.
- "Generator feedback" issue template and a pull request template.
- `SECURITY.md` (private reporting for leaked data or unsafe instructions) and `CODE_OF_CONDUCT.md`.
- `CONTRIBUTORS.md`, `CITATION.cff` and `.github/CODEOWNERS`.
- README: licence, citation and code owner badges, a table of contents, a link to the latest release and an acknowledgements section.
- This changelog.

### Fixed
- Quoted `alt_text` in the sample prompt and the page template so the YAML frontmatter parses.

## [1.0.0] - 2026-11-20

First public release.

### Added
- Skill folder `interview-to-image/` for Claude Code and similar tools: intake interview (source, privacy, image type, audience, destination), transcript-to-moments step, page prompts with a lettering block, and a QA checklist with a fix loop.
- Manual copy-and-paste kit in `manual/manual-kit.md` for any chat assistant.
- Invented sample interview extract and page prompt, plus two anonymised example images.
- README with privacy warning, tested-on notes, the two usage paths, "after the prompt" steps and iteration tips.
- MIT licence.

### Notes
- Tested on Gemini's Nano Banana image creator in "Pro" mode (paid plan), with one run in "Auto" mode on the free tier. Other generators are untested.

[Unreleased]: https://github.com/renebastijans/interview-to-image/compare/v1.1.2...HEAD
[1.1.2]: https://github.com/renebastijans/interview-to-image/compare/v1.1.1...v1.1.2
[1.1.1]: https://github.com/renebastijans/interview-to-image/compare/v1.1.0...v1.1.1
[1.1.0]: https://github.com/renebastijans/interview-to-image/compare/v1.0.2...v1.1.0
[1.0.2]: https://github.com/renebastijans/interview-to-image/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/renebastijans/interview-to-image/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/renebastijans/interview-to-image/releases/tag/v1.0.0
