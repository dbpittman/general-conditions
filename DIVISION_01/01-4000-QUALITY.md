# 01-4000 — Quality Requirements

> **Produced by:** PROC-004 (Execution Instructions), refined per component
>
> **Used by:** PROC-007 (Quality Verification) as the standard for evaluation
>
> **This is a template. The agent completes this document during PROC-004. It defines how quality is measured and verified.**
>
> Implements GC-02 (review and inspection) and GC-08 Section 8.2 (automated evaluation).

## Acceptance Criteria

<!-- Global acceptance criteria that apply across all components. Component-specific criteria live in each SPEC-XXX file produced by PROC-003. -->

### Functional Requirements
- [ ]

### Non-Functional Requirements
- **Performance:**
- **Security:**
- **Accessibility:**
- **Compatibility:**

## Testing Requirements

<!-- What testing is required? Defines the standard PROC-007 evaluates against. -->

| Type | Required | Standard |
|------|----------|----------|
| Unit tests | Yes / No | Coverage target: ___% |
| Integration tests | Yes / No | |
| End-to-end tests | Yes / No | |
| Manual testing | Yes / No | |
| Security review | Yes / No | |
| Performance testing | Yes / No | Target: ___ |

## Automated Evaluation

<!-- What automated checks must pass before submission? Per GC-08.2.3, the Agent runs these before every submittal (PROC-006). -->

- [ ] Linting passes (tool: ___)
- [ ] Type checking passes (tool: ___)
- [ ] Tests pass
- [ ] Build succeeds
- [ ] No known vulnerabilities in dependencies (tool: ___)

**Checks marked as acceptance criteria are dispositive per GC-08.2.2. All others are advisory.**

## Coding Standards

<!-- What standards apply? Referenced by PROC-007 during quality verification. -->

- Style guide:
- Naming conventions:
- Documentation requirements:
- Commit message format:

## Review Criteria

<!-- What does the Evaluator specifically look for during PROC-006 (Intermediate Approval)? -->

The Evaluator reviews for:

1. Conformance to the component specification (SPEC-XXX)
2. Conformance to coding standards above
3. Appropriate test coverage per testing requirements above
4. Documentation completeness
5. Security best practices per GC-09
