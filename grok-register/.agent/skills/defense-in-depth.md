# Defense in Depth

## Overview
After finding the root cause, add validation at multiple layers to prevent similar bugs in the future.

**Core principle:** One failure shouldn't crash the system. Validate assumptions at every boundary.

## Layers of Defense
1. **Input Validation:** Check parameters at the entry point.
2. **Logic Validation:** Check state before critical operations.
3. **Interface Validation:** Ensure external components return expected data.
4. **Environment Guards:** Verify configuration and environment variables.
