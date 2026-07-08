# Example: UAT Reopen for Enterprise Workflow Form

This is a synthetic example. It is not adapted from confidential delivery material.

## Scenario

An Enterprise Workflow Form was previously reported as `accepted_scope_limited` for desktop viewport, synthetic draft data, and the submit-button visibility assertion. A reviewer later says the acceptance should be reopened because the approval comment field is empty after reload.

## Incorrect Handling

```md
verdict: accepted
reason: The form was already accepted, and the route still loads.
```

Why this is wrong:

- Route reachability does not prove reload persistence.
- The prior receipt covered submit-button visibility, not comment persistence.
- The new challenge needs a smaller failing gate before owner assignment.

## Correct Intake

```md
verdict: needs_failed_gate_min
accepted_scope_recheck:
  prior_covered_routes: Enterprise Workflow Form
  prior_covered_surfaces: submit action area
  prior_covered_viewports: desktop
  prior_covered_data: synthetic draft record
  prior_assertions: submit button visible and enabled
  prior_fact_sources: local browser observation
  prior_skipped_checks: reload persistence, approval comment save, role variants
failed_gate_min_candidate:
  surface: approval comment field
  expected_signal: saved comment remains visible after reload
  actual_signal: not yet reproduced in a bounded check
failure_type: missing_evidence
missing_evidence: reload check with one saved comment and stated data shape
next_owner_decision: verifier_owner until the smallest failing gate is captured
return_owner_on_fail: verifier_owner
must_not_claim: accepted, closed, form workflow works end to end
```

## Boundary Lesson

A reopened UAT item starts with intake. The AI may not patch, re-accept, or assign runtime ownership until the failed gate is small enough to verify.
