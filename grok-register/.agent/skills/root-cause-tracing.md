# Root Cause Tracing

## Overview
Bugs often manifest deep in the call stack. Your instinct is to fix where the error appears, but that's treating a symptom.

**Core principle:** Trace backward through the call chain until you find the original trigger, then fix at the source.

## The Tracing Process
1. **Observe the Symptom:** Note the exact error and location.
2. **Find Immediate Cause:** What code directly causes this?
3. **Ask: What Called This?** Trace back through the stack.
4. **Keep Tracing Up:** What value was passed? Where did it originate?
5. **Find Original Trigger:** Fix at the source, not at the symptom point.

## Adding Stack Traces
When you can't trace manually, add instrumentation:
```typescript
const stack = new Error().stack;
console.error('DEBUG:', { context, stack });
```

## Key Principle
```
NEVER fix just where the error appears. 
Trace back to find the original trigger.
```
