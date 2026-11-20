# Changelog

All notable changes to this project are listed here. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and versions follow [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Added
- `CONTRIBUTING.md`, with the rule against posting real interview data.
- "Generator feedback" issue template and a pull request template.
- `SECURITY.md` (private reporting for leaked data or unsafe instructions) and `CODE_OF_CONDUCT.md`.
- Licence badge and a link to the latest release in the README.
- This changelog.

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

[Unreleased]: https://github.com/renebastijans/interview-to-image/compare/v1.0.0...HEAD
[1.0.0]: https://github.com/renebastijans/interview-to-image/releases/tag/v1.0.0
