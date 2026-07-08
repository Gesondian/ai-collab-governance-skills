# intake_decision

Use this template to record the decision made after UAT reopen intake.

```md
case:
intake_owner:
date_label:

user_challenge:
accepted_scope_recheck_ref:
failed_gate_min_ref:

decision:
failure_type:
evidence_basis:
unsupported_claims:
missing_evidence:

next_owner:
owner_reason:
return_gate:
return_owner_on_fail:
unblock_condition:
human_review_needed:

response_to_user:
remaining_risks:
```

Allowed `decision` values:

- `reopen_required`
- `needs_failed_gate_min`
- `needs_evidence`
- `reroute_owner`
- `no_reopen_from_current_evidence`
