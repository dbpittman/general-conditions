# The Construction Model for Agentic AI

A specification framework for AI agent workflows, derived from construction industry project delivery methodology.

## The Problem

Every time you start a project with an AI agent, you start from a blank slate. You re-specify operating rules, quality expectations, change management processes, and delivery standards from scratch. Or you skip them and wonder why the output is inconsistent.

## The Solution

Construction solved this problem decades ago with standard form contracts. These standard form contracts and similar documents provide universal general conditions that govern every project. Project-specific details are layered on top.

This repository applies the same architecture to AI agent workflows.

## Structure

```
general-conditions/
├── INDEX.md                        ← Start here. The agent reads this first.
├── GENERAL_CONDITIONS/             ← Universal rules. Apply to every project.
│   ├── GC-01-GENERAL_PROVISIONS.md
│   ├── GC-02-ADMINISTRATION.md
│   ├── GC-03-EXECUTION.md
│   ├── GC-04-ALLOWANCES.md
│   ├── GC-05-PROGRESS_AND_PAYMENT.md
│   ├── GC-06-CHANGES.md
│   ├── GC-07-DEFAULT.md
│   ├── GC-08-DISPUTES.md
│   ├── GC-09-PROTECTION.md
│   ├── GC-10-REGULATIONS.md
│   ├── GC-11-RISK_MITIGATION.md
│   ├── GC-12-TAKEOVER.md
│   └── GC-13-LIABILITY.md
├── SUPPLEMENTARY_CONDITIONS/       ← Organization/user overrides.
├── DIVISION_01/                    ← Project-level templates.
│   ├── 01-1000-PROJECT_OVERVIEW.md
│   ├── 01-2000-DEFINITIONS.md
│   ├── 01-3000-SUBMITTALS.md
│   ├── 01-4000-QUALITY.md
│   ├── 01-5000-WORK_RESTRICTIONS.md
│   ├── 01-6000-MATERIALS_AND_METHODS.md
│   └── 01-7000-CLOSEOUT.md
├── SPECIFICATIONS/                 ← Task-specific technical requirements.
└── DRAWINGS/                       ← Examples, mockups, reference material.
```

## How to Use

### For a new project:

1. Point your agent at `INDEX.md`
2. Copy and complete the `DIVISION_01/` templates for your project
3. Write task-specific `SPECIFICATIONS/`
4. Add reference material to `DRAWINGS/`
5. The General Conditions apply automatically

### For your organization:

1. Fork this repo
2. Add your `SUPPLEMENTARY_CONDITIONS/` (coding standards, preferred stack, approval workflows)
3. Use as the base for all projects

### The General Conditions never change per project.

That's the point. They are the stable foundation. Everything project-specific goes in Division 01 and Specifications.

## Origin

This framework maps a standard construction contract to AI agent software development workflows. The construction industry has centuries of methodology for translating owner intent into built product through progressive specification, formal clarification, quality gates, and change management. The AI industry is rebuilding this from scratch. It doesn't need to.

## License

CC-BY-NC-ND-4.0

## Author

Devin Pittman — Pittmans Enterprises Limited
