# Writing Plans

## Overview
Write comprehensive implementation plans assuming the engineer has zero context for our codebase. Document everything they need to know: files to touch, code, testing, docs.

**Announce at start:** "I'm using the writing-plans skill to create the implementation plan."

## Save plans to:
`docs/superpowers/plans/YYYY-MM-DD-<feature-name>.md`

## Plan Document Header
Every plan MUST start with this header:
```markdown
# [Feature Name] Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** [One sentence describing what this builds]
**Architecture:** [2-3 sentences about approach]
**Tech Stack:** [Key technologies/libraries]
```

## Task Structure
Each step is one action (2-5 minutes):
1. **RED:** Write the failing test.
2. **Verify RED.**
3. **GREEN:** Write minimal implementation.
4. **Verify GREEN.**
5. **Commit.**

## Execution Handoff
After saving the plan, offer execution choice:
1. **Subagent-Driven (recommended).**
2. **Inline Execution.**
