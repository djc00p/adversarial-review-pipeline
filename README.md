# adversarial-review-pipeline

[![ClawHub Skill](https://img.shields.io/badge/ClawHub-Skill-blue)](https://clawhub.ai/djc00p/skills/adversarial-review-pipeline)

Adversarially review a code change before it ships - a single-agent severity-graded review that works anywhere, an optional three-agent Writer/Breaker/Reviewer pipeline, and an optional five-agent pipeline with a fix loop and browser verification. Use when: reviewing a diff, branch, or PR before merge; checking a feature for bugs, security issues, or unnecessary complexity; asking whether a change is over-engineered or missing edge cases; or setting up a review workflow for a team. Triggers: adversarial review, review this PR, break this change, find problems with this diff, code review, YAGNI check, over-engineering review.

---

## Install

Install from ClawHub:

```bash
clawhub install adversarial-review-pipeline
```

Or clone this repo and add the skill folder to your agent's skills path.

## Usage

This skill activates automatically when a request matches its description.
See `SKILL.md` for the full instructions the agent follows.

## Repository layout

```
SKILL.md      # agent instructions
LICENSE       # MIT-0 / MIT
README.md     # this file
```

## Versions

Releases track the published ClawHub versions.

| Version | ClawHub |
| --- | --- |
| 1.0.1 | [adversarial-review-pipeline v1.0.1](https://clawhub.ai/djc00p/skills/adversarial-review-pipeline) |

---

**Published by [@djc00p](https://github.com/djc00p)**
