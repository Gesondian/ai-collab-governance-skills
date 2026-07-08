# Example: Business Table Owner Boundary

This is a synthetic example. It is not adapted from confidential delivery material.

## Scenario

A Business Table appears on two Process Pages. On Page A, the row action opens the wrong drawer. Page B uses the same shared table package and works correctly.

## Incorrect Handling

```md
verdict: shared_capability_owner
reason: The failing code imports a shared table package.
```

Why this is wrong:

- A shared import is not proof of shared mechanism failure.
- Negative reproduction on Page B narrows the likely owner.
- The failure may be in Page A composition, action mapping, or data binding.

## Correct Triage

```md
verdict: feature_owner
failure_summary: Row action opens the wrong drawer on Page A.
reproduction_breadth:
  reproduces: Page A Business Table row action
  does_not_reproduce: Page B Business Table row action
mechanism_attribution: route-specific action mapping is the current best explanation
excluded_owners:
  shared_capability_owner: not supported because another consumer works
  data_owner: not supported without data-shape evidence
missing_checks:
  - confirm Page A action mapping
  - compare one representative row shape between Page A and Page B
next_owner: Page A feature owner
return_gate: row action on Page A opens the expected drawer with stated data shape
return_owner_on_fail: Page A feature owner
```

## Boundary Lesson

Owner assignment needs reproduction breadth plus mechanism attribution. Source location alone is not enough.
