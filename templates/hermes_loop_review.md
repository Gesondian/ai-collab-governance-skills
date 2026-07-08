# hermes_loop_review

Use this template to decide whether a delivery failure should become a reusable governance improvement.

```md
case:
review_owner:
date_label:

failure_signal:
source_context:
evidence_boundary_ref:
accepted_scope_ref:
failed_gate_ref:
trial_observation_ref:

candidate_pattern:
why_it_may_repeat:
why_it_may_be_one_off:
agent_rationalization_seen:
existing_artifact_gap:

reuse_scope:
not_reuse_scope:
false_positive_risk:
false_negative_risk:
maintenance_cost:
over_governance_risk:

recommended_change:
target_artifact:
change_size:
forward_test_needed:
forward_test_scenario:
forward_test_result:
behavior_change_evidence:
rollback_condition:

decision:
next_owner:
unblock_condition:
must_not_claim:
remaining_risks:
```

Allowed `decision` values:

- `record_observation`
- `revise_wording`
- `revise_template`
- `add_example`
- `forward_test_candidate`
- `promote_to_hard_gate_candidate`
- `drop_candidate`
