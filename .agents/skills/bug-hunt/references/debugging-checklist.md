# Debugging Checklist

## Problem definition
- What is the actual observed behavior?
- What is the expected behavior?
- Can the issue be narrowed to a specific route/component/service?

## Boundary isolation
- UI rendering
- Local state
- Derived state
- Form handling
- Async race/timing
- Validation/schema mismatch
- API transport
- Auth/permission logic
- Environment/config

## Common defect sources
- stale assumptions about data shape
- missing null handling
- effect dependency issues
- state not reset correctly
- loading/error path not handled
- incorrect conditional rendering
- client/server boundary misuse
- schema drift
- accidental breaking change in shared utility

## Fix quality
- Is this the root cause or a symptom patch?
- Is the fix minimal?
- Could the fix hide another issue?
- What adjacent behavior may be affected?