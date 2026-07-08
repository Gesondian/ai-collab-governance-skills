# accepted_scope_recheck

Use this template before reopening or expanding a previously accepted result.

```md
case:
prior_receipt:
recheck_reason:

prior_verdict:
prior_covered_routes:
prior_covered_surfaces:
prior_covered_viewports:
prior_covered_data:
prior_assertions:
prior_fact_sources:
prior_skipped_checks:
prior_receipt_identity:

new_challenge:
challenge_within_prior_scope:
challenge_outside_prior_scope:
stale_or_inherited_evidence:
missing_evidence:
checks_run:

safe_current_verdict:
must_not_claim:
next_owner_decision:
return_owner_on_fail:
remaining_risks:
```

Allowed `safe_current_verdict` values:

- `reopen_required`
- `needs_failed_gate_min`
- `needs_evidence`
- `no_reopen_from_current_evidence`
- `reroute_owner`
