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

## X / Twitter Version

```text
AI coding agents do not only fail by writing bad code.

They also fail by moving too fast through delivery judgment:

- weak evidence -> accepted
- mock data -> workflow accepted
- user reopen -> immediate patch
- shared import -> shared-owner blame

I published a small skill pack for this gap:
AI Collaboration Governance Skills

It focuses on:
- UAT reopen intake
- evidence boundaries
- acceptance scope control
- owner-boundary triage

The goal is simple:
help agents pause before they fix, accept, route, or harden rules.

Repo:
https://github.com/Gesondian/ai-collab-governance-skills
```

## LinkedIn Version

```text
AI coding agents are getting better at implementation, but many delivery failures happen before or after the code change.

The repeated pattern I see:

- A partial check becomes `accepted`
- A route loading becomes workflow acceptance
- Mock data becomes real business confidence
- A user reopening acceptance becomes an immediate patch
- A shared import becomes shared-owner blame

I published a small public skill pack called AI Collaboration Governance Skills.

It is not a project-management framework. It is a set of lightweight agent skills for the judgment points around AI-assisted software delivery:

- `uat-reopen-intake`: handle disputed or reopened acceptance before repair
- `evidence-boundary`: state what evidence can and cannot prove
- `acceptance-scope-control`: keep `accepted`, `passed`, `closed`, `ready`, and `done` scoped to verified dimensions
- `owner-boundary-triage`: assign owners only when reproduction breadth and mechanism attribution support it

The goal is to help AI agents pause before the expensive mistakes:

fix before intake
accept before evidence
route before mechanism
harden rules before repeated proof

v0.1 is intentionally small, synthetic, and public.

Feedback welcome, especially from teams using AI agents in QA, UAT, enterprise software delivery, or workflow-heavy products.

https://github.com/Gesondian/ai-collab-governance-skills
```

## Hacker News / Reddit Version

```text
I made a small skill pack for AI-assisted software delivery governance.

The problem it targets is not "AI writes bad code". It is the delivery judgment around code:

- accepting weak evidence
- treating mock data as real workflow proof
- fixing immediately when a user reopens acceptance
- assigning shared owners from imports or file paths

The repo contains four small skills:

- UAT reopen intake
- evidence boundary
- acceptance scope control
- owner-boundary triage

Each skill is just Markdown plus lightweight templates and synthetic examples. v0.1 passed a small three-scenario forward test, but broader real-world testing is still needed.

I would be interested in feedback from people using coding agents in real delivery workflows.

Repo: https://github.com/Gesondian/ai-collab-governance-skills
```
