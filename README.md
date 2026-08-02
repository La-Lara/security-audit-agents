# Security Audit Agents Framework

A modular, LLM-agnostic, evidence-based framework for auditing software
repositories.

## Overview

This framework provides structured guidance for security, monitoring,
operations, compliance, and observability assessments. It is designed to work
with any LLM and provides evidence-based audit capabilities.

## Features

- Multi-agent architecture;
- Evidence-based assessment;
- LLM-agnostic design;
- Framework-agnostic approach;
- Modular structure.

## Architecture

### Agents

- Lead Auditor: Orchestrates the audit process;
- Security Auditor: Assesses security posture;
- Monitoring Auditor: Assesses monitoring readiness;
- Operations Auditor: Assesses operational readiness;
- Compliance Auditor: Assesses technical compliance;
- Observability Auditor: Assesses observability maturity.

### Standards

- Status Model;
- Severity Model;
- Evidence Model;
- Finding Model;
- Maturity Model.

### Frameworks

- OWASP Top 10;
- OWASP ASVS;
- OWASP MASVS;
- LGPD;
- NIST CSF;
- CIS Controls.

## Usage

### Discovery Mode

```
TARGET_REPOSITORY=<path>
```

Only discovery and planning.

### Domain Modes

```
TARGET_REPOSITORY=<path>
AUDIT_MODE=security
```

Execute specific auditor.

### Full Mode

```
TARGET_REPOSITORY=<path>
AUDIT_MODE=full
```

Execute all applicable auditors.

## Audit Modes

- discovery: Only discovery and planning;
- security: Security Auditor only;
- monitoring: Monitoring Auditor only;
- operations: Operations Auditor only;
- compliance: Compliance Auditor only;
- observability: Observability Auditor only;
- full: All applicable auditors.

## Audit Workspace

Default: `.audit`

The audit workspace contains all generated artifacts.

## Documentation

- `docs/architecture.md`: Architecture documentation;
- `docs/audit-flow.md`: Audit flow documentation;
- `docs/framework-concepts.md`: Framework concepts.

## Limitations

- Evidence-based only;
- No assumptions;
- No conversation memory;
- Repository is the source of truth.

## License

See LICENSE file.
