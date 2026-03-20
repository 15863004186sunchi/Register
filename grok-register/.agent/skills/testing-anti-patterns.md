# Testing Anti-Patterns

## Overview
Tests must verify real behavior, not mock behavior. Mocks are a means to isolate, not the thing being tested.

## The Iron Laws
1. **NEVER test mock behavior.**
2. **NEVER add test-only methods to production classes.**
3. **NEVER mock without understanding dependencies.**

## Anti-Patterns
1. **Testing Mock Behavior:** Asserting that a mock element exists rather than testing real UI behavior.
2. **Test-Only Methods:** Adding `destroy()` or `cleanup()` to production classes just for tests.
3. **Mocking Without Understanding:** Over-mocking can break the actual behavior you're trying to test.
4. **Incomplete Mocks:** Partial mocks can fail silently when code depends on omitted fields.

## The Bottom Line
**Mocks are tools to isolate, not things to test.**
If TDD reveals you're testing mock behavior, you've gone wrong.
