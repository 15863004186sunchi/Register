# Condition-Based Waiting

## Overview
Replace arbitrary timeouts with condition polling to make tests and async operations more reliable.

**Core principle:** Wait for the specific condition you need, not for a fixed amount of time.

## Guidelines
1. **Identify Condition:** What exactly are we waiting for? (e.g., file exists, element visible).
2. **Poll:** Check the condition in a loop.
3. **Timeout:** Set a reasonable maximum wait time.
4. **Fail:** If the condition isn't met within the timeout, throw a clear error.
