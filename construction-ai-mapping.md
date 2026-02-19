# Construction Contract → Agentic AI: Complete Mapping

*Mapping a Standard Construction Contract to AI Agent Software Development Workflows*

*Working Document — Draft v0.1*

Devin Pittman — Pittmans Enterprises Limited

February 2026

---

## How to Read This Document

This document takes the complete structure of a standard construction contract and maps every section to its equivalent in an AI agent software development workflow. The construction contract is the source framework. The AI mapping is the derived application.

Where a standard contract section has no direct AI equivalent, it is noted as such with an explanation. Where the AI equivalent extends beyond what construction addresses, that is also noted.

## Agreement Between Owner and Contractor

The Agreement is the core contract. It defines who the parties are, what the work is, what it costs, and how payment works. In AI terms, this is the project charter: the foundational understanding between the user and the agent before any work begins.

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| A-1 | The Work | Task Definition | What the agent is being asked to build or produce. Scope boundary. |
| A-2 | Agreements & Amendments | Context & Overrides | Prior conversations, memory, user preferences. What modifies the base operating rules. |
| A-3 | Contract Documents | Specification Stack | System prompt, project context, examples, reference materials. The complete set of documents the agent works from, in priority order. |
| A-4 | Contract Price | Resource Budget | Token limits, compute budget, time constraints, API costs. The agreed cost envelope. |
| A-5 | Payment | Progress Delivery | How and when intermediate outputs are delivered. Milestone-based, not all-at-end. |
| A-6 | Addresses for Notices | Communication Channels | Where outputs go. File paths, repos, APIs, chat interfaces. How user and agent communicate. |
| A-7 | Language of Contract | Output Format & Language | Programming language, natural language, file formats, encoding. The medium of the deliverable. |
| A-8 | Succession | Session Continuity | How context transfers between sessions, agents, or models. Memory, handoff protocols. |

## Definitions

Construction contracts define terms precisely because ambiguity costs money. AI agent systems suffer from exactly the same problem. The following maps construction contract defined terms to their AI equivalents.

| Construction Term | AI Term | Explanation |
|---|---|---|
| Change Directive | Priority Override | User directs a change mid-task without waiting for the agent to assess impact. The agent must comply and proceed, assessing cost/impact retroactively. |
| Change Order | Scope Amendment | A mutually acknowledged change to the task requirements, with both parties agreeing on the revised scope before proceeding. |
| Construction Equipment | Tooling & Infrastructure | The agent's tools: code interpreters, file systems, APIs, search, databases. Required for execution but not part of the deliverable. |
| Consultant | System Architect / Evaluator | The intermediary that designs the solution and evaluates conformance. Could be a separate model, an evaluation harness, or the user in a review role. |
| Contract | Project Agreement | The complete set of operating rules, specifications, and context governing this task. |
| Contract Documents | Specification Stack | All documents the agent references, in defined priority order: system prompt > user instructions > project context > examples > general knowledge. |
| Contract Price | Compute/Resource Budget | Total resources allocated: tokens, API calls, time, compute cycles. |
| Contract Time | Deadline / Time Budget | When the work must be complete. Session timeout, sprint deadline, or user-imposed time constraint. |
| Contractor | Agent / AI System | The party executing the work. |
| Drawings | Examples / Mockups / Reference Outputs | Visual or concrete representations of the intended result. Sample code, wireframes, screenshots, reference implementations. |
| Notice in Writing | Logged Communication | Any communication that is recorded and becomes part of the project record. Chat history, commit messages, documented decisions. |
| Owner | User / Operator | The party commissioning and receiving the work. |
| Other Contractor | Other Agents / Services | External systems the agent must coordinate with: other AI agents, microservices, human team members working on the same project. |
| Place of the Work | Execution Environment | Where the agent operates: local machine, cloud VM, container, sandbox. Defines what the agent has access to. |
| Product | Dependency / Library / Component | Third-party materials incorporated into the deliverable. NPM packages, APIs, datasets, pre-trained models. |
| Project | Project | The total undertaking, which may include multiple tasks and multiple agents. |
| Ready-for-Takeover | Deployment Ready | The work is substantially complete, tested, documented, and ready for the user to operate independently. |
| Shop Drawings | Implementation Plans / PRs | Detailed plans showing how the agent intends to implement a specific component. Submitted for review before execution. |
| Specifications | Requirements Document | Written description of what the deliverable must do, how it must perform, and what standards it must meet. |
| Subcontractor | Sub-Agent / Tool Chain | Other agents, models, or automated processes the primary agent delegates work to. |
| Substantial Performance | MVP / Functional Delivery | The work is sufficiently complete that the user can use it for its intended purpose, even if minor items remain. |
| Supplemental Instruction | Clarification Response | A response to an agent's question that does not change scope but clarifies intent. The AI equivalent of an RFI response. |
| Supplier | Data / Service Provider | External sources that provide inputs the agent incorporates: APIs, databases, web services. |
| Temporary Work | Scaffolding / Dev Tooling | Code, scripts, or configurations needed during development but not included in the final deliverable. Build scripts, test harnesses, mock servers. |
| Work | Deliverable | Everything the agent is required to produce, including documentation, tests, and supporting artifacts. |
| Working Day | Active Session | A period of active agent execution. Excludes idle time, waiting for user input, or rate-limited periods. |

## General Conditions

The General Conditions are the heart of a standard construction contract. They define how the project operates regardless of what is being built. This is the section that translates most directly to AI agent design, because it is entirely about process, not product.

### Part 1 — General Provisions

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 1.1 | Contract Documents | Specification Priority Order | Defines which document takes precedence when conflicts exist. In AI: system prompt > user message > project context > memory > training data. This is critical and almost never explicitly defined in AI systems. |
| GC 1.2 | Law of the Contract | Governing Constraints | The non-negotiable rules: safety guidelines, ethical constraints, platform policies, regulatory requirements. Overrides everything else. |
| GC 1.3 | Rights and Remedies | Fallback Behaviors | What happens when something goes wrong. Error handling, retry logic, graceful degradation, escalation to human. |
| GC 1.4 | Assignment | Agent Handoff Protocol | Rules for transferring a task from one agent/model to another. Context requirements, state preservation, continuity guarantees. |

### Part 2 — Administration

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 2.1 | Authority of the Consultant | Evaluator Authority | Who or what has authority to approve, reject, or direct changes to the agent's work. Defines the review chain. |
| GC 2.2 | Role of the Consultant | Evaluation Scope | What the evaluator reviews (design conformance) vs. what they don't (means and methods). The evaluator checks if output meets spec, not how the agent produced it. |
| GC 2.3 | Review and Inspection | Quality Gates | Defined checkpoints where output is reviewed against requirements. When they occur, what is evaluated, pass/fail criteria. |
| GC 2.4 | Defective Work | Failed Output Handling | What happens when output doesn't meet spec. Rejection, rework requirements, and the agent's obligation to correct without additional resource allocation. |

### Part 3 — Execution

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 3.1 | Control of the Work | Agent Autonomy Scope | The agent controls means, methods, and sequencing unless the spec dictates otherwise. The user defines what, the agent determines how. |
| GC 3.2 | Construction by Others | Multi-Agent Coordination | Rules for when multiple agents or humans are working on the same project. Interface boundaries, conflict resolution, shared resource management. |
| GC 3.3 | Temporary Work | Development Scaffolding | Agent is responsible for any temporary code, environments, or tooling needed during execution. These are not part of the deliverable. |
| GC 3.4 | Construction Schedule | Execution Plan | Agent provides a plan showing task sequencing, dependencies, and milestones before beginning work. Updated as work progresses. |
| GC 3.5 | Supervision | Agent Self-Monitoring | Agent must monitor its own execution quality and flag issues proactively rather than waiting for review to catch them. |
| GC 3.6 | Subcontractors & Suppliers | Sub-Agents & Dependencies | Agent is responsible for the quality of any tools, models, or services it delegates to. The user holds the primary agent accountable, not the sub-agent. |
| GC 3.7 | Labour and Products | Code Quality & Dependencies | All code must be fit for purpose. Dependencies must be current, licensed appropriately, and vetted. No deprecated or vulnerable packages. |
| GC 3.8 | Shop Drawings | Implementation Submittals | Before building a major component, agent submits a detailed implementation plan for review. Agent verifies plan against requirements before submitting. Reviewer checks design conformance only. |

### Part 4 — Allowances

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 4.1 | Cash Allowances | Resource Reservations | Budget set aside for items not yet fully specified. In AI: token/compute allocation for tasks whose scope will be determined during execution. Research phases, exploratory work. |
| GC 4.2 | Contingency Allowance | Error/Rework Budget | Resources reserved for corrections, rework, and unexpected complexity. Critical for realistic planning. |

### Part 5 — Payment

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 5.1 | Owner Financing Info | User Capacity Disclosure | User communicates their available resources, access levels, and constraints upfront. Agent should know what the user can and cannot do. |
| GC 5.2 | Applications for Payment | Progress Reports | Agent provides structured progress updates at defined intervals showing work completed, work remaining, and any issues. Not just output dumps. |
| GC 5.3 | Payment | Output Acceptance | User reviews progress delivery and formally accepts or rejects. Non-response within a defined period constitutes acceptance. |
| GC 5.4 | Substantial Performance | MVP Delivery | The point at which the deliverable is usable for its intended purpose even if punch list items remain. Triggers a different phase of the relationship. |
| GC 5.5 | Final Payment | Final Acceptance | All work complete, all deficiencies resolved, all documentation delivered. Project is formally closed. |
| GC 5.6 | Deferred Work | Backlog Items | Work that is deliberately deferred to a future phase. Must be explicitly documented and agreed upon, not silently dropped. |
| GC 5.7 | Non-conforming Work | Accepted Deviations | Output that doesn't meet spec but is accepted by the user at a reduced scope/cost. Documented acceptance of known shortcomings. |

### Part 6 — Changes in the Work

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 6.1 | Owner's Right to Make Changes | User Scope Authority | The user can change requirements at any point. This is a right, not an exception. The system must be designed to accommodate it. |
| GC 6.2 | Change Order | Agreed Scope Change | Both user and agent acknowledge the change, its impact on work completed, and the revised plan. Documented and versioned. |
| GC 6.3 | Change Directive | Directed Change | User directs a change and the agent must proceed immediately, even if impact assessment is incomplete. Assessment happens retroactively. |
| GC 6.4 | Concealed or Unknown Conditions | Discovered Complexity | The agent encounters something unexpected: an API behaves differently than documented, data is malformed, a dependency has breaking changes. The agent must notify the user and assess impact before proceeding. |
| GC 6.5 | Delays | Blocked Progress | Causes of delay categorized: user-caused (not responding to RFIs), external (API outages, rate limits), agent-caused (poor execution). Different causes have different remedies. |
| GC 6.6 | Claims for Change in Price | Resource Impact Assessment | When changes or discovered conditions affect resource requirements, the agent documents the impact and the user decides whether to proceed. |

### Part 7 — Default Notice

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 7.1 | Owner's Right to Terminate | Task Abort / Agent Replacement | User can terminate the agent's involvement at any point. Agent must leave work in a usable state with documentation of what was completed and what remains. |
| GC 7.2 | Contractor's Right to Suspend/Terminate | Agent Escalation / Refusal | The agent can flag that it cannot proceed: missing information, contradictory requirements, ethical constraints, technical impossibility. It must explain why and what would be needed to resume. |

### Part 8 — Dispute Resolution

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 8.1 | Authority of Consultant | Evaluator as First Arbiter | Disagreements between user intent and agent output are first assessed against the specification. The spec is the authority, not either party's interpretation. |
| GC 8.2 | Adjudication | Automated Evaluation | Fast, structured assessment of whether output meets spec. Rule-based checks, test suites, linting. Quick resolution without full review. |
| GC 8.3 | Negotiation, Mediation, Arbitration | Escalation Ladder | Progressive resolution: agent self-correction → user clarification → re-specification → alternative agent/approach → human intervention. |
| GC 8.4 | Retention of Rights | Preserved Options | Using one resolution path doesn't preclude others. User can accept partial output while disputing other parts. |

### Part 9 — Protection of Persons and Property

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 9.1 | Protection of Work & Property | Data & System Protection | Agent must not damage existing systems, data, or configurations. Backups before destructive operations. Principle of least privilege. |
| GC 9.2 | Toxic & Hazardous Substances | Harmful Output Prevention | Agent must not produce code that is malicious, insecure, or introduces vulnerabilities. Includes injection risks, data exposure, and destructive operations. |
| GC 9.3 | Artifacts and Fossils | Unexpected Discoveries | Agent encounters something unexpected in the codebase or data: security vulnerabilities, sensitive data, legacy issues. Must stop and notify rather than proceeding or ignoring. |
| GC 9.4 | Construction Safety | Execution Safety | Sandboxing, resource limits, timeout protections. The agent operates within safe boundaries to prevent runaway processes or unintended side effects. |
| GC 9.5 | Mould | Technical Debt | Conditions that develop over time and compromise the integrity of the work. Agent should identify and flag accumulating technical debt during execution. |

### Part 10 — Governing Regulations

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 10.1 | Taxes and Duties | Licensing & Compliance Costs | License fees for dependencies, API costs, regulatory compliance costs. Must be accounted for in the resource budget. |
| GC 10.2 | Laws, Notices, Permits | Platform Policies & Regulations | Agent must comply with applicable platform terms, API usage policies, data regulations (GDPR, PIPEDA), and industry standards. Agent notifies user of compliance requirements. |
| GC 10.3 | Patent Fees | IP & Licensing | Agent must respect intellectual property. Open source license compatibility, attribution requirements, copyright. Agent should flag potential IP issues. |
| GC 10.4 | Workers' Compensation | No direct equivalent | Construction-specific. However, the broader principle of protecting the people involved in the work translates to responsible AI use, operator wellbeing, and preventing overreliance. |

### Part 11 — Insurance

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 11.1 | Insurance | Risk Mitigation & Rollback | Version control, backups, undo capability, staging environments. The ability to recover from agent errors without catastrophic loss. Also: monitoring and alerting on agent actions in production. |

### Part 12 — Owner Takeover

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 12.1 | Ready-for-Takeover | Deployment Readiness | Conditions that must be met before the user takes ownership: tests passing, documentation complete, environment configured, no critical deficiencies, compliance verified. |
| GC 12.2 | Early Occupancy | Partial Deployment | User begins using part of the deliverable before all work is complete. Requires clear documentation of what is done vs. what remains. Responsibility shifts for the deployed portion. |
| GC 12.3 | Warranty | Post-Delivery Support Window | A defined period after delivery during which the agent will fix defects in its work at no additional cost. Distinguishes defects (agent's responsibility) from new requirements (new scope). |

### Part 13 — Indemnification and Waiver

| Ref | Construction | AI Equivalent | Notes |
|---|---|---|---|
| GC 13.1 | Indemnification | Liability Boundaries | What the agent is responsible for vs. what the user assumes risk for. Agent-generated code used in production: who owns the consequences? Must be explicitly defined. |
| GC 13.2 | Waiver of Claims | Acceptance Finality | After final acceptance, the scope for revisiting completed work is limited. Prevents endless rework cycles. Both parties accept the delivered state. |

## Key Insights from the Mapping

### The specification priority order is the most important missing piece

In construction, the General Conditions define exactly which document wins when documents conflict. No AI agent framework does this explicitly. When a system prompt contradicts user memory, which wins? When user preferences conflict with a project specification, what takes precedence? Defining this order would eliminate an enormous class of inconsistent agent behavior.

### The distinction between Change Orders and Change Directives matters

Construction distinguishes between agreed changes (Change Orders) and directed changes (Change Directives). In AI, every mid-task change is currently treated the same way. Some changes should trigger impact assessment before proceeding — similar to a Proposed Change Order. Others are urgent directives where the agent must act first and assess later. The system should know which is which.

### The agent's right to stop work is underappreciated

The General Conditions give the contractor the right to suspend or terminate. In AI, agents almost never refuse to proceed even when they should: contradictory requirements, missing critical information, or tasks that will clearly fail. An agent that flags "I cannot proceed because…" is more valuable than one that silently produces garbage.

### Discovered complexity is normal, not failure

The concealed conditions provision treats unexpected complexity as a standard project event with a defined process for handling it. In AI, when an agent discovers that a task is harder than expected, there is no process. The agent either struggles silently or the user gets frustrated. Construction's approach is better: notify, assess, decide, proceed.

### Closeout is not optional

The Ready-for-Takeover and Warranty provisions ensure that work is handed off in a state the owner can maintain. AI agents almost never do this. They produce output and the conversation ends. Documentation, maintenance guidance, and a defined support window would dramatically increase the usable value of agent output.

---

This mapping demonstrates that the standard construction contract structure translates almost entirely to AI agent workflows. The construction industry spent decades refining these processes. The AI industry is rebuilding them from scratch, poorly. The next step is to draft an actual AI General Conditions document using this mapping as the specification.
