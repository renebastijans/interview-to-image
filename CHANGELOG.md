# Changelog

All notable changes to this project are listed here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow [Semantic Versioning](https://semver.org/).

## [Unreleased]

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

[Unreleased]: https://github.com/renebastijans/interview-to-image/compare/v1.0.1...HEAD
[1.0.1]: https://github.com/renebastijans/interview-to-image/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/renebastijans/interview-to-image/releases/tag/v1.0.0
