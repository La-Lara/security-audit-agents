# Finding Model

This file defines the canonical finding structure and boundaries for all audit
agents.

A finding is an evidence-supported audit record describing an issue, gap, risk,
or weakness within the assigned audit scope. Findings must be distinct from
general recommendations, future improvements, framework checklist items, and
areas that were not applicable or not assessed.

## Identifier

Each specialized auditor uses its domain prefix followed by a three-digit
sequence number.

Allowed prefixes:

- `SEC-XXX` for Security findings;
- `MON-XXX` for Monitoring findings;
- `OPS-XXX` for Operations findings;
- `COMP-XXX` for Compliance findings;
- `OBS-XXX` for Observability findings.

Examples:

- `SEC-001`
- `MON-001`
- `OPS-001`
- `COMP-001`
- `OBS-001`

The Lead Auditor may preserve source identifiers during consolidation and may
deduplicate equivalent findings, but must not change their meaning.

## Required Fields

Every finding must include:

- identifier;
- title or description;
- evidence;
- risk or impact;
- severity;
- status;
- recommendation;
- validation suggestions.

Use `Risk` for security, monitoring, operations, and compliance findings. Use
`Impact` when an agent's domain language is impact-oriented, such as
observability. Compliance findings may include a `Compliance Reference` when a
Lead-selected framework supports it.

## Optional Fields

Include these fields only when applicable:

- evidence classification;
- framework mapping;
- affected component;
- assumptions or limitations;
- related findings;
- owner or remediation phase when a template requests it.

Framework mappings must come from Lead-selected frameworks and must not be
forced.

## Finding Boundaries

Create a finding only when repository evidence supports it.

Do not create a finding for:

- hypothetical vulnerabilities;
- absent technologies that are out of scope;
- generic best practices with no repository-specific evidence;
- unselected framework controls;
- future improvements with no current evidence-supported issue;
- legal conclusions or legal violations.

When a concern is plausible but incomplete, use `POTENTIAL` status and explain
what validation is needed. When the area is relevant but not evaluable, record
it outside confirmed findings with `NOT_TESTED` status and the appropriate
evidence classification, such as `NOT_EVIDENCED` or `NOT_ASSESSED`.

## Consolidation Rules

The Lead Auditor should:

- merge duplicate findings without losing evidence;
- preserve domain context;
- separate confirmed findings from potential findings;
- keep recommendations and future improvements separate from findings;
- retain status, severity, evidence, and validation suggestions.

## Validation Rules

- Confirm every finding has all required fields.
- Confirm identifiers match the assigned auditor prefix.
- Confirm every finding has evidence and a valid status and severity.
- Confirm recommendations are actionable but do not claim validation occurred.
- Confirm findings do not assert facts beyond the cited evidence.
