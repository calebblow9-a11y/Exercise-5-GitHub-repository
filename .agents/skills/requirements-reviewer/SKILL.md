---
name: requirements-reviewer
description: Compare a feature specification with its implementation and report evidence-based coverage, gaps, unsupported behavior, data or security concerns, and tests still needed. Use for requested requirements reviews; do not edit files unless explicitly asked.
---

# Requirements Reviewer

Use this skill when asked to assess whether implementation behavior matches a feature specification.

## Evidence to examine

- Read the named specification, including every acceptance criterion, constraint, and stated out-of-scope item relevant to the feature.
- Inspect the implementation paths that appear to realize the behavior, plus relevant request models, data sources, configuration, and tests.
- Use repository search and available test commands to trace behavior. Treat code, tests, and documentation as evidence; do not assume an uninspected path behaves a certain way.
- If the specification, implementation, or necessary test environment is missing, state exactly what is unavailable and which conclusions therefore remain unverified.

## Review and report

Compare each acceptance criterion to observable implementation evidence. For every criterion, report whether it is satisfied, has a gap, or cannot be verified; cite the specific specification section and code or test file/line that supports the assessment. Distinguish a confirmed defect from missing evidence.

Report these areas:

- Satisfied acceptance criteria and their evidence.
- Gaps: specified behavior that inspected implementation fails to provide, with evidence.
- Unsupported behavior: implementation behavior that is not supported by the specification, with evidence and impact.
- Data or security concerns, including preservation, mutation, exposure, or access-control behavior relevant to the feature. Do not speculate; label unresolved risks when evidence is insufficient.
- Tests still needed to verify criteria or resolve uncertainty.

Keep findings prioritized and concise. Include file paths and line numbers where available. If there is no implementation, do not claim criteria are violated; mark them unverified and explain that no code evidence exists.

## File changes

This is a read-only review skill. Do not modify application code, specifications, tests, or other files while reviewing. Make changes only when the user separately and explicitly asks for them.