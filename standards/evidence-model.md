# Evidence Model

This file defines the canonical evidence rules used by all audit agents.

Repository artifacts are the audit source of truth. Conversation memory,
assumptions, unexecuted tests, external systems, and framework expectations are
not evidence unless they are represented in the repository or explicitly
provided as audit artifacts.

## Evidence Sources

Acceptable evidence may include:

- file paths;
- code references;
- configuration snippets;
- infrastructure definitions;
- dependency manifests;
- deployment manifests;
- tests and test configuration;
- CI/CD workflow definitions;
- documentation, runbooks, and architecture notes;
- generated audit artifacts from the current audit workspace.

## Evidence Classifications

### EVIDENCED

Direct repository or audit artifact evidence supports the statement.

Examples:

- implemented control in code;
- configuration value in a tracked file;
- documented procedure in repository documentation;
- workflow or manifest that defines the behavior being assessed.

### PARTIALLY_EVIDENCED

Some evidence exists, but it is incomplete, indirect, or not enough to confirm
the full control or issue.

Examples:

- documentation exists without implementation evidence;
- implementation exists without configuration or runtime evidence;
- one component is covered but similar in-scope components are not.

### NOT_EVIDENCED

No supporting evidence was identified in the repository or audit artifacts.

This does not prove the capability, control, or process does not exist outside
the repository. Word findings and assessments as evidence limitations, not as
absolute claims about external reality.

### NOT_APPLICABLE

The capability, control, component, data flow, or technology does not apply to
the audited scope.

The assessment must explain why it is out of scope.

### NOT_ASSESSED

The area was not assessed because available information, audit scope, or agent
assignment was insufficient.

Use this for domain-level or control-level assessment records. Do not use it as
a finding evidence classification unless a template explicitly allows it.

## Finding Evidence Requirements

Every finding must include evidence.

Evidence entries should identify:

- the source path or artifact name;
- the relevant component, configuration, or document section;
- the observed condition;
- any limitation in what the evidence can prove.

If evidence cannot be identified, do not create a finding. Record the area as
`NOT_EVIDENCED`, `NOT_ASSESSED`, or `NOT_APPLICABLE` in the appropriate
assessment section instead.

## Evidence Language

Use careful language:

- "The repository contains..."
- "No evidence was identified for..."
- "The available evidence suggests..."
- "This could be validated by..."

Avoid unsupported language:

- "The system has no..."
- "The organization does not..."
- "This is compliant..."
- "This violates the law..."
- "Testing confirmed..." unless testing was actually performed.

## Validation Rules

- Confirm each finding cites at least one repository or audit artifact source.
- Confirm evidence classifications use only the allowed values.
- Confirm absence of evidence is not stated as absence of capability.
- Confirm validation suggestions are clearly separate from executed validation.
