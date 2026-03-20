# Systematic Debugging

## Overview
Random fixes waste time and create new bugs. Quick patches mask underlying issues.

**Core principle:** ALWAYS find root cause before attempting fixes. Symptom fixes are failure.

**Violating the letter of this process is violating the spirit of debugging.**

## The Iron Law
```
NO FIXES WITHOUT ROOT CAUSE INVESTIGATION FIRST
```

If you haven't completed Phase 1, you cannot propose fixes.

## When to Use
Use for ANY technical issue:
- Test failures
- Bugs in production
- Unexpected behavior
- Performance problems
- Build failures
- Integration issues

**Use this ESPECIALLY when:**
- Under time pressure (emergencies make guessing tempting)
- "Just one quick fix" seems obvious
- You've already tried multiple fixes
- Previous fix didn't work
- You don't fully understand the issue

## The Four Phases
You MUST complete each phase before proceeding to the next.

### Phase 1: Root Cause Investigation
**BEFORE attempting ANY fix:**

1. **Read Error Messages Carefully**
2. **Reproduce Consistently**
3. **Check Recent Changes**
4. **Gather Evidence in Multi-Component Systems**
5. **Trace Data Flow** (See root-cause-tracing.md)

### Phase 2: Pattern Analysis
**Find the pattern before fixing:**

1. **Find Working Examples**
2. **Compare Against References**
3. **Identify Differences**
4. **Understand Dependencies**

### Phase 3: Hypothesis and Testing
**Scientific method:**

1. **Form Single Hypothesis**
2. **Test Minimally**
3. **Verify Before Continuing**
4. **When You Don't Know, Research More**

### Phase 4: Implementation
**Fix the root cause, not the symptom:**

1. **Create Failing Test Case**
2. **Implement Single Fix**
3. **Verify Fix**
4. **If Fix Doesn't Work, Stop and Re-analyze**
5. **If 3+ Fixes Failed: Question Architecture**
