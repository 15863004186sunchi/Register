# Test-Driven Development (TDD)

## Overview
Write the test first. Watch it fail. Write minimal code to pass.

**Core principle:** If you didn't watch the test fail, you don't know if it tests the right thing.

**Violating the letter of the rules is violating the spirit of the rules.**

## When to Use
**Always:**
- New features
- Bug fixes
- Refactoring
- Behavior changes

## The Iron Law
```
NO PRODUCTION CODE WITHOUT A FAILING TEST FIRST
```

Write code before the test? Delete it. Start over.

## Red-Green-Refactor

### RED - Write Failing Test
Write one minimal test showing what should happen.

### Verify RED - Watch It Fail
**MANDATORY. Never skip.**
Confirm test fails for the expected reason.

### GREEN - Minimal Code
Write simplest code to pass the test. Don't over-engineer.

### Verify GREEN - Watch It Pass
**MANDATORY.**
Confirm test passes and no other tests are broken.

### REFACTOR - Clean Up
After green only, remove duplication and improve names while staying green.

### Repeat
Next failing test for next feature.

## Red Flags - STOP and Start Over
- Code before test
- Test after implementation
- Test passes immediately
- Can't explain why test failed
- Using mocks to test implementation rather than behavior
