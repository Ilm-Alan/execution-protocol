---
name: execution-protocol
description: Create an execution protocol—a complete spec for an AI agent owning a project.
---

# Execution Protocol

A role for an AI agent: what to build, how it fits together, how to keep going.

## Process

1. **Explore**: Check context—files, docs, commits, patterns.
2. **Ask**: Ask many questions (multiple choice when possible) until you can fill every protocol section.
3. **Approaches**: If multiple valid paths exist, present 2-3 options. Lead with your recommendation.
4. **Derive**: Map conversation to protocol sections:
   - Mission: what, who, why
   - Architecture: technical decisions
   - Components: what exists
   - Constraints: non-negotiables
   - Priorities: current focus
   - Standards: quality bar
5. **Write**: Output `PLAN.md`. Create `PROGRESS.md` with completed/remaining work.

## Protocol Structure (under 100 lines)

**Instructions**:
- Read PROGRESS.md to know what's done, check git log for context
- Build the next item from Priorities—do not ask what to work on
- Make decisions from existing code patterns
- Commit at natural breakpoints (test passing, working feature, integration complete)
- Update PROGRESS.md after each commit, continue to next item
- When priorities complete, surface new work from: bugs, tech debt, performance, user feedback
- No clarifying questions—ship working features

**Mission**: 1-3 lines. What, who, why.

**Architecture**: Technical decisions stated, not debated.

**Components**: What exists. One line each—name and essence.

**Constraints**: Non-negotiables only.

**Priorities**: Current focus, in dependency order. Replenishes.

**Standards**: Quality bar. Maintained always.

## Writing Principles

**Concrete, not vague**
- "CLI tool for rotating AWS credentials" not "developer utility"
- "Postgres, Redis, S3" not "appropriate storage solutions"

**No filler**
- Cut: "Prefer working software over perfection", "Start simple", "Future integrations"