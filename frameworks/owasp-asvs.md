# OWASP ASVS Framework

## Purpose

This file provides a concise, audit-oriented adaptation of the OWASP Application
Security Verification Standard (ASVS) for use within the Security Audit Agents
Framework. It is not a replacement for the original standard.

## Version

4.0.3

## Scope

Web applications, backend services, APIs, and systems with authentication,
authorization, or user input handling.

## When to Use

Select this framework when repository evidence shows:

- web applications with user authentication;
- backend services processing user requests;
- APIs with access control requirements;
- systems requiring application security verification.

## Verification Levels

### Level 1 - Baseline

Basic security controls suitable for low-risk applications.

Focus areas:

- basic authentication;
- basic access control;
- basic input validation;
- basic cryptography.

---

### Level 2 - Standard

Standard security controls for most applications.

Focus areas:

- secure authentication;
- session management;
- access control;
- input validation;
- cryptography;
- error handling;
- logging.

---

### Level 3 - Advanced

Advanced security controls for high-risk applications.

Focus areas:

- advanced authentication;
- advanced authorization;
- advanced cryptography;
- secure architecture;
- advanced logging and monitoring.

---

## Verification Categories

### V1 - Architecture, Design and Threat Modeling

Evaluate evidence of:

- security architecture documentation;
- threat modeling;
- secure design patterns.

---

### V2 - Authentication

Evaluate evidence of:

- password requirements;
- multi-factor authentication;
- credential recovery;
- session management.

---

### V3 - Session Management

Evaluate evidence of:

- session token handling;
- session expiration;
- session fixation prevention.

---

### V4 - Access Control

Evaluate evidence of:

- authorization mechanisms;
- role-based access;
- resource-level access control.

---

### V5 - Input Validation

Evaluate evidence of:

- input sanitization;
- parameterized queries;
- output encoding.

---

### V6 - Cryptography

Evaluate evidence of:

- encryption algorithms;
- key management;
- secure random number generation.

---

### V7 - Error Handling and Logging

Evaluate evidence of:

- error handling mechanisms;
- logging practices;
- sensitive data exposure prevention.

---

### V8 - Data Protection

Evaluate evidence of:

- data classification;
- data encryption;
- data retention;
- secure data disposal.

---

### V9 - Communication Security

Evaluate evidence of:

- TLS configuration;
- certificate management;
- secure communication channels.

---

### V10 - Malicious Code防护

Evaluate evidence of:

- code review practices;
- dependency scanning;
- malicious code prevention.

---

## Evidence Mapping

Map repository evidence to verification categories. Do not force mappings. Only
create findings when repository evidence supports the control gap.

## Limitations

- This is an adapted reference, not the full ASVS standard.
- Do not use as a checklist; use as evidence-based guidance.
- Verification levels are guidance, not requirements.
- Always prioritize repository evidence over framework categories.

## Reference

OWASP ASVS: https://owasp.org/www-project-application-security-verification-standard/
