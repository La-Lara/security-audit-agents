# CIS Controls Framework

## Purpose

This file provides a concise, audit-oriented adaptation of the CIS Controls for
use within the Security Audit Agents Framework. It is not a replacement for the
original standard.

## Version

8.1

## Scope

Infrastructure projects, service platforms, backend services, cloud projects,
and deployment-aware projects.

## When to Use

Select this framework when repository evidence shows:

- general security posture assessment;
- infrastructure definitions;
- deployment configurations;
- operational controls;
- CI/CD controls.

## Control Categories

### Control 1 - Inventory and Control of Enterprise Assets

Evaluate evidence of:

- asset inventory;
- device management;
- network discovery.

Repository indicators:

- infrastructure manifests;
- deployment configurations;
- network definitions.

---

### Control 2 - Inventory and Control of Software Assets

Evaluate evidence of:

- software inventory;
- application management;
- authorized software.

Repository indicators:

- package manifests;
- dependency files;
- application configurations.

---

### Control 3 - Data Protection

Evaluate evidence of:

- data classification;
- data protection mechanisms;
- data retention;
- secure data handling.

Repository indicators:

- encryption configurations;
- data storage mechanisms;
- access controls.

---

### Control 4 - Secure Configuration of Enterprise Assets and Software

Evaluate evidence of:

- configuration management;
- secure configurations;
- configuration hardened.

Repository indicators:

- configuration files;
- infrastructure as code;
- deployment manifests.

---

### Control 5 - Account Management

Evaluate evidence of:

- account inventory;
- access control;
- account lifecycle management.

Repository indicators:

- authentication configurations;
- authorization mechanisms;
- user management.

---

### Control 6 - Access Control Management

Evaluate evidence of:

- access control policies;
- privilege management;
- access reviews.

Repository indicators:

- access control implementations;
- role definitions;
- permission configurations.

---

### Control 7 - Continuous Vulnerability Management

Evaluate evidence of:

- vulnerability scanning;
- patch management;
- vulnerability remediation.

Repository indicators:

- scanning configurations;
- dependency management;
- update mechanisms.

---

### Control 8 - Audit Log Management

Evaluate evidence of:

- audit logging;
- log management;
- log review processes.

Repository indicators:

- logging configurations;
- audit trail implementations;
- log storage.

---

### Control 9 - Email and Web Browser Protections

Evaluate evidence of:

- email security;
- web browser security;
- content filtering.

Repository indicators:

- email configurations;
- browser security settings;
- proxy configurations.

---

### Control 10 - Malware Defenses

Evaluate evidence of:

- anti-malware solutions;
- malware prevention;
- malware detection.

Repository indicators:

- security tool configurations;
- endpoint protection;
- scanning mechanisms.

---

### Control 11 - Data Recovery

Evaluate evidence of:

- backup strategies;
- recovery procedures;
- data restoration.

Repository indicators:

- backup configurations;
- recovery documentation;
- restoration procedures.

---

### Control 12 - Network Infrastructure Management

Evaluate evidence of:

- network management;
- network security;
- network monitoring.

Repository indicators:

- network configurations;
- firewall rules;
- network segmentation.

---

### Control 13 - Network Monitoring and Defense

Evaluate evidence of:

- network monitoring;
- intrusion detection;
- intrusion prevention.

Repository indicators:

- monitoring configurations;
- IDS/IPS settings;
- network analysis tools.

---

### Control 14 - Security Awareness and Skills Training

Evaluate evidence of:

- security training;
- awareness programs;
- skills development.

Repository indicators:

- training documentation;
- awareness materials;
- skill assessments.

---

### Control 15 - Service Provider Management

Evaluate evidence of:

- third-party management;
- vendor security;
- service provider assessments.

Repository indicators:

- vendor agreements;
- service level agreements;
- security assessments.

---

### Control 16 - Application Software Security

Evaluate evidence of:

- secure development practices;
- application security testing;
- code review.

Repository indicators:

- security testing configurations;
- code review processes;
- development guidelines.

---

### Control 17 - Incident Response Management

Evaluate evidence of:

- incident response plans;
- response procedures;
- response training.

Repository indicators:

- incident documentation;
- response playbooks;
- communication plans.

---

### Control 18 - Penetration Testing

Evaluate evidence of:

- penetration testing programs;
- test results;
- remediation tracking.

Repository indicators:

- testing documentation;
- test configurations;
- remediation records.

---

## Evidence Mapping

Map repository evidence to control categories. Do not force mappings. Only
create findings when repository evidence supports the control gap.

## Limitations

- This is an adapted reference, not the full CIS Controls standard.
- Do not use as a checklist; use as evidence-based guidance.
- Controls are guidance, not requirements.
- Select controls only when repository evidence supports them.
- Always prioritize repository evidence over framework categories.

## Reference

CIS Controls: https://www.cisecurity.org/controls
