# Maturity Model

This file defines the canonical maturity levels for audit domain assessments.

Maturity describes the observed development of a capability within repository
evidence and audit artifacts. It is not a certification, compliance conclusion,
or organization-wide rating.

## Allowed Levels

### Initial

Capability is absent, ad hoc, inconsistent, or not evidenced enough to show a
repeatable practice.

Use when:

- no direct evidence was identified;
- activity appears manual or undocumented;
- coverage is isolated or accidental;
- practices cannot be repeated from repository artifacts.

### Basic

Capability exists in a limited or simple form.

Use when:

- some direct evidence exists;
- implementation is narrow or partially documented;
- practices depend on manual effort;
- gaps remain in coverage, consistency, or ownership.

### Intermediate

Capability is defined and reasonably consistent for important in-scope areas.

Use when:

- implementation and documentation both have supporting evidence;
- common workflows are covered;
- gaps are identifiable but not foundational;
- practices appear repeatable from repository artifacts.

### Advanced

Capability is mature, broad, and well integrated into repository workflows.

Use when:

- controls or practices cover most in-scope areas;
- automation, documentation, and operational use are evident;
- exceptions are limited and explainable;
- evidence supports active maintenance.

### Optimized

Capability is continuously improved, measured, and strongly integrated.

Use when:

- metrics, feedback loops, or review mechanisms are evidenced;
- automation and documentation are comprehensive;
- improvement over time is visible in repository artifacts;
- the capability is resilient to routine change.

## Usage Rules

- Do not introduce additional maturity levels.
- Level names must use the capitalization listed above.
- Every maturity assessment must include justification.
- Maturity must be assessed per applicable domain or capability, not inferred
  globally from a single artifact.
- Absence of repository evidence should be described as an evidence limitation.
- Do not claim organization-wide maturity beyond the audited scope.

## Domain Usage

The maturity model applies to the domains selected by the Lead Auditor, such as:

- Security;
- Monitoring;
- Operations;
- Compliance;
- Observability.

Specialized auditors may assess domain-specific capabilities within those
domains, including authentication, alerting, recovery, privacy controls,
logging, metrics, tracing, documentation, or other applicable areas.

## Validation Rules

- Confirm every maturity level is one of the allowed levels.
- Confirm every maturity rating has repository-backed justification.
- Confirm non-applicable domains are excluded or marked with rationale.
- Confirm maturity language does not imply certification or legal compliance.
