# Validation Report

## Validation Date

2024-01-15

## Validation Summary

Static end-to-end validation completed successfully for the baseline framework
and ambiguity-remediation rules.

## File Path Validation

All expected files exist:

- agents/: 6 files
- standards/: 5 files
- methodologies/: 5 files
- templates/: 8 files
- frameworks/: 7 files
- docs/: 9 files
- examples/: 3 profiles

## Reference Validation

### Framework References

All framework references in the registry point to existing files:

- frameworks/owasp-asvs.md ✓
- frameworks/owasp-masvs.md ✓
- frameworks/owasp-top10.md ✓
- frameworks/nist-csf.md ✓
- frameworks/cis-controls.md ✓
- frameworks/lgpd.md ✓

### Agent References

All agent references are consistent:

- _lead-auditor.md ✓
- security-auditor.md ✓
- monitoring-auditor.md ✓
- operations-auditor.md ✓
- compliance-auditor.md ✓
- observability-auditor.md ✓

## Terminology Validation

### Status Values

Status values are consistent across all files:

- CONFIRMED ✓
- POTENTIAL ✓
- NOT_TESTED ✓
- NOT_APPLICABLE ✓
- FALSE_POSITIVE ✓

### Severity Values

Severity values are consistent across all files:

- Critical ✓
- High ✓
- Medium ✓
- Low ✓
- Informational ✓

### Maturity Levels

Maturity levels are consistent across all files:

- Initial ✓
- Basic ✓
- Intermediate ✓
- Advanced ✓
- Optimized ✓

## Audit Mode Validation

Audit modes are consistent in Lead Auditor:

- discovery ✓
- security ✓
- monitoring ✓
- operations ✓
- compliance ✓
- observability ✓
- full ✓

Missing and ambiguous mode behavior:

- repository path only: discovery and applicability, then stop ✓
- invalid or ambiguous mode: explain and request selection ✓
- `full` requires explicit user selection ✓
- audit mode is distinct from report artifact type ✓

## Applicability and Phase-Gate Validation

- `APPLICABLE` executes the assigned auditor ✓
- `PARTIALLY_APPLICABLE` executes only the applicable scope ✓
- `NOT_APPLICABLE` is skipped with rationale ✓
- `UNKNOWN` is not executed automatically ✓
- domain-to-auditor ownership is explicit ✓
- `audit-plan.md` is required before specialized execution ✓
- `session-manifest.md` is updated at session start and phase boundaries ✓

## Vocabulary Validation

- finding statuses and evidence classifications are separate ✓
- `NOT_EVIDENCED` and `NOT_ASSESSED` are not finding statuses ✓
- future improvements remain outside findings without evidence ✓
- maturity is limited to selected and executed domains ✓

## Regression Case Coverage

The provider-independent regression matrix is documented in
`docs/ambiguity-regression-cases.md`.

- Static contract coverage: complete ✓
- Live LLM execution: not run in this validation environment
- Live results MUST NOT be marked as passed without an actual model response
  and artifact review.

## Framework Selection Validation

Framework selection rules are consistent:

- Registry is single source of truth ✓
- Frameworks are references only ✓
- Evidence comes from repository ✓
- No forced mappings ✓

## Conclusion

All validations passed. The framework is ready for use.
