# Audit Flow Documentation

## Overview

This document describes the audit flow executed by the Lead Auditor and
specialized auditors.

## Audit Modes

### Discovery Mode

Only discovery and planning:

1. Inspect repository;
2. Identify technologies;
3. Determine applicability;
4. Present recommendations.

### Domain Modes

Execute specific auditor:

- security: Security Auditor only;
- monitoring: Monitoring Auditor only;
- operations: Operations Auditor only;
- compliance: Compliance Auditor only;
- observability: Observability Auditor only.

### Full Mode

Execute all applicable auditors:

1. Run discovery;
2. Determine applicability;
3. Select frameworks;
4. Execute applicable auditors;
5. Consolidate results.

## Phase Details

### Phase 1 - Discovery

Input: Repository path.

Process:

1. Inspect directory structure;
2. Identify programming languages;
3. Detect frameworks;
4. Find configuration files;
5. Locate security-relevant components.

Output: discovery.md.

---

### Phase 2 - Applicability

Input: discovery.md.

Process:

1. Evaluate each audit domain;
2. Classify applicability;
3. Document evidence.

Output: applicability.md.

---

### Phase 3 - Planning

Input: applicability.md, user preferences.

Process:

1. Present detected characteristics;
2. Recommend audit mode;
3. Wait for user selection;
4. Select applicable frameworks;
5. Record framework assignments.

Output: audit-plan.md.

---

### Phase 4 - Execution

Input: audit-plan.md, discovery.md, applicability.md, frameworks.

Process:

1. Load auditor instructions;
2. Provide artifacts to auditor;
3. Execute auditor independently;
4. Collect auditor output.

Output: domain-specific audit files.

---

### Phase 5 - Consolidation

Input: All audit artifacts.

Process:

1. Read all audit files;
2. Merge findings;
3. Remove duplicates;
4. Cross-reference issues;
5. Generate reports.

Output:

- executive-report.md;
- technical-report.md;
- risk-register.md;
- audit-roadmap.md.

## Auditor Independence

Each auditor works independently:

- No cross-auditor conclusions;
- No shared assumptions;
- Evidence-based only;
- Domain boundaries respected.

## Evidence Flow

1. Repository artifacts → Discovery;
2. Discovery → Applicability;
3. Applicability → Framework selection;
4. Framework selection → Auditor assignment;
5. Auditor execution → Domain findings;
6. Domain findings → Consolidation;
7. Consolidation → Reports.

## Quality Gates

Before consolidation:

- All findings have evidence;
- All statuses are valid;
- All severities are justified;
- No assumptions classified as facts.
