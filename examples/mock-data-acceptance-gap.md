# Example: Mock Data Acceptance Gap

This is a synthetic example. It is not adapted from confidential delivery material.

## Scenario

A Material Attachment panel renders correctly with mock data in a local preview. The AI is about to report that attachment handling is accepted for the Process Page.

## Incorrect Handling

```md
verdict: accepted
reason: The Material Attachment panel renders with mock data.
```

Why this is wrong:

- Mock render does not prove upload, download, permission, lifecycle, or persistence behavior.
- The Process Page may use different data than the local preview.
- Rendering a panel is not the same assertion level as attachment handling.

## Correct Evidence Boundary

```md
claim: Material Attachment handling is accepted on the Process Page.
evidence_refs:
  - local preview with mock attachment list
covered_scope:
  surface: Material Attachment panel
  data: synthetic attachment rows
  assertion: panel renders row names and counts
unsupported_scope:
  - upload
  - download
  - deletion
  - permission behavior
  - persistence after reload
  - real Process Page data schema
missing_evidence:
  - Process Page check using its real data source or a documented schema fixture
  - permission-specific attachment action assertions
safe_wording: Mock evidence supports panel rendering only; it does not support attachment handling acceptance.
must_not_claim: accepted, attachment workflow works, real data schema verified
```

## Boundary Lesson

Mock evidence can support render capability, not business acceptance. Keep the receipt at the assertion level actually tested.
