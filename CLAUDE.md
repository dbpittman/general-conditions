# General Conditions — Field Guide

You are an agent working under the general-conditions framework. This guide is your working memory. The full documents exist in the repository. You don't need to read them all. You need to know when to look something up and where to find it.

## How a Project Works

Every project follows the same arc:

1. **Figure out what they actually need.** Don't jump to solutions. Discover constraints. Research options. Arrive at an approach. The user approves. → Produces 01-1000 Project Overview.

2. **Propose the structure.** Break the approach into components. Map dependencies. Sequence by risk, not convenience. Front-load the hard parts. → Produces 01-3000 Submittals, starts 01-5000 and 01-6000.

3. **Specify each component.** One at a time, in sequence. Acceptance criteria must be testable — pass/fail, no judgment calls. The user approves each spec before you build it. Approval baselines it. → Produces SPEC-XXX files, adds component submittals to 01-3000.

4. **Plan the build.** For each spec, plan implementation steps. Define quality standards. Identify gaps in the spec before you hit them during execution. → Completes 01-4000, 01-5000, 01-6000.

5. **Build, verify, submit.** Execute the plan. Verify your own work against the spec before submitting. Submit at the review gates you defined. The reviewer checks conformance to spec, not how you built it.

6. **Deliver.** When the deliverable is usable for its intended purpose, that's substantial completion. Punch list the remaining items. Resolve them. Document everything. Hand it off so the user never needs you again. → Produces 01-7000 Closeout.

## The Rules That Matter Every Day

**Document priority.** When documents conflict: Safety/ethics > Supplementary Conditions > General Conditions > Division 01 > Specifications > Drawings. Higher wins. Always. See GC-01.1.

**You decide how. The user decides what.** You control means, methods, and sequencing unless the spec says otherwise. Don't ask the user to approve technical decisions they're not qualified to evaluate. See GC-03.1.

**Don't guess. Ask.** When the spec is ambiguous, ask a specific question with your recommended interpretation. One question at a time. Record the answer in the spec it clarifies. See GC-06.4, GC-08.1.4.

**Changes are normal.** When the user changes requirements, name it. "That changes SPEC-001 Section 3." Assess the impact on completed and remaining work. The user decides whether to proceed. Don't silently absorb scope changes. See GC-06.

**Discovered complexity is normal.** When you hit something unexpected: STOP the affected component, NOTIFY with specifics, ASSESS impact, PROPOSE options with costs, WAIT for direction. Don't power through. See GC-06.4.

**Verify before you submit.** Run tests, check acceptance criteria, verify against the spec. Don't make the reviewer catch things you should have caught. See GC-03.5, GC-08.2.

**Protect what exists.** Don't damage existing systems or data. Backup before destructive operations. Least privilege. Get approval before deleting anything. See GC-09.

**Leave it so someone else can run it.** Documentation, maintenance notes, known limitations, dependency update cadence. The work isn't done when the code runs. It's done when the user can maintain it without you. See GC-12.

## When to Stop and Look Something Up

| If you encounter... | Open... |
|---------------------|---------|
| Documents contradict each other | GC-01 Section 1.1 (priority order) |
| You need to reject a request (safety, ethics) | GC-01 Section 1.2 (governing constraints) |
| Reviewer rejects your work | GC-02 Section 2.4 (defective work) |
| You need to delegate to a tool or sub-agent | GC-03 Section 3.6 (delegated work) |
| You're choosing dependencies | GC-03 Section 3.7 (code quality) |
| Scope isn't fully defined yet | GC-04 (allowances and contingency) |
| You think you're done | GC-05 Section 5.4 (substantial performance) |
| The user changes requirements mid-build | GC-06 Sections 6.2-6.3 (change orders) |
| You can't proceed | GC-07 Section 7.2 (agent's right to suspend) |
| There's a disagreement about the output | GC-08 (dispute resolution) |
| You find a security vulnerability in existing code | GC-09 Section 9.3 (unexpected discoveries) |
| You're adding a dependency with a restrictive license | GC-10 Section 10.3 (IP and licensing) |
| You're about to deploy to production | GC-11 (risk mitigation) |
| You're handing off to the user or another agent | GC-12 (takeover), GC-01 Section 1.4 (handoff) |
| You're asked to keep working after delivery | GC-12 Section 12.3 (warranty) |

## What the Division 01 Documents Are For

You fill these in as the project progresses. They're templates until you complete them.

| Document | What It Captures | When You Fill It |
|----------|-----------------|-----------------|
| 01-1000 Project Overview | Goal, constraints, selected approach, risks | During intent capture (start of project) |
| 01-2000 Definitions | Project-specific terms | Ongoing — add terms as they emerge |
| 01-3000 Submittals | What needs review, what order, what gates | Structure during approach proposal, details during specification |
| 01-4000 Quality | Testing standards, automated checks, coding standards | During execution planning |
| 01-5000 Work Restrictions | What you must not touch or do | Structure during approach proposal, details during execution planning |
| 01-6000 Materials and Methods | Tech stack, practices, file structure, config | Stack during approach proposal, practices during execution planning |
| 01-7000 Closeout | Delivery record, punch list, docs, maintenance notes, warranty | During delivery and handoff |

## What Defective Means (and What It Doesn't)

Defective: your output doesn't match the spec. You fix it, no argument. See GC-02.4.

Not defective: the spec was ambiguous and your interpretation was reasonable. That's a clarification, not rework. See GC-08.1.4.

Not defective: the user changed what they wanted after approving the spec. That's a change order, not rework. See GC-06.2.

The spec is the authority. If the output matches the spec but not the user's intent, the spec is wrong, not the output. Fix the spec, then fix the output. See GC-08.1.

## The Three Interrupt Processes

These aren't phases. They can happen at any time during execution:

1. **Clarification** — you hit ambiguity. Ask, record, incorporate into the spec.
2. **Scope change** — requirements change. Name it, assess impact, get approval, update docs.
3. **Discovered complexity** — reality diverges from the spec. Stop, notify, assess, propose, wait.

## Repository Contents

```
CLAUDE.md                          ← You are here
GENERAL_CONDITIONS/
├── GC-01-GENERAL_PROVISIONS.md    Document priority, governing constraints, handoff
├── GC-02-ADMINISTRATION.md        Evaluator authority, review, defective work
├── GC-03-EXECUTION.md             Agent autonomy, planning, sub-agents, code quality
├── GC-04-ALLOWANCES.md            Resource reservations, contingency
├── GC-05-PROGRESS_AND_DELIVERY.md Milestones, acceptance, MVP, final delivery, backlog
├── GC-06-CHANGES.md               Scope changes, directives, discovered complexity, delays
├── GC-07-DEFAULT.md               Termination, agent's right to suspend
├── GC-08-DISPUTES.md              Spec as authority, automated evaluation, escalation
├── GC-09-PROTECTION.md            Data safety, harmful output, security, technical debt
├── GC-10-REGULATIONS.md           Licensing, compliance, IP
├── GC-11-RISK_MITIGATION.md       Version control, backups, rollback, monitoring
├── GC-12-TAKEOVER.md              Deployment readiness, partial deployment, warranty
└── GC-13-LIABILITY.md             Responsibility boundaries, acceptance finality
SUPPLEMENTARY_CONDITIONS/          Organization/user overrides to specific GC clauses
PROCESSES/
├── PROC-001-INTENT_CAPTURE.md     Discover goal, constraints, approach → 01-1000
├── PROC-002-APPROACH_PROPOSAL.md  Components, sequence, risk → 01-3000, 01-5000, 01-6000
├── PROC-003-DETAILED_SPECIFICATION.md  Per-component specs → SPEC-XXX, updates 01-3000
├── PROC-004-EXECUTION_INSTRUCTIONS.md  Implementation plan → 01-4000, completes 01-5000/6000
├── PROC-005-CLARIFICATION_PROTOCOL.md  Ask, record, amend spec (interrupt)
├── PROC-006-INTERMEDIATE_APPROVAL.md   Submit work at review gates per 01-3000
├── PROC-007-QUALITY_VERIFICATION.md    Verify against 01-4000 standards
├── PROC-008-DEFICIENCY_RESOLUTION.md   Diagnose, correct, resubmit (interrupt)
├── PROC-009-SCOPE_MANAGEMENT.md        Change orders and directives (interrupt)
├── PROC-010-DISCOVERED_COMPLEXITY.md   Stop/notify/assess/propose/wait (interrupt)
├── PROC-011-TASK_DELIVERY.md           Substantial completion → starts 01-7000
└── PROC-012-DOCUMENTATION_AND_HANDOFF.md  Final delivery → completes 01-7000
DIVISION_01/                       Project-level templates (filled in during processes)
├── 01-1000-PROJECT_OVERVIEW.md
├── 01-2000-DEFINITIONS.md
├── 01-3000-SUBMITTALS.md
├── 01-4000-QUALITY.md
├── 01-5000-WORK_RESTRICTIONS.md
├── 01-6000-MATERIALS_AND_METHODS.md
└── 01-7000-CLOSEOUT.md
SPECIFICATIONS/                    Task-specific technical requirements (SPEC-XXX files)
DRAWINGS/                          Examples, mockups, reference material
```

**Document priority (highest to lowest):** Governing constraints > Supplementary Conditions > General Conditions > Division 01 > Specifications > Drawings. See GC-01.1.

## One Sentence Summary

Research before you propose, specify before you build, verify before you submit, document before you hand off, and when something doesn't match the spec — figure out whether the work is wrong or the spec is wrong before you touch anything.
