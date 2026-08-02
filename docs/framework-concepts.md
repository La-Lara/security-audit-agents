# Framework Concepts Documentation

## Overview

This document explains how frameworks are used within the Security Audit Agents
Framework.

## Framework Purpose

Frameworks provide:

- Structured audit references;
- Control categories;
- Evidence mapping guidance;
- Risk classification support.

Frameworks do not provide:

- Evidence;
- Findings;
- Compliance conclusions;
- Legal opinions.

## Framework Registry

The registry is the single source of truth:

- Available frameworks;
- Framework metadata;
- Selection criteria;
- Version information.

All framework selection must come from the registry.

## Framework Selection

### Selection Process

1. Analyze discovery results;
2. Analyze applicability results;
3. Consult registry;
4. Select applicable frameworks;
5. Assign to auditors;
6. Record decisions.

### Selection Criteria

- Project type match;
- Technology relevance;
- Audit objective alignment;
- Evidence support.

### Selection Rules

- Do not load all frameworks automatically;
- Only select frameworks supported by evidence;
- Record selection justification;
- Record skipped frameworks.

## Framework Usage

### By Specialized Auditors

- Use only assigned frameworks;
- Do not select independent frameworks;
- Map evidence to framework controls;
- Do not force mappings.

### By Lead Auditor

- Select frameworks from registry;
- Assign to appropriate auditors;
- Record selection decisions;
- Monitor framework usage.

## Framework Types

### Security Frameworks

- OWASP Top 10: Risk categories;
- OWASP ASVS: Verification levels;
- OWASP MASVS: Mobile security.

### Compliance Frameworks

- LGPD: Privacy controls.

### Governance Frameworks

- NIST CSF: Security lifecycle.

### Controls Frameworks

- CIS Controls: Security baseline.

## Evidence Mapping

### Mapping Principles

- Evidence comes from repository;
- Frameworks are references only;
- Do not force mappings;
- Natural alignment required.

### Mapping Process

1. Collect repository evidence;
2. Consult framework controls;
3. Identify natural alignment;
4. Document mapping;
5. Create findings only for gaps.

## Limitations

- Frameworks are not evidence;
- Frameworks are not checklists;
- Frameworks are not compliance guarantees;
- Repository evidence always takes precedence.

## Version Management

- Registry tracks versions;
- Review status documented;
- Updates recorded;
- Legacy versions noted.
