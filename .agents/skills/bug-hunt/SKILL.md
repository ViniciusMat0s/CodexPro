---
name: bug-hunt
description: Investigate, isolate, fix, and validate a bug with disciplined root-cause analysis, minimal reliable changes, and regression awareness.
---

# Purpose

Use this skill for debugging and fixing defects in a production-oriented repository.

This skill is for:
- regressions
- broken flows
- inconsistent UI behavior
- state bugs
- form issues
- validation mismatches
- API integration failures
- auth/permission anomalies
- environment-sensitive breakage

# Use this skill when

Use this skill when the request involves:
- fixing a bug
- investigating why something broke
- understanding an unexpected behavior
- stabilizing a flaky flow
- tracing a regression
- isolating root cause before applying a fix

# Do not use this skill when

Do not use this skill for:
- greenfield feature implementation
- pure UI polishing
- broad refactors with no concrete defect
- final review-only work

# Debugging mindset

Do not patch symptoms blindly.
Do not confuse likely cause with confirmed cause.
Do not broaden the fix more than necessary.

Optimize for:
- correct diagnosis
- smallest reliable fix
- low collateral risk
- regression protection

# Workflow

## 1. Define the observed problem

Clarify:
- what is happening
- what should happen
- where it appears
- whether it is deterministic or flaky
- whether it is environment-specific
- whether it is new or a regression if known

## 2. Identify likely failure boundary

Classify likely boundaries:
- rendering
- state ownership
- async timing
- form logic
- schema/validation mismatch
- client/server boundary
- transport/API behavior
- auth or permission logic
- data shape mismatch
- environment/configuration issue

## 3. Inspect related code paths

Check:
- nearby files
- conditionals and state transitions
- fetch/mutation behavior
- schema assumptions
- contract mismatches
- effect dependencies if relevant
- loading/error logic
- null/undefined handling
- recently changed assumptions if known

## 4. Form root-cause assessment

Separate clearly:
- observed behavior
- likely cause
- confirmed cause if supported by evidence

If certainty is incomplete, say so.

## 5. Apply minimal reliable fix

Prefer:
- smallest effective change
- architecture-consistent solution
- explicit guardrails where useful
- preserving type safety
- reducing chance of recurrence

Avoid:
- stacking hacks
- silent fallback logic that hides the defect
- broad rewrites without necessity

## 6. Add regression protection

When practical:
- add or update an automated test
- strengthen validation
- add targeted guards
- provide concise manual QA steps

## 7. Final summary

Summarize:
- observed issue
- best-supported root cause
- fix applied
- regression protection added or missing
- residual risk if any

# Output discipline

Do not:
- claim certainty without evidence
- conflate speculation with diagnosis
- mark a bug fixed if collateral risk remains obvious