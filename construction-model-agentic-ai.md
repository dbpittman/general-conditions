# The Construction Model for Agentic AI

*A Framework for Progressive Specification and Quality Assurance in AI Agent Design*

**DRAFT v0.3**

Devin Pittman — Pittmans Enterprises Limited

February 2026

---

## Abstract

The AI industry has a specification problem. Users struggle to communicate intent to AI agents, agents struggle to produce intended output, and the resulting feedback loop is ad hoc at best. This is not a new problem. The construction industry has spent centuries developing a rigorous methodology for translating an owner's intent into a built product through progressive specification, formal clarification mechanisms, quality inspections, and change management. This paper proposes that the construction project delivery model—from schematic design through substantial completion—provides a proven, directly applicable framework for designing, operating, and evaluating agentic AI systems.

Specifically, this paper identifies the specification priority order—the rule that determines which document governs when documents conflict—as the single most important missing piece in current AI agent design. No existing framework defines this explicitly. Construction has required it for decades.

## 1. The Problem

Agentic AI is at an inflection point. Large language models can now use tools, write and execute code, manage files, search the web, and chain complex tasks together. The bottleneck is no longer capability—it is specification. Users cannot reliably communicate what they want, and agents cannot reliably determine what users mean.

The current approach to this problem is "prompt engineering"—essentially, writing better instructions. This is necessary but insufficient. It treats each interaction as an isolated specification exercise without any surrounding process architecture. It is the equivalent of an owner handing a contractor a napkin sketch and expecting a building.

The result is predictable: rework, frustration, abandoned tasks, and a widespread perception that AI agents are unreliable. The problem is not the agent. The problem is the absence of a delivery methodology.

Five specific failures recur across agent implementations:

- **No defined priority order when instructions conflict.** When a system prompt contradicts user memory, or user preferences conflict with a project specification, agents behave inconsistently because no framework tells them which document wins.

- **No distinction between agreed changes and directed changes.** Every mid-task scope change is treated identically. Some should trigger impact assessment before proceeding; others are urgent directives where the agent must act first and assess later.

- **No agent right to stop work.** Agents almost never refuse to proceed, even when they should: contradictory requirements, missing critical information, or tasks that will clearly fail. An agent that flags "I cannot proceed because…" is more valuable than one that silently produces garbage.

- **No process for discovered complexity.** When an agent discovers that a task is harder than expected—an API behaves differently than documented, data is malformed, a dependency has breaking changes—there is no standard process. The agent either struggles silently or the user gets frustrated.

- **No closeout.** Agents produce output and the conversation ends. Documentation, maintenance guidance, and a defined support window would dramatically increase the usable value of agent output.

## 2. Why Construction

Construction is the original complex project delivery discipline. It shares several critical characteristics with agentic AI task execution:

- The owner (user) has intent but cannot fully specify it upfront.
- The builder (agent) has capability but needs progressive clarification.
- A design intermediary (prompt/system architecture) translates between the two.
- Perfect specification is impossible; the process must accommodate ambiguity.
- Scope changes during execution are inevitable, not exceptional.
- Quality must be verified at checkpoints, not only at final delivery.

Construction does not pretend to solve the specification problem. Instead, it builds an entire system of progressive elaboration, formal clarification, approvals, and accountability around the acknowledgment that specifications are always incomplete. This is the insight the AI industry is missing.

The standard-form construction contract provides universal General Conditions that govern every project regardless of what is being built. Project-specific details are layered on top. The General Conditions never change per project. That stability is the foundation that makes the system work.

## 3. The Core Insight: Specification Priority Order

The most important provision in any construction contract is the document priority clause. It defines exactly which document governs when documents conflict. In a standard construction contract, this is typically the first provision in the General Conditions.

No AI agent framework does this explicitly.

When a system prompt contradicts user memory, which wins? When user preferences conflict with a project specification, what takes precedence? When an example shows one thing and the written requirements say another, which governs? These questions arise constantly in agent operation, and the answer is currently ad hoc—determined by whatever the model happens to prioritize in context.

Construction's answer is a defined hierarchy:

1. Governing Constraints (safety, ethics, laws—non-negotiable, override everything)
2. Supplementary Conditions (organization-specific overrides)
3. General Conditions (universal operating rules)
4. Division 01 — General Requirements (project-level administration)
5. Specifications (task-specific technical requirements)
6. Drawings / Examples / Reference Material

This hierarchy eliminates an enormous class of inconsistent agent behavior. It is not a suggestion—it is a rule. When documents conflict, the higher-priority document governs. Period.

The AI equivalent maps directly:

1. Platform safety guidelines and ethical constraints (non-negotiable)
2. Organization or user-level overrides (coding standards, preferred stack)
3. Universal agent operating rules (change management, quality gates, clarification protocols)
4. Project-level requirements (timeline, tech stack, access restrictions)
5. Task-specific requirements (what to build, acceptance criteria)
6. Examples, mockups, reference implementations

Defining this order would resolve conflicts that currently produce unpredictable agent behavior. It is a structural fix, not a prompting fix.

## 4. The Framework: Construction Phases Mapped to AI Agent Workflow

The following maps standard construction project delivery phases to equivalent stages in an agentic AI task lifecycle.

### 4.1 Pre-Design → Intent Capture

In construction, pre-design documents the owner's requirements: what the building needs to do, who will use it, what constraints exist. It does not describe the physical asset. It describes the problem.

In AI, the equivalent is capturing user intent before any work begins. This is not a prompt. It is a structured understanding of what the user is trying to accomplish, what constraints they have, what quality means to them, and what they already know. Most AI interactions skip this phase entirely, jumping straight to execution.

### 4.2 Conceptual Design → Approach Proposal

In construction, conceptual design establishes the broad approach: layout, major systems, appearance. The owner reviews and approves before investing in detail.

In AI, this is the agent proposing an approach before executing. Outlining the structure of a document before writing it. Describing the architecture of a solution before coding it. This is a mandatory gate, not an optional nicety.

### 4.3 Design Development → Detailed Specification

Design development refines the approved concept into specific systems, materials, and details. It is iterative. The designer and owner go back and forth to resolve how the broad approach will be implemented.

In AI, this is the elaboration of the approved approach into specifics: the function signatures and data models for a coding task, the section-by-section outline for a document. The agent elaborates and seeks user confirmation on key decisions before proceeding to execution.

### 4.4 Construction Documents → Execution Instructions

Construction documents are the fully detailed instructions from which the project is built. In practice, they are never truly complete—which is why RFIs exist.

In AI, this is the fully elaborated system prompt, tool configuration, and context the agent uses to execute. The parallel is important: just as construction documents are never perfect, the execution instructions for an AI agent will always have gaps. The system must accommodate this.

### 4.5 RFIs → Clarification Protocol

The Request for Information is construction's formal mechanism for handling ambiguity. When the contractor encounters something unclear, they submit an RFI rather than guessing. The response becomes part of the project record.

This is a critical concept missing from current AI agent design. When an agent encounters ambiguity, it should have a formal, structured mechanism to ask for clarification rather than guessing or hallucinating. The clarification and its response should be recorded and become part of the task context.

### 4.6 Submittals → Intermediate Approval

Before installing materials, the contractor submits product data, samples, and shop drawings for architect approval. This catches errors before they are built into the project.

In AI, this is the agent presenting intermediate outputs for user review before proceeding. The key principle is that review happens at intermediate stages, not only at final delivery. Complex tasks should be decomposed into stages with user review gates between them.

### 4.7 Inspections → Quality Verification

Construction inspections verify that work meets specifications at defined milestones. They are performed by parties other than the builder.

In AI, this maps to evaluation and testing of agent output against defined criteria. The critical principle from construction is that the builder does not inspect their own work. Evaluation should be separated from generation—a separate model call, a rule-based check, or user review.

### 4.8 Deficiency List → Deficiency Resolution

The deficiency list is a systematic inventory of items that do not meet specifications, compiled near the end of the project. It is specific, itemized, and tied to the original specification.

In AI, this is structured feedback on agent output that is specific, actionable, and traceable to the original requirements. Most AI feedback is either thumbs up/down or unstructured natural language. The deficiency list model demands specificity: what is wrong, what specification it violates, and what the expected result should be.

### 4.9 Change Orders → Scope Management

When the owner wants to change something after construction has begun, a change order documents the change, its impact on cost and schedule, and requires formal approval. Construction distinguishes between two types:

**Change Orders** are agreed changes. Both parties acknowledge the change, its impact, and the revised plan before proceeding.

**Change Directives** are directed changes. The owner instructs the contractor to proceed immediately, even if impact assessment is incomplete. Assessment happens retroactively.

In AI, every mid-task change is currently treated identically. This distinction matters. Some changes should trigger a pause for impact assessment: "Actually, let's rebuild this as a microservice instead." Others are urgent directives where the agent must act first: "Stop—the API endpoint changed, use this one instead." The system should know which is which.

### 4.10 Concealed Conditions → Discovered Complexity

In construction, when a contractor opens a wall and finds unexpected conditions—rot, asbestos, structural deficiencies—the standard contract defines the process: stop, notify, assess, propose options, wait for direction. The contractor does not silently work around the problem, guess at the solution, or abandon the project.

In AI, the equivalent happens constantly. An API behaves differently than documented. Data is malformed. A dependency has undisclosed breaking changes. Currently, there is no standard process for handling these discoveries. The construction model provides one:

1. Stop work on the affected component (not the entire project).
2. Notify the user with specific details about what was discovered.
3. Assess the impact on scope, timeline, and approach.
4. Propose options: workaround, alternative approach, scope reduction, or additional resources.
5. Wait for user direction before proceeding on the affected component.

Discovered complexity is a normal project event, not a failure. The process exists because specifications are never complete.

### 4.11 Substantial Completion → Task Delivery

Substantial completion in construction means the building can be occupied for its intended purpose, even if minor items remain. It triggers a different phase of the relationship: the owner begins using the building, and remaining items become a punch list.

In AI, this is the MVP: the deliverable is usable for its intended purpose even if polish items remain. The distinction between "substantially complete" and "finally complete" is important because it prevents the perfect from being the enemy of the good.

### 4.12 Closeout → Documentation and Handoff

Construction closeout requires the contractor to deliver as-built drawings, operation manuals, warranties, and maintenance guidance. The work is not done when the building is standing—it is done when the owner can operate it independently.

AI agents almost never do this. They produce output and the conversation ends. A defined closeout process—documentation, known limitations, maintenance notes, a warranty period for defect correction—would dramatically increase the usable value of agent output.

## 5. Summary Mapping

| Construction Phase | AI Agent Equivalent | Key Principle |
|---|---|---|
| Pre-Design | Intent Capture | Define the problem before the solution |
| Conceptual Design | Approach Proposal | Confirm direction before investing in detail |
| Design Development | Detailed Specification | Elaborate iteratively with user input |
| Construction Documents | Execution Instructions | Living specification, never truly complete |
| RFI | Clarification Protocol | Ask, don't guess; log the answer |
| Submittals | Intermediate Approval | Review at stages, not just at delivery |
| Inspections | Quality Verification | Separate evaluation from generation |
| Deficiency List | Deficiency Resolution | Specific, actionable, traceable feedback |
| Change Orders | Scope Management | Acknowledge change; assess impact |
| Substantial Completion | Task Delivery (MVP) | Complete enough to use; known items remain |
| Closeout | Documentation & Handoff | Record what was done and why |

## 6. What This Changes in Practice

Applying this framework produces several concrete shifts in how agentic AI is designed and operated.

### 6.1 From Prompt Engineering to Process Architecture

The focus shifts from writing better prompts to designing better workflows. The prompt is one artifact within a larger delivery process, not the process itself. A system prompt is a construction document—necessary but never sufficient without the surrounding process architecture of clarifications, submittals, inspections, and change management.

### 6.2 From Single-Shot to Phased Delivery

Complex tasks are decomposed into phases with defined gates. The agent does not disappear for an hour and return with a finished product. It engages the user at structured checkpoints. The gate structure is not bureaucracy—it is the mechanism that catches errors before they compound.

### 6.3 From Guessing to Asking

Agents are given an explicit, structured mechanism for clarification that is distinct from their conversational interface. The cost of asking is lower than the cost of rework. Construction proved this decades ago with the RFI process: a contractor who asks a question costs the project hours; a contractor who guesses wrong costs the project weeks.

### 6.4 From Binary Feedback to Structured Deficiency Tracking

User feedback becomes specific and tied to requirements, not general satisfaction. "This doesn't look right" becomes "Section 3.2 of the specification required pagination; the output does not paginate." This makes iteration converge faster because both parties know exactly what needs to change.

### 6.5 From Start-Over to Change Management

Mid-task changes are handled through an explicit process rather than by restarting or producing inconsistent output. The agent acknowledges the change, assesses impact on completed work, and confirms the new direction before proceeding. The distinction between Change Orders (agreed changes) and Change Directives (directed changes) prevents both unnecessary delays and unexamined scope creep.

### 6.6 From Disposable Output to Maintained Deliverables

The closeout and warranty provisions mean agent output is not disposable. It is a deliverable with documentation, known limitations, and a defined period during which defects are the agent's responsibility. This changes the incentive structure: the agent has reason to build something maintainable, not just something that passes the immediate test.

## 7. The General Conditions: What Was Built

To validate this framework, a complete set of General Conditions was drafted as an operational specification for AI agent workflows. These 13 sections map directly from the standard construction contract structure:

| Section | Subject | Construction Origin |
|---|---|---|
| GC-01 | General Provisions | Document priority, governing constraints, assignment |
| GC-02 | Administration | Evaluator authority, review and inspection, defective work |
| GC-03 | Execution | Agent autonomy, scheduling, subcontractors, code quality |
| GC-04 | Allowances | Resource reservations, contingency |
| GC-05 | Progress and Delivery | Milestones, acceptance, MVP, final delivery, backlog |
| GC-06 | Changes | Scope changes, directives, discovered complexity, delays |
| GC-07 | Default and Termination | Task abort, agent refusal, suspension |
| GC-08 | Dispute Resolution | Specification as authority, escalation ladder |
| GC-09 | Protection | Data safety, harmful output, security, technical debt |
| GC-10 | Regulations | Licensing, compliance, IP |
| GC-11 | Risk Mitigation | Version control, backups, rollback, monitoring |
| GC-12 | Takeover and Warranty | Deployment readiness, partial deployment, warranty period |
| GC-13 | Liability and Acceptance | Responsibility boundaries, acceptance finality |

These General Conditions are supplemented by Division 01 templates (project-level requirements), a Specifications directory (task-level technical requirements), and a Drawings directory (examples and reference material). The complete framework is available as a public repository.

## 8. Limitations

This framework is an analogy, and analogies break. Several important differences between construction and AI must be acknowledged.

**Rework cost is asymmetric.** Tearing down a wall is expensive. Regenerating a response is nearly free. This changes the economic calculus of quality gates—some gates that are essential in construction may be unnecessary overhead in AI. The framework must be calibrated so that process cost does not exceed rework cost.

**Iteration speed is different.** Construction phases take weeks or months. AI phases could take seconds. The framework must be adapted for speed without losing rigor. Not every gate needs to be a blocking review—some can be self-certified by the agent.

**Scale varies enormously.** Not every AI task needs a full phased delivery. A simple question needs none of this. The framework applies to complex, multi-step agentic tasks where the cost of failure justifies the cost of process.

**The roles are collapsed.** In construction, owner, designer, contractor, and inspector are different entities with different incentives. In most AI interactions, the user and agent play all roles. This reduces some benefits of the framework—particularly the separation of evaluation from generation—though multi-agent architectures restore this separation.

**Operator wellbeing is unaddressed.** Construction contracts include provisions for worker safety and compensation. The AI equivalent—preventing operator overreliance on AI systems, managing cognitive load, and maintaining human judgment in critical decisions—is an emerging concern that this framework does not yet address but should.

These limitations are real but do not invalidate the core insight: a process architecture for managing specification ambiguity is more valuable than better specifications alone.

## 9. Next Steps

This paper establishes the conceptual framework and describes an initial implementation. The following work is needed to make it operational:

1. Build a reference implementation that applies the General Conditions to a real agent workflow—code generation, document creation, or data analysis—and measure whether phased delivery produces better outcomes than single-shot prompting for complex work.

2. Define task complexity tiers that determine which phases and gates are required. The framework should scale from lightweight (simple tasks, self-certified gates) to full phased delivery (complex multi-step tasks, mandatory review at every gate).

3. Design the clarification protocol as a structured data format, not just conversational back-and-forth. An RFI should be a first-class object in the agent's context, not a chat message that gets lost in history.

4. Develop tooling that implements the framework as middleware or agent orchestration logic. The General Conditions should be enforceable by the system, not just advisory to the agent.

5. Test adversarially. The highest-value behavioral change to validate is GC-06 Section 6.4 (Discovered Complexity): does the STOP → NOTIFY → ASSESS → PROPOSE → WAIT protocol actually produce better outcomes than the current pattern of silent workarounds?

The construction industry did not solve the specification problem. It built a system that works despite the specification problem. That system is available. The AI industry should use it.
