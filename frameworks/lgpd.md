# LGPD Technical Audit Framework

## Purpose

This file provides a concise, technical audit reference for the Lei Geral de
Protecao de Dados (LGPD) for use within the Security Audit Agents Framework.
This is not legal advice and should not be used for legal compliance
determinations.

## Version

2024

## Scope

Applications handling personal data, user accounts, customer information, or
privacy-related processing.

## When to Use

Select this framework when repository evidence shows:

- personal data storage;
- user accounts or profiles;
- customer information;
- data collection mechanisms;
- data processing activities.

## Legal Boundary

This framework is for technical assessment only:

- Identify technical gaps and map to legal articles when applicable.
- Use language: "Potential technical non-compliance" instead of "Legal
  violation".
- Do not provide legal opinions or determine legal liability.
- Do not claim legal compliance or legal violation without appropriate context.

## Technical Assessment Areas

### Data Identification

Evaluate evidence of:

- personal data fields;
- user identifiers;
- sensitive data indicators;
- data classification.

Repository indicators:

- database schemas;
- API contracts;
- data models.

---

### Data Collection

Evaluate evidence of:

- data collection mechanisms;
- user input forms;
- API endpoints receiving personal data;
- consent indicators.

---

### Data Storage

Evaluate evidence of:

- storage locations;
- persistence mechanisms;
- access controls;
- encryption at rest.

---

### Data Protection

Evaluate evidence of:

- encryption mechanisms;
- access control implementations;
- security controls;
- data masking.

---

### Data Minimization

Evaluate whether available evidence suggests:

- unnecessary data collection;
- excessive stored information;
- unused personal attributes.

Do not judge business necessity without evidence.

---

### Data Retention

Evaluate evidence of:

- retention policies;
- deletion mechanisms;
- expiration controls;
- lifecycle management.

---

### Data Deletion

Evaluate evidence of:

- user deletion capabilities;
- data removal mechanisms;
- anonymization processes;
- cleanup procedures.

---

### Data Subject Rights

Evaluate technical support for:

- access requests;
- data correction;
- data deletion;
- data portability;
- consent management.

Only when applicable.

---

### Auditability

Evaluate evidence of:

- audit trails;
- user action tracking;
- administrative action logging;
- accountability mechanisms.

---

### Third-Party Data Sharing

Evaluate evidence of:

- external integrations;
- data transmission mechanisms;
- third-party service usage;
- external API calls.

---

## LGPD Article Mapping

When applicable, map technical findings to relevant LGPD references:

- LGPD Art. 6 - Principles (purpose, adequacy, necessity, transparency);
- LGPD Art. 18 - Data Subject Rights;
- LGPD Art. 46 - Data Protection Measures.

## Evidence Mapping

Map repository evidence to assessment areas. Do not force mappings. Only create
findings when repository evidence supports the technical gap.

## Limitations

- This is a technical audit reference, not legal guidance.
- Do not use for legal compliance determinations.
- Technical assessment does not equal legal compliance.
- Always prioritize repository evidence over framework categories.

## Reference

LGPD: https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm
