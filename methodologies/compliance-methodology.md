# Compliance Methodology

This file defines the audit process for the Compliance Auditor. It provides
phase-level guidance without duplicating agent responsibilities, domain lists,
or finding structures.

## Purpose

Guide the Compliance Auditor through a repeatable, evidence-based process for
evaluating technical compliance, privacy controls, and regulatory-related
evidence within repository scope.

## Inputs

Read before starting:

- `discovery.md` from the audit workspace;
- `applicability.md` from the audit workspace;
- selected framework list supplied by the Lead Auditor.

Use `discovery.md` as the authoritative source for architecture and technologies.
Use `applicability.md` as the authoritative source for scope boundaries.

## Process Phases

### Phase 1 - Scope Confirmation

Confirm which compliance domains apply based on `applicability.md`. Mark
non-applicable domains as `NOT_APPLICABLE` with scope justification. Do not
audit absent components.

### Phase 2 - Evidence Collection

For each applicable domain, collect repository evidence:

- source code;
- database models;
- storage mechanisms;
- APIs;
- authentication flows;
- authorization controls;
- configuration files;
- documentation;
- privacy-related documentation.

If evidence cannot be identified, record `NOT_EVIDENCED` or `NOT_TESTED` and
move to the next domain. Do not create findings without evidence.

### Phase 3 - Framework Consultation

Consult only Lead-selected framework references. Map evidence to framework
controls where natural alignment exists. Do not force mappings. Frameworks are
references, not evidence sources.

### Phase 4 - Finding Generation

For each evidence-supported issue, generate a finding using the canonical
finding model. Assign identifier, title, description, evidence, risk, severity,
status, recommendation, and validation suggestions. Use allowed status and
severity values only. Include compliance reference when applicable.

### Phase 5 - Maturity Assessment

Assess maturity per compliance domain using the canonical maturity model levels:
Initial, Basic, Intermediate, Advanced, Optimized. Every rating must include
repository-backed justification.

### Phase 6 - Future Improvements

Document optional improvements not supported by current evidence as findings.
Keep this section separate from confirmed and potential findings.

## Evidence Handling

- Evidence must come from repository artifacts or audit workspace artifacts.
- Use evidence classifications: EVIDENCED, PARTIALLY_EVIDENCED, NOT_EVIDENCED,
  NOT_APPLICABLE, NOT_ASSESSED.
- Use careful evidence language: "The repository contains...", "No evidence was
  identified for...", "The available evidence suggests...".
- Do not claim validation occurred unless tests were actually executed.

## Legal Boundary

This methodology operates within technical boundaries only:

- Identify technical gaps and map to legal articles when applicable.
- Use language: "Potential technical non-compliance" instead of "Legal
  violation".
- Do not provide legal opinions or determine legal liability.
- Do not claim legal compliance or legal violation without appropriate context.

## Output

Generate `compliance.md` inside the audit workspace following the structure
defined in the Compliance Auditor agent file.

## Boundaries

This methodology does not:

- define compliance domains (see Compliance Auditor agent);
- define finding structure (see finding-model.md);
- define severity criteria (see severity-model.md);
- define status values (see status-model.md);
- define evidence rules (see evidence-model.md);
- define maturity levels (see maturity-model.md).
