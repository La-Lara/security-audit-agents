# Framework Registry

## Purpose

This document provides the catalog of security, compliance, and operational frameworks available in this audit framework.

Its purpose is to help:

- Lead Auditor select applicable frameworks;
- auditors understand available references;
- maintain framework versions;
- identify missing framework coverage.

This document contains metadata only.

The detailed audit criteria remain inside each framework file.

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

Only applicable frameworks should be loaded by auditors.

---

# Available Frameworks

---

# OWASP ASVS

## File
frameworks/owasp-asvs.md

## Purpose

Application Security Verification Standard.

Provides security requirements for web applications and backend systems.

## Used By

- Security Auditor

## Apply When

- Web applications exist;
- Backend services exist;
- APIs process user requests;
- Authentication or authorization exists.

## Not Primary For

- Native mobile-only applications.

## Status

Available

## Version

TBD

## Last Review

TBD

---

# OWASP MASVS

## File
frameworks/owasp-masvs.md

## Purpose

Mobile Application Security Verification Standard.

Provides security requirements for mobile applications.

## Used By

- Security Auditor

## Apply When

- Android applications exist;
- iOS applications exist;
- Mobile application security is in scope.

## Covers

- local storage;
- authentication;
- communication security;
- platform interaction;
- cryptography.

## Status

Available

## Version

TBD

## Last Review

TBD

---

# OWASP Top 10

## File
frameworks/owasp-top10.md

## Purpose

Reference for common web application security risks.

## Used By

- Security Auditor

## Apply When

- Web applications exist;
- APIs exist;
- User-controlled input exists.

## Status

Available

## Version

TBD

## Last Review

TBD

---

# NIST Cybersecurity Framework

## File
frameworks/nist-csf.md

## Purpose

Cybersecurity risk management framework.

## Used By

- Lead Auditor
- Security Auditor
- Operations Auditor

## Apply When

- Enterprise security maturity is evaluated;
- Governance is relevant;
- Security lifecycle assessment is required.

## Covers

- Identify;
- Protect;
- Detect;
- Respond;
- Recover.

## Status

Available

## Version

TBD

## Last Review

TBD

---

# CIS Controls

## File
frameworks/cis-controls.md

## Purpose

Security controls baseline.

## Used By

- Security Auditor
- Operations Auditor

## Apply When

- General security posture is evaluated;
- Infrastructure or operational controls exist.

## Status

Available

## Version

TBD

## Last Review

TBD

---

# LGPD Technical Audit Framework

## File
frameworks/lgpd.md

## Purpose

Technical privacy and personal data protection assessment.

## Used By

- Compliance Auditor

## Apply When

- Personal data exists;
- User accounts exist;
- Customer information is processed;
- Personal information storage exists.

## Covers

- data protection;
- privacy controls;
- data lifecycle;
- technical safeguards.

## Status

Available

## Version

TBD

## Last Review

TBD

---

# Future Framework Candidates

The following frameworks may be added in future versions.

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