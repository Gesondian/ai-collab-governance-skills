# Hermes Loop Engineering

Hermes Loop Engineering is a human-in-the-loop self-improvement loop for AI-assisted software delivery governance.

It does not train a model automatically. It improves the collaboration system by turning disputed delivery outcomes into reusable judgment, templates, and skill wording after evidence and forward-testing support the change.

## Core Loop

```text
delivery failure or disputed outcome
-> intake
-> evidence boundary
-> smallest failed gate
-> trial observation
-> reusable pattern decision
-> skill / template refinement
-> forward-test
-> keep / revise / promote / drop
```

## What Counts As Self-Improvement

Self-improvement means a later agent has better guidance because an earlier delivery failure was captured, bounded, tested, and converted into a reusable artifact.

Examples:

- A repeated UAT reopen becomes a clearer `uat-reopen-intake` trigger.
- A repeated evidence overclaim becomes stronger acceptance wording.
- A repeated owner-routing mistake becomes an owner-boundary example or template field.
- A candidate rule that causes false positives is revised or dropped.

## How To Prove The Loop Improved

Do not claim self-improvement just because a document changed.

The loop has improved only when there is evidence that a later agent or later delivery decision behaves better because of the updated artifact.

Minimum proof:

1. A prior failure or disputed outcome is captured.
2. The evidence boundary and smallest failed gate are explicit.
3. A skill, template, example, or wording change is made.
4. A forward-test or later real case shows a better decision.
5. The change does not create unacceptable false positives, maintenance cost, or over-governance.

If step 4 is missing, the result is only a candidate improvement.
If step 5 fails, revise or drop the candidate.

## What Does Not Count

- Immediately adding a hard rule after one failure.
- Treating every user complaint as a reusable pattern.
- Updating a skill without observing whether the wording changes agent behavior.
- Claiming a model has learned when only a document was edited.
- Using governance language to hide missing evidence.

## Decision Ladder

| Level | Meaning | Action |
| --- | --- | --- |
| `observation` | A signal was seen, but pattern value is unknown. | Record only. |
| `candidate_pattern` | The signal may generalize beyond one case. | Fill `trial_observation`. |
| `wording_guidance` | Light wording can reduce a repeated mistake. | Revise skill wording. |
| `template_field` | The missing information is repeatedly needed. | Add or revise a template field. |
| `forward_tested_guidance` | A pressure scenario shows the wording changes agent behavior. | Keep and document. |
| `hard_gate_candidate` | Failure is repeated, high-risk, low-false-positive, and cheap to check. | Consider a hard gate. |
| `drop_or_revise` | The candidate is noisy, too broad, or not useful. | Remove or narrow it. |

## Minimum Evidence Before Promotion

Before promoting a candidate beyond wording guidance, capture:

- the original failure signal,
- evidence boundary,
- accepted or receipt scope involved,
- failed gate or missing evidence,
- agent rationalization observed,
- false positive / false negative risk,
- maintenance burden,
- forward-test result.

## Promotion And Rollback

A candidate can be promoted only when it has a clear use scope and a clear non-use scope.

Rollback or revise the candidate when:

- it causes agents to ask for unnecessary evidence,
- it turns local defects into broad owner disputes,
- it makes handoffs longer without improving decisions,
- it is applied outside the scenario that justified it,
- it cannot be explained as a concrete behavior change.

## How This Repository Uses The Loop

The loop connects existing artifacts:

- `uat-reopen-intake`: captures reopened or disputed acceptance.
- `evidence-boundary`: limits what evidence can prove.
- `acceptance-scope-control`: keeps completion wording scoped.
- `owner-boundary-triage`: prevents premature owner assignment.
- `trial_observation`: records whether a candidate rule is worth hardening.
- `hermes_loop_review`: decides whether to keep, revise, promote, or drop a candidate improvement.

## Safety Rule

The loop should make future agents more accurate, not heavier.

When in doubt, prefer:

```text
observation -> wording guidance -> forward-test
```

over:

```text
single failure -> new hard gate
```
