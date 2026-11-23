## Description:

Adversarial review pipeline for any language or framework. Review a change the way someone who wants it to fail would, finding what is wrong with it before it ships.

Three tiers. Tier 1 is a single-agent severity-graded review that works anywhere with no dependencies. Tier 2 adds a three-agent Writer / Breaker / Reviewer pipeline. Tier 3 adds a five-agent pipeline with a fix loop, system-spec writing, and browser verification.

This skill is ready for commercial/non-commercial use.

## Publisher:

[djc00p](https://clawhub.ai/user/djc00p)

### License/Terms of Use:

MIT-0

## Use Case:

Developers and agent operators use this skill to review a diff, branch, or pull request before merge, to check a feature for bugs, security issues, or unnecessary complexity, and to decide whether a change is over-engineered or missing edge cases. The single-agent tier works with any language and framework; the multi-agent tiers apply when subagents are available.

### Deployment Geography for Use:

Global

## Known Risks and Mitigations:

Risk: An adversarial review may over-report low-value findings and create more work than it removes.

Mitigation: Grade every finding by severity and block only on real defects. Record explicitly what was skipped and why, so reviewers can see the coverage boundary.

Risk: Agent reviewers may review the code as written rather than the behavior the change is supposed to produce, letting a spec that was written to match the implementation pass unnoticed.

Mitigation: Require the review to state the intended behavior before reading the implementation, and treat "the spec matches the code" as a finding rather than a pass.

Risk: Multi-agent pipelines cost tokens and time, and a tiered pipeline may be run where a single review would have been sufficient.

Mitigation: Start at the single-agent tier and escalate only when the change size, blast radius, or risk justifies it.

Risk: Review guidance and framework behaviors change over time, so stored review checks may drift from current framework behavior.

Mitigation: Confirm framework-specific checks against current documentation before relying on them.

## Reference(s):

- [Three-Agent Pipeline](artifact/references/three-agent-pipeline.md)
- [Five-Agent Pipeline](artifact/references/five-agent-pipeline.md)
- [Review Checklists](artifact/references/review-checklists.md)
- [Rails Turbo and Controller Traps](artifact/references/rails-turbo-and-controller-traps.md)
- [Rails System Spec Review](artifact/references/rails-system-spec-review.md)
- [Rails Money and State Checks](artifact/references/rails-money-and-state-checks.md)
- [Rails Review Checks](artifact/references/rails-review-checks.md)
- [ClawHub skill page](https://clawhub.ai/djc00p/skills/adversarial-review-pipeline)

## Skill Output:

**Output Type(s):** [guidance, markdown, review findings]

**Output Format:** [Markdown guidance with severity-graded findings, pipeline prompts, and review checklists]

**Output Parameters:** [1D]

**Other Properties Related to Output:** [Findings are graded by severity with a clear verdict; review scope and anything deliberately skipped are stated alongside the findings.]

## Skill Version(s):

1.0.0 (source: server release evidence)

## Ethical Considerations:

Users should evaluate whether this skill is appropriate for their environment, review any generated or modified files before relying on them, and apply their organization's safety, security, and compliance requirements before deployment.
