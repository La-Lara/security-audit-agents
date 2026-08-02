# Architecture Documentation

## Overview

The Security Audit Agents Framework is a modular, LLM-agnostic, evidence-based
framework for auditing software repositories. It provides structured guidance
for security, monitoring, operations, compliance, and observability assessments.

## Core Principles

- Evidence-based assessment;
- Repository as source of truth;
- LLM-agnostic design;
- Vendor-agnostic approach;
- Tool-agnostic methodology.

## Framework Components

### Agents

Specialized auditors responsible for domain-specific assessments:

- Lead Auditor: Orchestrates the audit process;
- Security Auditor: Assesses security posture;
- Monitoring Auditor: Assesses monitoring readiness;
- Operations Auditor: Assess operational readiness;
- Compliance Auditor: Assesses technical compliance;
- Observability Auditor: Assesses observability maturity.

### Standards

Canonical definitions shared across all agents:

- Status Model: Finding status values;
- Severity Model: Impact classification;
- Evidence Model: Evidence rules;
- Finding Model: Finding structure;
- Maturity Model: Capability assessment levels.

### Methodologies

Domain-specific process guidance:

- Security Methodology;
- Monitoring Methodology;
- Operations Methodology;
- Compliance Methodology;
- Observability Methodology.

### Templates

Reusable structures for audit artifacts:

- Discovery Template;
- Finding Template;
- Risk Register Template;
- Executive Report Template;
- Technical Report Template;
- Roadmap Template;
- Audit Plan Template;
- Session Manifest Template.

### Frameworks

Curated audit references:

- OWASP Top 10;
- OWASP ASVS;
- OWASP MASVS;
- LGPD;
- NIST CSF;
- CIS Controls;

All frameworks are managed through the Framework Registry.

## Audit Flow

1. Discovery: Identify project characteristics and technologies;
2. Applicability: Determine which audit domains apply;
3. Planning: Select audit mode and frameworks;
4. Execution: Run specialized auditors;
5. Consolidation: Merge findings and generate reports.

## Artifact Generation

The Lead Auditor generates:

- discovery.md;
- applicability.md;
- audit-plan.md;
- session-manifest.md.

Specialized auditors generate:

- security.md;
- monitoring.md;
- operations.md;
- compliance.md;
- observability.md.

Consolidation generates:

- executive-report.md;
- technical-report.md;
- risk-register.md;
- audit-roadmap.md.

## LLM Portability

The framework is designed to work with any LLM:

- All instructions are in markdown files;
- No LLM-specific syntax or features;
- Evidence-based approach works across models;
- Structured output formats are consistent.

## Evidence Philosophy

Repository artifacts are the source of truth:

- No assumptions;
- No conversation memory;
- No inferred implementations;
- No invented findings.
