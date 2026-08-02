# Framework Registry

## Purpose

This document provides the catalog of security, compliance, and operational frameworks available in this audit framework.

Its purpose is to help:

- Lead Auditor select applicable frameworks;
- maintain framework versions;
- identify missing framework coverage.

This document contains metadata only.

The detailed audit criteria remain inside each framework file.

---

# Registry Authority

This registry is the single source of truth for framework selection.

Framework metadata must not be duplicated elsewhere.

Every new framework must first be registered here before it can be selected, assigned, or loaded by any auditor.

The Lead Auditor must select frameworks exclusively from this registry.

Specialized auditors must use only the frameworks supplied by the Lead Auditor.

---

# Framework Location

All framework files are located under:
frameworks/

---

# Framework Selection Principles

Frameworks should be selected based on:

- application type;
- architecture;
- data processed;
- technology stack;
- audit objective.

Do not apply all frameworks automatically.

Only frameworks supported by project evidence should be selected.

The Lead Auditor must record:

- selected frameworks;
- auditor assignment;
- evidence supporting each selection;
- skipped frameworks;
- justification for each skipped framework.

Auditors must load only the frameworks assigned to them by the Lead Auditor.

---

# Available Frameworks

| Framework | Location | Purpose | Supported Audit Domains | Supported Project Types | Responsible Auditor(s) | Applicability Criteria | Selection Notes | Dependencies | Incompatible Scenarios | Priority | Version | Review Status | Last Review |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| OWASP ASVS | frameworks/owasp-asvs.md | Application Security Verification Standard for web applications and backend systems. | Application Security; Secure Coding; API Security | Web application; backend service; API | Security Auditor | Select when repository evidence shows web applications, backend services, APIs that process user requests, authentication, or authorization. | Use as the primary application security reference when application security depth is required. | None | Native mobile-only applications without web, backend, or API scope. | High | 4.0.3 | Available | 2024-01-15 |
| OWASP MASVS | frameworks/owasp-masvs.md | Mobile Application Security Verification Standard for mobile applications. | Mobile Security; Application Security; Secure Coding | Mobile application; Android application; iOS application | Security Auditor | Select when repository evidence shows Android code, iOS code, mobile application structure, or mobile application security scope. | Use as the primary mobile application security reference. | None | Projects without mobile application evidence. | High | 2.0.0 | Available | 2024-01-15 |
| OWASP Top 10 | frameworks/owasp-top10.md | Reference for common web application security risks. | Web Security; API Security; Application Security | Web application; API; backend service | Security Auditor | Select when repository evidence shows web applications, APIs, or user-controlled input handling. | Use as a risk-category mapping reference; do not use as a replacement for evidence-based findings. | None | Native mobile-only applications without web, backend, or API scope. | Medium | 2021 | Available | 2024-01-15 |
| NIST Cybersecurity Framework | frameworks/nist-csf.md | Cybersecurity risk management framework. | Security Governance; Security Maturity; Operational Resilience; Incident Response | Enterprise system; service platform; infrastructure project; hybrid project | Lead Auditor; Security Auditor; Operations Auditor | Select when repository evidence or audit objective supports enterprise security maturity, governance relevance, security lifecycle assessment, or risk management assessment. | Use for lifecycle and maturity context across Identify, Protect, Detect, Respond, and Recover functions. | None | Narrow code-only audits where governance, lifecycle, or maturity assessment is outside scope. | Medium | 2.0 | Available | 2024-01-15 |
| CIS Controls | frameworks/cis-controls.md | Security controls baseline. | Infrastructure Security; Secure Operations; General Security Controls; CI/CD Security | Infrastructure project; service platform; backend service; cloud or deployment-aware project | Security Auditor; Operations Auditor | Select when repository evidence shows general security posture assessment, infrastructure definitions, deployment configuration, operational controls, or CI/CD controls. | Use as a baseline controls reference when control coverage can be mapped to repository evidence. | None | Projects with no infrastructure, deployment, operational, or control evidence in audit scope. | Medium | 8.1 | Available | 2024-01-15 |
| LGPD Technical Audit Framework | frameworks/lgpd.md | Technical privacy and personal data protection assessment. | Privacy; LGPD; Data Protection; Technical Compliance | Application handling personal data; API handling personal data; system with user accounts or customer records | Compliance Auditor | Select when repository evidence shows personal data, user accounts, customer information, personal information storage, or privacy-related processing. | Use only for technical and documentary compliance assessment; do not produce legal opinions. | None | Projects without evidence of personal data or privacy-related processing in audit scope. | High | 2024 | Available | 2024-01-15 |

---

# Future Framework Candidates

The following frameworks may be added in future versions.

These candidates are not available for audit selection until they are moved into the Available Frameworks table with complete registry metadata.

---

# OWASP API Security Top 10

## Recommended For

- REST APIs;
- GraphQL APIs;
- Backend services.

## Used By

- Security Auditor

## Priority

High

---

# OWASP SAMM

## Recommended For

- Secure development lifecycle assessment;
- software security maturity evaluation.

## Used By

- Lead Auditor
- Security Auditor

## Priority

Medium

---

# OWASP Mobile Top 10

## Recommended For

- Mobile application security complementing MASVS.

## Used By

- Security Auditor

## Priority

Medium

---

# CIS Benchmarks

## Recommended For

- Infrastructure hardening;
- operating systems;
- cloud environments.

## Used By

- Operations Auditor
- Security Auditor

## Priority

Medium

---

# Framework Maintenance

Each framework should maintain:

- version;
- last review date;
- source/reference;
- applicability.

Before an audit, the Lead Auditor should verify:

- framework availability;
- framework relevance;
- framework review status.

---

# Current Coverage Summary

| Area | Framework Coverage |
|---|---|
| Mobile Application | OWASP MASVS |
| Web Application | OWASP ASVS + OWASP Top 10 |
| APIs | OWASP ASVS (future: OWASP API Security Top 10) |
| Privacy | LGPD |
| Security Governance | NIST CSF |
| General Security Controls | CIS Controls |
| Infrastructure Hardening | Future CIS Benchmarks |
