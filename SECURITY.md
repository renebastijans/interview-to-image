# Security policy

This repository holds instructions, templates and examples. It contains no executable code and calls no services, so the main risks are about data and instructions, not software vulnerabilities.

## What to report

- **Personal or confidential data in the repo.** Real interview text, names, quotes, employers, products or images derived from real interviews, in any file, commit or issue.
- **Unsafe instructions.** Text in the skill, references or manual kit that could make an assistant leak the user's data, call an external service the user did not ask for, run commands, or follow instructions hidden in interview material (prompt injection).
- **Misleading privacy claims** in the README or skill.

## How to report

Use GitHub's private reporting: open the repository's **Security** tab and choose **Report a vulnerability**. Do not open a public issue or pull request for personal data or an unsafe instruction, because that spreads it further.

Say where the problem is (file and line, or commit) and what you expect to happen instead. Do not paste the sensitive data itself if a description is enough.

## What to expect

This is a small, free project maintained by one person. Reports are read as soon as possible, with no guaranteed response time. Confirmed leaks of personal data are removed first and discussed afterwards.

## Supported versions

Only the latest release and the `main` branch.

## Your own data

Using the skill sends your text to an LLM and an image generator you choose. That is outside this repository's control. See the privacy section of the [README](README.md) before you paste real material.
