# OWASP Top 10 Framework

## Purpose

This file provides a concise, audit-oriented adaptation of the OWASP Top 10 for
use within the Security Audit Agents Framework. It is not a replacement for the
original standard.

## Version

2021

## Scope

Web applications, APIs, and backend services with user-controlled input.

## When to Use

Select this framework when repository evidence shows:

- web applications;
- APIs;
- user-controlled input handling;
- client-side processing.

## Risk Categories

### A01 - Broken Access Control

Evaluate evidence of:

- privilege enforcement;
- access control mechanisms;
- resource-level permissions.

Repository indicators:

- authorization middleware;
- role-based access configurations;
- endpoint access restrictions.

---

### A02 - Cryptographic Failures

Evaluate evidence of:

- sensitive data protection;
- encryption usage;
- key management.

Repository indicators:

- encryption libraries;
- TLS configurations;
- secret storage mechanisms.

---

### A03 - Injection

Evaluate evidence of:

- input sanitization;
- parameterized queries;
- output encoding.

Repository indicators:

- query builders;
- ORM usage;
- input validation functions.

---

### A04 - Insecure Design

Evaluate evidence of:

- security architecture patterns;
- threat modeling indicators;
- design-level controls.

Repository indicators:

- security middleware;
- architectural documentation;
- design patterns.

---

### A05 - Security Misconfiguration

Evaluate evidence of:

- default configurations;
- unnecessary features;
- error handling.

Repository indicators:

- configuration files;
- debug settings;
- error handlers.

---

### A06 - Vulnerable and Outdated Components

Evaluate evidence of:

- dependency management;
- version pinning;
- update mechanisms.

Repository indicators:

- package manifests;
- lock files;
- dependency scanning configurations.

---

### A07 - Identification and Authentication Failures

Evaluate evidence of:

- authentication mechanisms;
- session management;
- credential handling.

Repository indicators:

- authentication libraries;
- session configurations;
- password policies.

---

### A08 - Software and Data Integrity Failures

Evaluate evidence of:

- integrity verification;
- secure update mechanisms;
- CI/CD pipeline integrity.

Repository indicators:

- signed artifacts;
- integrity checks;
- pipeline configurations.

---

### A09 - Security Logging and Monitoring Failures

Evaluate evidence of:

- security logging;
- audit trails;
- monitoring integration.

Repository indicators:

- logging frameworks;
- audit configurations;
- monitoring libraries.

---

### A10 - Server-Side Request Forgery (SSRF)

Evaluate evidence of:

- URL validation;
- network access controls;
- external request handling.

Repository indicators:

- HTTP clients;
- URL validation logic;
- network configurations.

---

## Evidence Mapping

Map repository evidence to risk categories. Do not force mappings. Only create
findings when repository evidence supports the risk.

## Limitations

- This is an adapted reference, not the full OWASP standard.
- Do not use as a checklist; use as evidence-based guidance.
- Risk categories are not finding identifiers.
- Always prioritize repository evidence over framework categories.

## Reference

OWASP Top 10: https://owasp.org/www-project-top-ten/
