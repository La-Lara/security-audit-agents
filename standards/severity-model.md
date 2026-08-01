# Severity Model

This file defines the canonical severity values for security, monitoring,
operations, compliance, and observability findings.

Severity describes the likely impact of an evidence-supported condition within
the audited repository scope. It is not a confidence score, priority score, or
proof that exploitation or outage has occurred.

## Allowed Values

### Critical

Use when evidence indicates a severe risk to confidentiality, integrity,
availability, privacy, operational continuity, or diagnostic capability.

Typical indicators:

- severe compromise may be possible;
- critical service operation may be materially impaired;
- sensitive data protection may be significantly weakened;
- recovery, detection, or diagnosis for critical behavior may be absent.

### High

Use when evidence indicates a material risk that could cause significant
security, compliance, operational, monitoring, or observability impact.

Typical indicators:

- important controls are missing or materially incomplete;
- exposed attack paths, operational gaps, or privacy weaknesses are plausible;
- incidents or failures may be difficult to detect, diagnose, or recover from.

### Medium

Use when evidence indicates a meaningful but bounded risk.

Typical indicators:

- controls exist but are incomplete;
- impact is limited by scope, architecture, or compensating evidence;
- remediation is important but not urgent enough for High or Critical.

### Low

Use when evidence indicates a minor risk, localized weakness, or limited
operational impact.

Typical indicators:

- issue affects a narrow component or non-critical workflow;
- exposure is limited;
- improvement would reduce risk but does not materially change posture alone.

### Informational

Use for observations, maturity improvements, or documentation improvements
where no meaningful risk is identified.

Typical indicators:

- no direct vulnerability or control failure is evidenced;
- recommendation is useful but optional;
- item belongs in future improvements rather than confirmed findings when no
  issue exists.

## Usage Rules

- Do not introduce additional severity values.
- Severity values must use the capitalization listed above.
- Every `CONFIRMED` and `POTENTIAL` finding must have exactly one severity.
- Severity must be justified by repository evidence and scoped impact.
- Do not escalate severity because a framework mentions a control; the
  repository evidence must support the impact.
- When evidence is incomplete, prefer `POTENTIAL` status and explain confidence
  separately instead of inflating severity.

## Validation Rules

- Confirm every finding severity is one of the allowed values.
- Confirm the stated impact matches the selected severity.
- Confirm Informational items do not claim material risk.
- Confirm Critical and High findings cite strong evidence and affected scope.
