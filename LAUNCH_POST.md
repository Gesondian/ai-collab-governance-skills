# Launch Post Draft

AI coding agents need a way to learn from delivery mistakes without turning every mistake into a heavy rule.

I built **AI Collaboration Governance Skills** around **Hermes Loop Engineering**: a human-in-the-loop self-improvement loop for AI-assisted software delivery.

The loop turns repeated delivery failures into reusable governance improvements:

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

The failure modes it targets:

- weak evidence becomes `accepted`
- route reachability becomes workflow acceptance
- mock data becomes business correctness
- a user reopen becomes an immediate patch
- a shared import becomes shared-owner blame
- a repeated mistake becomes either ignored noise or an over-heavy rule

It contains five skills:

- `hermes-loop-engineering`: decide whether a failure becomes observation, wording, template, example, forward-test, hard-gate candidate, or is dropped
- `uat-reopen-intake`: handle reopened or disputed acceptance before repair
- `evidence-boundary`: state what evidence can and cannot prove
- `acceptance-scope-control`: keep `accepted`, `passed`, `closed`, `ready`, and `done` scoped to verified dimensions
- `owner-boundary-triage`: assign owners only when reproduction breadth and mechanism attribution support it

The pack also includes lightweight templates for:

- `hermes_loop_review`
- `failed_gate_min`
- `accepted_scope_recheck`
- `intake_decision`
- `trial_observation`

The goal is not to create a heavy project-management framework.

The goal is to make the collaboration loop improve while staying lightweight: observe first, harden only after repeated proof.

The self-improvement claim is intentionally evidence-based: a document edit is not enough. The loop only counts as improved when a later agent or later delivery decision behaves better under a forward-test or real follow-up case.

v0.1 is intentionally small. It includes synthetic examples and has passed an initial three-scenario forward test:

- UAT reopen after prior acceptance
- mock data overclaiming acceptance
- shared table owner-boundary dispute

If you are using AI agents in enterprise software delivery, QA, UAT, or workflow-heavy product development, I would be interested in feedback on whether these skills match the failure modes you see.

Suggested post title:

```text
AI agents need self-improving governance loops, not just coding skills
```

Short version:

```text
I published a small skill pack for AI-assisted software delivery:

AI Collaboration Governance Skills introduces Hermes Loop Engineering: a human-in-the-loop self-improvement loop that turns delivery failures into reusable governance skills.

It focuses on UAT reopen intake, evidence boundaries, acceptance scope control, owner-boundary triage, and keep/revise/promote/drop decisions for candidate improvements.
```

## X / Twitter Version

```text
AI coding agents need a way to learn from delivery mistakes without turning every mistake into a hard rule.

I published a small skill pack around Hermes Loop Engineering:
a human-in-the-loop self-improvement loop for AI-assisted software delivery.

It helps agents turn failures into reusable governance improvements:

failure -> intake -> evidence boundary -> trial observation -> skill/template refinement -> forward-test -> keep/revise/promote/drop

It focuses on:
- Hermes Loop review
- UAT reopen intake
- evidence boundaries
- acceptance scope control
- owner-boundary triage

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
- A repeated failure becomes either ignored noise or an over-heavy rule

I published a small public skill pack called AI Collaboration Governance Skills, built around Hermes Loop Engineering.

Hermes Loop Engineering is a human-in-the-loop self-improvement loop for AI-assisted software delivery governance:

failure -> intake -> evidence boundary -> scoped failed gate -> trial observation -> skill/template refinement -> forward-test -> keep/revise/promote/drop

It is not automatic model training and it is not a project-management framework. It is a lightweight way to help the collaboration system improve from repeated delivery mistakes.

- `hermes-loop-engineering`: decide whether an observed failure should become wording, a template, an example, a forward-test, a hard-gate candidate, or be dropped
- `uat-reopen-intake`: handle disputed or reopened acceptance before repair
- `evidence-boundary`: state what evidence can and cannot prove
- `acceptance-scope-control`: keep `accepted`, `passed`, `closed`, `ready`, and `done` scoped to verified dimensions
- `owner-boundary-triage`: assign owners only when reproduction breadth and mechanism attribution support it

v0.1 is intentionally small, synthetic, and public.

Feedback welcome, especially from teams using AI agents in QA, UAT, enterprise software delivery, or workflow-heavy products.

https://github.com/Gesondian/ai-collab-governance-skills
```

## Hacker News / Reddit Version

```text
I made a small skill pack for AI-assisted software delivery governance.

The core idea is Hermes Loop Engineering: a human-in-the-loop self-improvement loop for turning repeated delivery failures into reusable governance improvements.

The problem it targets is not only "AI writes bad code". It is the delivery judgment around code:

- accepting weak evidence
- treating mock data as real workflow proof
- fixing immediately when a user reopens acceptance
- assigning shared owners from imports or file paths
- hardening rules before observing repetition and false-positive risk

The repo contains five small skills:

- Hermes Loop Engineering
- UAT reopen intake
- evidence boundary
- acceptance scope control
- owner-boundary triage

Each skill is just Markdown plus lightweight templates and synthetic examples. v0.1 passed a small three-scenario forward test, but broader real-world testing is still needed.

I would be interested in feedback from people using coding agents in real delivery workflows.

Repo: https://github.com/Gesondian/ai-collab-governance-skills
```
