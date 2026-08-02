# NIST Cybersecurity Framework

## Purpose

This file provides a concise, audit-oriented adaptation of the NIST
Cybersecurity Framework (CSF) for use within the Security Audit Agents
Framework. It is not a replacement for the original standard.

## Version

2.0

## Scope

Enterprise systems, service platforms, infrastructure projects, and hybrid
projects requiring security governance and lifecycle assessment.

## When to Use

Select this framework when repository evidence or audit objective supports:

- enterprise security maturity assessment;
- governance relevance;
- security lifecycle assessment;
- risk management evaluation.

## Framework Functions

### Identify (ID)

Evaluate evidence of:

- asset management;
- risk assessment;
- governance;
- supply chain risk management.

Repository indicators:

- documentation;
- dependency manifests;
- architecture documents;
- risk registers.

---

### Protect (PR)

Evaluate evidence of:

- identity management;
- access control;
- awareness and training;
- data security;
- platform security;
- technology infrastructure resilience.

Repository indicators:

- authentication mechanisms;
- access control implementations;
- encryption usage;
- security configurations.

---

### Detect (DE)

Evaluate evidence of:

- continuous monitoring;
- adverse event analysis.

Repository indicators:

- logging configurations;
- monitoring tools;
- alerting mechanisms;
- security event handling.

---

### Respond (RS)

Evaluate evidence of:

- response planning;
- communications;
- analysis;
- mitigation;
- improvements.

Repository indicators:

- incident response documentation;
- response procedures;
- communication plans.

---

### Recover (RC)

Evaluate evidence of:

- recovery planning;
- improvements;
- communications.

Repository indicators:

- recovery procedures;
- backup configurations;
- business continuity documentation.

---

## Implementation Tiers

### Tier 1 - Partial

Ad hoc and reactive risk management.

---

### Tier 2 - Risk Informed

Risk management practices are approved but may not be established.

---

### Tier 3 - Repeatable

Formal policies and procedures are updated regularly.

---

### Tier 4 - Adaptive

Adaptable practices based on lessons learned and predictive indicators.

---

## Evidence Mapping

Map repository evidence to framework functions. Do not force mappings. Only
create findings when repository evidence supports the control gap.

## Limitations

- This is a high-level reference, not the full NIST CSF standard.
- Do not use as a checklist; use as evidence-based guidance.
- Implementation tiers are guidance, not requirements.
- Do not force maturity assessment if governance is outside scope.
- Always prioritize repository evidence over framework categories.

## Reference

NIST CSF: https://www.nist.gov/cyberframework
