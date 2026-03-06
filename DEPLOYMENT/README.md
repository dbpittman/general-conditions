# Deployment

Operational deployment configuration for the General Conditions framework. This directory contains everything needed to run the framework as a multi-agent system using Claude Code.

## Architecture

Two Claude Code instances running in separate git worktrees, communicating via a shared project directory and `queue.json` task queue. The Owner watches both via tmux/ttyd browser sessions and can interact with either agent at any time.

```
┌─────────────────────┐         ┌─────────────────────────┐
│  Browser Window 1   │         │   Browser Window 2       │
│  ttyd :8080         │         │   ttyd :8081             │
│                     │         │                          │
│  PM Agent           │         │   Contractor Agent       │
│  (Claude Code)      │         │   (Claude Code)          │
│                     │         │                          │
│  Captures intent    │         │   Watches queue          │
│  Queues tasks       │  queue  │   Spawns Workers         │
│  Evaluates work ────┼── .json─┼── Produces deliverables  │
│  Presents to Owner  │         │   Updates status         │
│                     │         │                          │
│  Own worktree       │  shared │   Own worktree           │
│  Own CLAUDE.md      │  project│   Own CLAUDE.md          │
│                     │   dir   │   .claude/agents/worker  │
└─────────────────────┘         └─────────────────────────┘
         │                                  │
         └──────────┐    ┌──────────────────┘
                    ▼    ▼
              Shared Project Directory
              ├── queue.json
              ├── pm/direction/
              ├── pm/evaluation/
              ├── contractor/submittals/
              ├── DIVISION_01/
              ├── SPECIFICATIONS/
              └── DRAWINGS/
```

### Roles

| Role | Instance | Spawns | Produces | Evaluates |
|------|----------|--------|----------|-----------|
| Owner | Human | — | Decisions, approvals | — |
| PM Agent | Claude Code (worktree 1) | — | Direction files, evaluation files, queue tasks | Deliverables against specs and Owner intent |
| Contractor Agent | Claude Code (worktree 2) | Worker subagents | — (coordinates Workers) | Completeness only (not conformance) |
| Worker Agents | Subagents of Contractor | — | Division 01 docs, SPEC-XXX files, project artifacts | Self-verification only |

### Communication

- **PM → Contractor:** Tasks written to `queue.json` with priority. Direction files in `pm/direction/`.
- **Contractor → PM:** Task status updates in `queue.json`. Deliverables in `contractor/submittals/`.
- **PM → Owner:** Conversation in PM terminal session. Evaluated deliverables presented for approval.
- **Owner → Either Agent:** Direct interaction via either ttyd terminal session at any time.

## Contents

```
DEPLOYMENT/
├── README.md                          ← You are here
├── GC-OPERATIONAL.md                  ← Compressed governance (shared by all agents)
├── pm/
│   └── CLAUDE.md                      ← PM Agent configuration
├── contractor/
│   ├── CLAUDE.md                      ← Contractor Agent configuration
│   └── .claude/
│       └── agents/
│           └── worker.md              ← Worker subagent definition
└── templates/
    └── queue.json                     ← Empty queue template
```

## Prerequisites

- Claude Code installed
- tmux installed
- ttyd installed
- Git (for worktrees)

## Setup

```bash
# From the general-conditions repo root:

# 1. Create the shared project directory
mkdir ../my-project
mkdir -p ../my-project/pm/direction
mkdir -p ../my-project/pm/evaluation
mkdir -p ../my-project/contractor/submittals
mkdir -p ../my-project/DIVISION_01
mkdir -p ../my-project/SPECIFICATIONS
mkdir -p ../my-project/DRAWINGS
cp DEPLOYMENT/templates/queue.json ../my-project/queue.json

# 2. Create worktrees
git worktree add ../my-project-pm pm-branch
git worktree add ../my-project-contractor contractor-branch

# 3. Configure PM instance
cp DEPLOYMENT/pm/CLAUDE.md ../my-project-pm/CLAUDE.md
cp DEPLOYMENT/GC-OPERATIONAL.md ../my-project-pm/GC-OPERATIONAL.md

# 4. Configure Contractor instance
cp DEPLOYMENT/contractor/CLAUDE.md ../my-project-contractor/CLAUDE.md
cp -r DEPLOYMENT/contractor/.claude ../my-project-contractor/
cp DEPLOYMENT/GC-OPERATIONAL.md ../my-project-contractor/GC-OPERATIONAL.md

# 5. Start tmux sessions with ttyd
tmux new-session -d -s pm "cd ../my-project-pm && claude"
tmux new-session -d -s contractor "cd ../my-project-contractor && claude"
ttyd -p 8080 tmux attach -t pm &
ttyd -p 8081 tmux attach -t contractor &
```

Open two browser windows:
- **PM Agent:** `http://localhost:8080`
- **Contractor Agent:** `http://localhost:8081`

## Usage

1. **Talk to the PM.** Tell it what you want to build. The PM will capture your intent through conversational discovery (PROC-001).

2. **Watch the PM queue work.** When the PM has enough information, it writes direction files and queues tasks to `queue.json`.

3. **Watch the Contractor execute.** The Contractor picks up tasks, spawns Workers, and writes deliverables to disk.

4. **The PM evaluates.** Once a task is complete, the PM reads the deliverable, evaluates it, and presents it to you for approval.

5. **You approve or redirect.** Approved deliverables are promoted to the project directory. Rejected deliverables get correction tasks queued.

6. **The PM moves ahead.** While the Contractor works, the PM can continue the next process step with you — capturing more intent, framing the next specification, etc.

7. **Intervene anytime.** Type into either terminal to correct, redirect, ask questions, or provide information.

## Relationship to Full Framework

The General Conditions (GC-00 through GC-13) remain the authoritative specification. GC-OPERATIONAL.md is a compressed extract for context window efficiency. The full GC documents govern when there is any ambiguity.

The PROCESSES/ directory (PROC-001 through PROC-012) defines the detailed workflow. The PM Agent drives projects through this process arc.

## Status

This is a test deployment configuration being validated against real projects.
