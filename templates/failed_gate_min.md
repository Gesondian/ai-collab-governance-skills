# failed_gate_min

Use this template to capture the smallest failing gate that must be resolved before owner assignment or acceptance closure.

```md
case:
reported_by:
date_label:

verdict:
failure_summary:
smallest_repro_scope:
route_or_entry:
surface:
viewport_or_environment:
data_shape:
role_or_permission:

expected_signal:
actual_signal:
evidence_refs:
checks_run:
missing_evidence:
scope_boundary:

failure_type:
candidate_owner:
owner_confidence:
return_gate:
return_owner_on_fail:
next_owner:
unblock_condition:

must_not_claim:
remaining_risks:
```

Allowed `verdict` values:

- `failed_gate_min_identified`
- `needs_smaller_repro`
- `needs_evidence`
- `owner_boundary_unclear`
