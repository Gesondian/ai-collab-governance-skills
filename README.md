# AI Collaboration Governance Skills

Hermes Loop Engineering for self-improving AI delivery governance.

AI coding agents do not only fail by writing bad code. They also fail by:

- accepting weak evidence,
- fixing before UAT intake,
- routing owners too early,
- turning one failure into a heavy rule,
- repeating the same delivery mistake in the next task.

This repo provides lightweight agent skills, templates, and examples that help AI teams turn delivery failures into reusable governance improvements.

The loop:

```text
failure
-> intake
-> evidence boundary
-> scoped failed gate
-> trial observation
-> skill / template refinement
-> forward-test
-> keep / revise / promote / drop
```

Self-improvement here does not mean automatic model training. It means later agents make better delivery decisions because earlier failures were captured, bounded, tested, and converted into human-reviewed skills or templates.

## What This Helps Prevent

| Risk | Skill |
| --- | --- |
| A user reopens an accepted result and the agent immediately patches or re-accepts. | `uat-reopen-intake` |
| Mock, inherited, visual, or partial evidence gets reported as workflow acceptance. | `evidence-boundary` |
| `accepted`, `passed`, `closed`, `ready`, or `done` wording exceeds the verified scope. | `acceptance-scope-control` |
| A shared owner is assigned from source location or imports instead of reproduction breadth and mechanism evidence. | `owner-boundary-triage` |
| A repeated failure becomes either noise or a heavy rule without observation and testing. | `hermes-loop-engineering` |

## Quick Example

```text
User: This was marked accepted, but reload loses my approval comment. Fix it and send accepted again.

Bad agent behavior:
-> patch immediately
-> say accepted again
-> assign owner without a scoped failing gate

With these skills:
-> re-check what the prior receipt actually covered
-> identify the smallest failed gate or missing evidence
-> decide the next owner only after the boundary is clear
-> record whether this is a one-off, repeated pattern, or candidate improvement
-> revise skill/template wording only after observation and forward-test support it
```

## v0.1 Scope Verdict

v0.1 的最小范围是合理的，但必须保持为一个小型治理闭环，而不是方法论库。它只覆盖四个高风险判断：

1. UAT 或验收被打回后，是否允许重新进入处理。
2. 当前证据能支撑什么结论，不能支撑什么结论。
3. `accepted`、`passed`、`closed` 等结论是否超出了实际覆盖范围。
4. 问题应该回到哪个 owner，而不是由当前 AI 直接修复或扩展验收。
5. 失败是否值得沉淀为可复用治理改进，还是只应保持为 observation。

## Non-Goals

- 不包含完整项目管理框架。
- 不包含发布、CI、远端仓库、issue board 或 PR 自动化。
- 不替代人工最终验收。
- 不承诺仅凭单次检查即可关闭整类问题。
- 不自动训练模型；自改进发生在 human-reviewed skills, templates, examples, and forward tests.
- 不收录 actual organization, tenant, person, path, receipt identifier, private logs, or source-project rules.

## Repository Map

```text
README.md
LICENSE
HERMES_LOOP.md
skills/
  hermes-loop-engineering/SKILL.md
  uat-reopen-intake/SKILL.md
  evidence-boundary/SKILL.md
  acceptance-scope-control/SKILL.md
  owner-boundary-triage/SKILL.md
templates/
  hermes_loop_review.md
  failed_gate_min.md
  accepted_scope_recheck.md
  intake_decision.md
  trial_observation.md
examples/
  uat-reopen-enterprise-form.md
  business-table-owner-boundary.md
  mock-data-acceptance-gap.md
```

## Skills

| Skill | Use When | Output |
| --- | --- | --- |
| `uat-reopen-intake` | A previously accepted UAT or acceptance result is challenged. | Intake decision with `failed_gate_min` and `next_owner_decision`. |
| `evidence-boundary` | A conclusion depends on partial, indirect, mock, or inherited evidence. | Evidence scope, unsupported claims, and missing proof. |
| `acceptance-scope-control` | An AI is about to say `accepted`, `passed`, or `closed`. | Scope-limited receipt and uncovered dimensions. |
| `owner-boundary-triage` | Ownership is ambiguous between feature owner, shared capability owner, data owner, or verifier. | Owner verdict based on reproduction breadth and mechanism attribution. |
| `hermes-loop-engineering` | Repeated failures or trial observations may need reusable governance improvement. | Keep / revise / promote / drop decision for a candidate improvement. |

## Templates

- `failed_gate_min.md`: capture the smallest failing gate that must be resolved before owner assignment or acceptance closure.
- `accepted_scope_recheck.md`: re-check what the original accepted receipt actually covered.
- `intake_decision.md`: decide whether to reopen, reroute, request evidence, or reject a reopen.
- `trial_observation.md`: record lightweight field observations before hardening a governance rule.
- `hermes_loop_review.md`: decide whether an observed failure should become wording, template, example, forward-test, hard-gate candidate, or be dropped.

## Hermes Loop Engineering

Hermes Loop Engineering is the self-improvement layer in this repo. It connects delivery failures to durable governance improvements without pretending that every failure deserves a new rule.

Read [HERMES_LOOP.md](HERMES_LOOP.md) for the full loop.

Minimum loop:

```text
1. Capture the disputed outcome.
2. Re-check what the evidence actually proved.
3. Identify the smallest failed gate or missing evidence.
4. Record a trial observation.
5. Decide whether the pattern is one-off, repeated, or systemic.
6. Revise wording, template, example, or skill only when evidence supports it.
7. Forward-test the candidate change.
8. Keep, revise, promote, or drop it.
```

The loop counts as improved only when a later agent or later delivery decision behaves better because of the updated artifact. A document edit alone is not self-improvement.

Minimum proof:

- the old failure or bad conclusion is visible,
- the updated skill, template, or example changes the next decision,
- the change does not create excessive false positives or handoff burden,
- there is a rollback condition if the candidate proves noisy.

## Quickstart

1. Select the skill that matches the immediate risk.
2. Fill the matching template before changing implementation.
3. Keep the verdict narrower than the evidence.
4. Route the smallest failing gate to the next owner.
5. Treat human review as the final acceptance boundary.

Recommended first pass:

```text
User challenges prior acceptance
-> use uat-reopen-intake
-> fill accepted_scope_recheck
-> fill failed_gate_min if a real gap exists
-> record intake_decision
-> send only the bounded verdict
```

## Install / Use

This repository can be used as a reference pack, or individual skill folders can be copied into a local agent skills directory such as:

```text
$CODEX_HOME/skills/
```

For a minimal local install, copy only the skill folder you want to trial:

```text
skills/uat-reopen-intake
skills/evidence-boundary
skills/acceptance-scope-control
skills/owner-boundary-triage
skills/hermes-loop-engineering
```

Keep `templates/` and `examples/` nearby as reference material, not as mandatory control-plane files.

## Anonymization Rules

All examples in this repo are synthetic. They use generic enterprise software nouns such as:

- Enterprise Workflow Form
- Process Page
- Material Attachment
- Business Table

Do not add confidential delivery names, business paths, receipt identifiers, screenshots, logs, revision hashes, version-line labels, private enum vocabularies, or copied rule text from a source delivery.

## v0.1 Release Criteria

- All public files are synthetic and project-neutral.
- Every `SKILL.md` has valid `name` and `description` frontmatter.
- Every example demonstrates a boundary judgment rather than a full project story.
- Local v0.1 does not require a GitHub remote, push, PR, package publication, CI, or external sync.

## v0.1 Validation Status

- Structure check: passed.
- Skill frontmatter check: passed.
- Public artifact anonymization scan: passed.
- Initial forward-test with three independent synthetic pressure scenarios: passed.
- Broader forward-test across more domains and agent runtimes: pending.

## GitHub Release Readiness

Before publishing, run the structure, frontmatter, and anonymization scans again. Do not publish internal work logs, private execution records, source project rules, local paths, screenshots, or real delivery receipts.

## License

MIT.
