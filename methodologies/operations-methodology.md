# Operations Methodology

This file defines the audit process for the Operations Auditor. It provides
phase-level guidance without duplicating agent responsibilities, domain lists,
or finding structures.

## Purpose

Guide the Operations Auditor through a repeatable, evidence-based process for
evaluating operational readiness, maintainability, resilience, and
recoverability within repository scope.

## Inputs

Read before starting:

- `discovery.md` from the audit workspace;
- `applicability.md` from the audit workspace;
- selected framework list supplied by the Lead Auditor.

Use `discovery.md` as the authoritative source for architecture and technologies.
Use `applicability.md` as the authoritative source for scope boundaries.

## Process Phases

### Phase 1 - Scope Confirmation

Confirm which operational domains apply based on `applicability.md`. Mark
non-applicable domains as `NOT_APPLICABLE` with scope justification. Do not
audit absent components.

### Phase 2 - Evidence Collection

For each applicable domain, collect repository evidence:

- source code;
- configuration files;
- deployment files;
- infrastructure as code;
- CI/CD definitions;
- documentation;
- runbooks;
- architecture documents.

If evidence cannot be identified, record a non-finding assessment with
`NOT_TESTED` status and `NOT_EVIDENCED` evidence classification, or use
`NOT_ASSESSED` when the area could not be assessed. Do not create findings
without evidence.

### Phase 3 - Framework Consultation

Consult only Lead-selected framework references. Map evidence to framework
controls where natural alignment exists. Do not force mappings. Frameworks are
references, not evidence sources.

### Phase 4 - Finding Generation

For each evidence-supported issue, generate a finding using the canonical
finding model. Assign identifier, title, description, evidence, risk, severity,
status, recommendation, and validation suggestions. Use allowed status and
severity values only.

### Phase 5 - Maturity Assessment

Assess maturity per operational domain using the canonical maturity model
levels: Initial, Basic, Intermediate, Advanced, Optimized. Every rating must
include repository-backed justification.

### Phase 6 - Operational Recommendations

Document recommended improvements not supported by current evidence as
recommendations. Keep this section separate from findings.

## Evidence Handling

- Evidence must come from repository artifacts or audit workspace artifacts.
- Use evidence classifications: EVIDENCED, PARTIALLY_EVIDENCED, NOT_EVIDENCED,
  NOT_APPLICABLE, NOT_ASSESSED.
- Use careful evidence language: "The repository contains...", "No evidence was
  identified for...", "The available evidence suggests...".
- Absence of evidence is not evidence of absence.
- Do not claim validation occurred unless tests were actually executed.

## Output

Generate `operations.md` inside the audit workspace following the structure
defined in the Operations Auditor agent file.

## Boundaries

This methodology does not:

- define operational domains (see Operations Auditor agent);
- define finding structure (see finding-model.md);
- define severity criteria (see severity-model.md);
- define status values (see status-model.md);
- define evidence rules (see evidence-model.md);
- define maturity levels (see maturity-model.md).
