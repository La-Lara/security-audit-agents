# Status Model

This file defines the canonical finding status values for all audit agents.
Use only these values when classifying findings or finding-like audit records.

## Allowed Values

### CONFIRMED

Use when repository evidence directly supports the issue, gap, or control
weakness described by the finding.

Requirements:

- cite concrete repository evidence;
- describe the observed condition;
- avoid claims that require unperformed testing or external confirmation.

### POTENTIAL

Use when repository evidence suggests a plausible issue, but the available
evidence is incomplete or indirect.

Requirements:

- cite the evidence that created the concern;
- state what is unknown;
- include validation suggestions;
- do not present the issue as proven.

### NOT_TESTED

Use when a check or control is relevant but cannot be evaluated from the
available repository evidence.

Requirements:

- explain why testing or verification was not possible;
- identify evidence that would be needed;
- do not infer pass or fail.

### NOT_APPLICABLE

Use when the audited component, capability, technology, data flow, or control
does not apply to the repository scope.

Requirements:

- explain the scope reason;
- cite evidence or absence indicators when available;
- do not create a risk finding solely for a non-applicable area.

### FALSE_POSITIVE

Use when an initially suspected issue is contradicted by stronger repository
evidence.

Requirements:

- describe the original suspicion;
- cite the evidence that disproves or neutralizes it;
- keep the record separate from confirmed findings.

## Usage Rules

- Do not introduce additional status values.
- Status values must be uppercase exactly as listed.
- Every finding must have exactly one status.
- Findings with `CONFIRMED` or `POTENTIAL` status must include evidence.
- `NOT_TESTED`, `NOT_APPLICABLE`, and `FALSE_POSITIVE` records must include a
  concise rationale.
- Recommendations and future improvements are not findings unless they describe
  an evidence-supported issue.

## Validation Rules

- Search agent outputs for status values outside the allowed list.
- Confirm every status has supporting evidence or rationale.
- Confirm `POTENTIAL` findings are not worded as confirmed failures.
- Confirm `NOT_APPLICABLE` records explain why the area is out of scope.
