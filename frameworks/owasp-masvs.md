# OWASP MASVS Framework

## Purpose

This file provides a concise, audit-oriented adaptation of the OWASP Mobile
Application Security Verification Standard (MASVS) for use within the Security
Audit Agents Framework. It is not a replacement for the original standard.

## Version

2.0.0

## Scope

Android applications, iOS applications, and cross-platform mobile applications.

## When to Use

Select this framework when repository evidence shows:

- Android code (Java, Kotlin);
- iOS code (Swift, Objective-C);
- mobile application structure;
- mobile-specific security concerns.

## Verification Levels

### Level 1 - Standard

Standard security controls for mobile applications.

Focus areas:

- basic data storage security;
- basic authentication;
- basic network communication.

---

### Level 2 - Resilient

Advanced security controls for mobile applications handling sensitive data.

Focus areas:

- advanced data protection;
- advanced authentication;
- advanced cryptography;
- reverse engineering resistance.

---

## Verification Categories

### MASVS-STORAGE - Data Storage

Evaluate evidence of:

- local data storage;
- file system security;
- database security;
- keychain/keystore usage;
- sensitive data exposure.

---

### MASVS-CRYPTO - Cryptography

Evaluate evidence of:

- encryption algorithms;
- key management;
- cryptographic implementations;
- secure random number generation.

---

### MASVS-AUTH - Authentication

Evaluate evidence of:

- authentication mechanisms;
- session management;
- biometric authentication;
- multi-factor authentication.

---

### MASVS-NETWORK - Network Communication

Evaluate evidence of:

- TLS configuration;
- certificate validation;
- network security configuration;
- API communication security.

---

### MASVS-PLATFORM - Platform Interaction

Evaluate evidence of:

- permission handling;
- inter-process communication;
- intent handling;
- URL scheme handling.

---

### MASVS-CODE - Code Quality

Evaluate evidence of:

- code quality practices;
- error handling;
- memory management;
- binary protection.

---

### MASVS-RESILIENCE - Resilience

Evaluate evidence of:

- anti-tampering mechanisms;
- reverse engineering resistance;
- root/jailbreak detection;
- code obfuscation.

---

## Evidence Mapping

Map repository evidence to verification categories. Do not force mappings. Only
create findings when repository evidence supports the control gap.

## Mobile-Specific Considerations

Evaluate local storage security for:

- SharedPreferences (Android);
- UserDefaults (iOS);
- SQLite databases;
- file system storage.

Evaluate secrets exposure in:

- compiled binaries;
- configuration files;
- log outputs.

## Limitations

- This is an adapted reference, not the full MASVS standard.
- Do not use as a checklist; use as evidence-based guidance.
- Verification levels are guidance, not requirements.
- Always prioritize repository evidence over framework categories.

## Reference

OWASP MASVS: https://mas.owasp.org/MASVS/
