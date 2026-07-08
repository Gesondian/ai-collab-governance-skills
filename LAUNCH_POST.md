# Launch Post Draft

AI coding agents do not only fail by writing bad code.

They also fail by moving too fast through delivery judgment:

- weak evidence becomes `accepted`
- route reachability becomes workflow acceptance
- mock data becomes business correctness
- a user reopen becomes an immediate patch
- a shared import becomes shared-owner blame

I built **AI Collaboration Governance Skills** as a small skill pack for that gap.

It contains four skills:

- `uat-reopen-intake`: handle reopened or disputed acceptance before repair
- `evidence-boundary`: state what evidence can and cannot prove
- `acceptance-scope-control`: keep `accepted`, `passed`, `closed`, `ready`, and `done` scoped to verified dimensions
- `owner-boundary-triage`: assign owners only when reproduction breadth and mechanism attribution support it

The pack also includes lightweight templates for:

- `failed_gate_min`
- `accepted_scope_recheck`
- `intake_decision`
- `trial_observation`

The goal is not to create a heavy project-management framework.

The goal is to help agents pause before the most expensive mistakes:

```text
fix before intake
accept before evidence
route before mechanism
harden rules before repeated proof
```

v0.1 is intentionally small. It includes synthetic examples and has passed an initial three-scenario forward test:

- UAT reopen after prior acceptance
- mock data overclaiming acceptance
- shared table owner-boundary dispute

If you are using AI agents in enterprise software delivery, QA, UAT, or workflow-heavy product development, I would be interested in feedback on whether these skills match the failure modes you see.

Suggested post title:

```text
AI agents need governance skills, not just coding skills
```

Short version:

```text
I published a small skill pack for AI-assisted software delivery:

AI Collaboration Governance Skills helps agents avoid accepting weak evidence, fixing before UAT intake, and assigning owners without mechanism proof.

It focuses on UAT reopen intake, evidence boundaries, acceptance scope control, and owner-boundary triage.
```
