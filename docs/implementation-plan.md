# Security Audit Agents Framework Implementation Plan

## Current State

The repository contains the intended top-level structure for an LLM-agnostic, evidence-based security audit framework:

- `agents/` contains six agent definitions: Lead, Security, Monitoring, Operations, Compliance, and Observability.
- `frameworks/_framework-registry.md` exists and is the current authoritative framework selection catalog.
- `frameworks/*.md` files for OWASP Top 10, OWASP ASVS, OWASP MASVS, LGPD, NIST CSF, and CIS Controls exist but are empty.
- `standards/`, `methodologies/`, `templates/`, and `docs/` mostly contain empty placeholders.
- `examples/desktop-app`, `examples/mobile-app`, and `examples/web-api` exist as empty directories.
- `README.md` is minimal and contains encoding artifacts.
- `LICENSE` is complete.

The framework direction is clear, but many required artifacts are incomplete. The main architectural inconsistency is that the Lead Auditor currently does not fully support the `observability` audit mode even though the Observability Auditor exists.

## Repository Inventory

| Path | Current Purpose | Status | Dependencies | Issues |
|---|---|---|---|---|
| `README.md` | Project overview | Partial | Architecture docs | Minimal; encoding artifact; does not describe usage or current maturity |
| `LICENSE` | License | Complete | None | None identified |
| `.gitignore` | Ignore local IDE metadata | Partial | None | Only ignores `.vscode`; must not be modified automatically |
| `.vscode/.checkmarxIgnored` | IDE/tool metadata | Unclear | `.vscode` | Not part of framework architecture |
| `agents/_lead-auditor.md` | Orchestration agent | Partial | Registry, standards, templates, auditor files | Missing `observability` mode; no session manifest; no explicit audit-plan structure; maturity excludes Observability |
| `agents/security-auditor.md` | Security auditor | Partial | Standards, methodology, selected frameworks | Contains local status/severity/maturity definitions duplicated from future standards |
| `agents/monitoring-auditor.md` | Monitoring auditor | Partial | Standards, methodology | Duplicates status/severity/maturity definitions; needs canonical references |
| `agents/operations-auditor.md` | Operations auditor | Partial | Standards, methodology | Duplicates status/severity/maturity/evidence definitions |
| `agents/compliance-auditor.md` | Compliance auditor | Partial | Standards, methodology, selected frameworks | Duplicates status/severity/maturity/evidence definitions; LGPD sections must stay technical |
| `agents/observability-auditor.md` | Observability auditor | Partial | Standards, methodology decision | Exists but Lead does not fully orchestrate it; no methodology file yet |
| `frameworks/_framework-registry.md` | Framework metadata and selection authority | Partial | Framework files | Good authority model; version and review metadata are still `TBD` |
| `frameworks/owasp-top10.md` | Reserved customized framework file | Empty | Registry | Must be completed later without copying original standard |
| `frameworks/owasp-asvs.md` | Reserved customized framework file | Empty | Registry | Must be completed later without copying original standard |
| `frameworks/owasp-masvs.md` | Reserved customized framework file | Empty | Registry | Must be completed later without copying original standard |
| `frameworks/lgpd.md` | Reserved customized framework file | Empty | Registry | Must remain technical, not legal advice |
| `frameworks/nist-csf.md` | Reserved customized framework file | Empty | Registry | Must remain high-level and evidence-based |
| `frameworks/cis-controls.md` | Reserved customized framework file | Empty | Registry | Must be concise and audit-oriented |
| `standards/evidence-model.md` | Canonical evidence model | Empty | Agents, templates, methodologies | Required shared source of truth missing |
| `standards/finding-model.md` | Canonical finding model | Empty | Agents, templates | Required shared source of truth missing |
| `standards/maturity-model.md` | Canonical maturity model | Empty | Agents, reports | Required shared source of truth missing |
| `standards/severity-model.md` | Canonical severity model | Empty | Agents, findings | Required shared source of truth missing |
| `standards/status-model.md` | Canonical status model | Empty | Agents, findings | Required shared source of truth missing |
| `methodologies/security-methodology.md` | Security audit process | Empty | Security Auditor, standards | Required process guidance missing |
| `methodologies/monitoring-methodology.md` | Monitoring audit process | Empty | Monitoring Auditor, standards | Required process guidance missing |
| `methodologies/operations-methodology.md` | Operations audit process | Empty | Operations Auditor, standards | Required process guidance missing |
| `methodologies/compliance-methodology.md` | Compliance audit process | Empty | Compliance Auditor, standards | Required process guidance missing |
| `docs/architecture.md` | Architecture documentation | Empty | Agents, registry, standards | Required human/LLM documentation missing |
| `docs/audit-flow.md` | Audit flow documentation | Empty | Lead Auditor, templates | Required flow documentation missing |
| `docs/framework-concepts.md` | Framework concept documentation | Empty | Registry, framework files | Required framework guidance missing |
| `templates/discovery-template.md` | Discovery artifact template | Empty | Lead Auditor | Required template missing |
| `templates/finding-template.md` | Finding template | Empty | Finding model | Required template missing |
| `templates/risk-register-template.md` | Risk register template | Empty | Finding, severity, status models | Required template missing |
| `templates/executive-report-template.md` | Executive report template | Empty | Consolidation | Required template missing |
| `templates/technical-report-template.md` | Technical report template | Empty | Consolidation | Required template missing |
| `templates/roadmap-template.md` | Roadmap template | Empty | Consolidation | Required template missing |
| `examples/desktop-app/` | Example directory | Empty | Future examples | Needs minimal example artifact flow |
| `examples/mobile-app/` | Example directory | Empty | Future examples | Needs minimal example artifact flow |
| `examples/web-api/` | Example directory | Empty | Future examples | Needs minimal example artifact flow |

## Target State

The repository should provide a complete, modular, LLM-agnostic framework for auditing software repositories. The Lead Auditor orchestrates discovery, applicability analysis, planning, framework selection through the registry, specialized auditor execution, and consolidation. Specialized auditors consume only Lead-selected frameworks and produce evidence-based artifacts. Shared standards define canonical statuses, severity, evidence, finding, and maturity models. Methodologies define domain process. Templates define artifact structure. Framework files provide concise customized audit references. Docs and README explain how humans and LLM agents use the framework.

## Constraints

- Preserve the existing architecture and terminology.
- Do not redesign the framework from scratch.
- Keep the framework technology-agnostic, LLM-agnostic, vendor-agnostic, and tool-agnostic.
- Use repository evidence and audit artifacts as the audit source of truth.
- Do not rely on conversation memory.
- Do not invent findings, vulnerabilities, technologies, controls, tests, legal compliance, or legal violations.
- Do not force irrelevant frameworks or auditors.
- Do not load every framework automatically.
- Keep framework selection authoritative in `frameworks/_framework-registry.md`.
- Do not copy full copyrighted framework publications.
- Do not modify `.gitignore` automatically.
- Do not commit or push changes as part of implementation.
- Preserve progress in `docs/implementation-status.md`.

## Architecture Consistency Review

Identified inconsistencies and gaps:

- Lead Auditor lists `observability-auditor.md` but omits `observability` from supported audit modes.
- Lead Auditor maturity assessment omits Observability.
- Lead Auditor generates several artifacts but lacks explicit `session-manifest.md` and `audit-plan.md` structure.
- Standards are empty, so agents duplicate canonical status, severity, maturity, evidence, and finding rules.
- Methodologies are empty.
- Templates are empty and do not yet align with required audit workspace artifacts.
- Docs are empty.
- Framework files are empty even though the registry marks frameworks as available.
- Registry version and review fields remain `TBD`.
- Example directories are empty.
- README does not describe architecture, usage, limitations, audit modes, or portability.
- Compliance and Security auditors include framework mapping examples; these are output guidance, not selection rules, but should be reviewed after framework files exist.

## Task Dependency Graph

```text
T01 -> T02 -> T03 -> T04 -> T05 -> T06 -> T07 -> T08 -> T09 -> T10 -> T11 -> T12 -> T13
                  \                         \       \       \       \
                   \                         -> T14  -> T15  -> T16  -> T17
```

- T01 establishes persistent planning and inventory.
- T02 creates canonical standards.
- T03 creates methodologies.
- T04 creates templates.
- T05 refines registry metadata.
- T06-T11 complete customized framework files.
- T12 aligns agents.
- T13 completes docs.
- T14 completes README.
- T15 adds examples.
- T16 validates the framework.
- T17 records final status.

## Small Tasks

### T01 - Persistent Planning and Initial Status

- Objective: Create implementation plan and resumable status artifacts.
- Files allowed to change: `docs/implementation-plan.md`, `docs/implementation-status.md`.
- Files that must not change: all other files.
- Dependencies: repository discovery.
- Implementation steps: record inventory, constraints, task graph, tasks, current status.
- Acceptance criteria: both docs exist and describe current state and next task.
- Validation method: read both files and confirm task statuses.
- Status: COMPLETED.

### T02 - Define Shared Standards

- Objective: Complete canonical status, severity, evidence, finding, and maturity models.
- Files allowed to change: `standards/*.md`, `docs/implementation-status.md`.
- Files that must not change: agents, frameworks, templates, methodologies, README.
- Dependencies: T01.
- Implementation steps: define allowed values, usage rules, evidence language, model boundaries, validation rules.
- Acceptance criteria: all five standard files contain concise canonical definitions aligned with agents.
- Validation method: search agents for conflicting values; verify no new values introduced.
- Status: IN_PROGRESS.

### T03 - Define Methodologies

- Objective: Complete domain audit process files.
- Files allowed to change: `methodologies/*.md`, optional `methodologies/observability-methodology.md`, `docs/implementation-status.md`.
- Files that must not change: framework files, agents except status doc.
- Dependencies: T02.
- Implementation steps: define process phases, inputs, evidence handling, outputs, and boundaries for each domain; decide whether observability methodology is required.
- Acceptance criteria: methodology files guide process without duplicating full agent roles.
- Validation method: compare domains to agent responsibilities.
- Status: PENDING.

### T04 - Define Artifact Templates

- Objective: Complete templates for expected audit outputs.
- Files allowed to change: `templates/*.md`, optional missing templates if justified, `docs/implementation-status.md`.
- Files that must not change: agents, frameworks.
- Dependencies: T02.
- Implementation steps: create reusable structures for discovery, findings, risk register, executive report, technical report, roadmap; evaluate applicability/audit-plan/session-manifest templates.
- Acceptance criteria: templates align with statuses, severity, evidence, and artifacts named by Lead.
- Validation method: path and artifact name review.
- Status: PENDING.

### T05 - Refine Registry Metadata

- Objective: Replace `TBD` metadata where feasible and verify registry authority.
- Files allowed to change: `frameworks/_framework-registry.md`, `docs/implementation-status.md`.
- Files that must not change: other framework files.
- Dependencies: T02.
- Implementation steps: update version/review status fields conservatively; ensure all registered framework files exist.
- Acceptance criteria: registry remains single source of truth and references valid files.
- Validation method: path validation and duplicate selection search.
- Status: PENDING.

### T06 - Complete OWASP Top 10 Framework File

- Objective: Create concise audit-oriented OWASP Top 10 adaptation.
- Files allowed to change: `frameworks/owasp-top10.md`, `docs/implementation-status.md`.
- Files that must not change: other frameworks.
- Dependencies: T05.
- Acceptance criteria: contains applicability, domains, evidence, mapping guidance, limitations, metadata.
- Validation method: compare to registry purpose; check no copied full standard.
- Status: PENDING.

### T07 - Complete OWASP ASVS Framework File

- Objective: Create concise audit-oriented ASVS adaptation.
- Files allowed to change: `frameworks/owasp-asvs.md`, `docs/implementation-status.md`.
- Dependencies: T05.
- Acceptance criteria: covers application/API verification guidance without copying ASVS.
- Validation method: compare to registry purpose.
- Status: PENDING.

### T08 - Complete OWASP MASVS Framework File

- Objective: Create concise audit-oriented MASVS adaptation.
- Files allowed to change: `frameworks/owasp-masvs.md`, `docs/implementation-status.md`.
- Dependencies: T05.
- Acceptance criteria: covers mobile evidence and local/remote boundaries.
- Validation method: conceptual local mobile profile simulation.
- Status: PENDING.

### T09 - Complete LGPD Framework File

- Objective: Create technical LGPD audit reference.
- Files allowed to change: `frameworks/lgpd.md`, `docs/implementation-status.md`.
- Dependencies: T05.
- Acceptance criteria: technical only, no legal advice, evidence-based privacy controls.
- Validation method: legal-boundary language review.
- Status: PENDING.

### T10 - Complete NIST CSF Framework File

- Objective: Create high-level cybersecurity maturity and lifecycle reference.
- Files allowed to change: `frameworks/nist-csf.md`, `docs/implementation-status.md`.
- Dependencies: T05.
- Acceptance criteria: high-level functions, evidence mapping, no forced maturity use.
- Validation method: small-repo non-applicability review.
- Status: PENDING.

### T11 - Complete CIS Controls Framework File

- Objective: Create concise prioritized controls reference.
- Files allowed to change: `frameworks/cis-controls.md`, `docs/implementation-status.md`.
- Dependencies: T05.
- Acceptance criteria: safeguards are selectable only when repository evidence supports them.
- Validation method: infrastructure/control applicability review.
- Status: PENDING.

### T12 - Align Agent Definitions

- Objective: Align all six agents with standards, methodologies, templates, registry, and audit modes.
- Files allowed to change: `agents/*.md`, `docs/implementation-status.md`.
- Dependencies: T02, T03, T04, T05.
- Acceptance criteria: Lead supports `observability`; all agents use canonical artifacts and models; boundaries remain intact.
- Validation method: search for outdated modes, missing artifacts, independent framework selection.
- Status: PENDING.

### T13 - Complete Architecture Documentation

- Objective: Complete `docs/architecture.md`, `docs/audit-flow.md`, and `docs/framework-concepts.md`.
- Files allowed to change: those docs and `docs/implementation-status.md`.
- Dependencies: T02-T12.
- Acceptance criteria: docs explain architecture, flow, artifacts, framework concepts, LLM portability, and evidence philosophy.
- Validation method: read-through and reference validation.
- Status: PENDING.

### T14 - Complete README

- Objective: Update README after architecture files are stable.
- Files allowed to change: `README.md`, `docs/implementation-status.md`.
- Dependencies: T13.
- Acceptance criteria: README explains purpose, usage, modes, limitations, framework selection, maturity, and future work.
- Validation method: compare README claims to actual files.
- Status: PENDING.

### T15 - Add Minimal Examples

- Objective: Add small human-readable example flows without building sample apps.
- Files allowed to change: files under `examples/`, `docs/implementation-status.md`.
- Dependencies: T04, T12, T13.
- Acceptance criteria: examples show detected architecture, applicability, selected agents, selected frameworks, and artifact shape.
- Validation method: conceptual profile review.
- Status: PENDING.

### T16 - Static End-to-End Validation

- Objective: Validate paths, references, terms, modes, framework selection, and conceptual profiles.
- Files allowed to change: `docs/implementation-status.md`, optional `docs/validation-report.md`.
- Dependencies: T02-T15.
- Acceptance criteria: validation results recorded with pass/fail and remaining issues.
- Validation method: static search, path checks, conceptual simulations.
- Status: PENDING.

### T17 - Final Status Update

- Objective: Record final repository state and remaining recommendations.
- Files allowed to change: `docs/implementation-status.md`.
- Dependencies: T16.
- Acceptance criteria: status file states readiness and next known work.
- Validation method: final read-through.
- Status: PENDING.
