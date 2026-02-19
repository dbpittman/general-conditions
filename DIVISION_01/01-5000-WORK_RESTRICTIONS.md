# 01-5000 — Work Restrictions

> **Produced by:** PROC-002 (Approach Proposal) for project-level restrictions, refined by PROC-004 (Execution Instructions) per component
>
> **This is a template. The agent completes this document to define boundaries. It supplements GC-09 with project-specific restrictions.**

## Off-Limits Areas

<!-- What files, systems, databases, or services must the Agent not touch? Identified during PROC-002 when mapping dependencies and boundaries. -->

- Do not modify:
- Do not access:
- Do not delete:

## Restricted Operations

<!-- What operations require explicit approval before execution? Per GC-09 Section 9.1. Identified during PROC-004 when planning implementation steps that touch existing systems. -->

The following operations require User approval:

- [ ] Database schema changes
- [ ] Production deployments
- [ ] Deletion of any existing code or data
- [ ] Changes to authentication or authorization systems
- [ ] Changes to CI/CD pipelines
- [ ] External API integrations
- [ ] Changes to infrastructure configuration

## Prohibited Dependencies

<!-- Are there any libraries, frameworks, or services that must not be used? From PROC-001 hard constraints or PROC-002 approach decisions. -->

-

## Prohibited Approaches

<!-- Are there any technical approaches that are not acceptable? From PROC-001 hard constraints. -->

-

## Data Handling Restrictions

<!-- What are the rules for handling data in this project? Per GC-09.2 and GC-10.2. -->

- **Sensitive data:**
- **User data:**
- **Credentials:**
- **Logging restrictions:**

## Environment Restrictions

<!-- What are the boundaries of the execution environment? Identified during PROC-004. -->

- **Accessible environments:**
- **Production access:** Yes / No / Read-only
- **Network access:**
- **External service calls:**
