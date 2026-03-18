---
name: pre-merge-review
description: Perform a strict production-readiness review for correctness, maintainability, security, testing, UX, UI polish, and release risk.
---

# Purpose

Use this skill before considering work complete or ready to merge.

This is the quality gate skill.
Its job is to identify:
- correctness risks
- maintainability issues
- architecture drift
- missing validation
- test gaps
- security concerns
- performance concerns
- accessibility issues
- UX/UI quality gaps

# Use this skill when

Use this skill when the request involves:
- final review before merge
- assessing production readiness
- finding must-fix issues
- classifying risks by priority
- reviewing a completed feature or bugfix
- performing a disciplined quality pass

# Do not use this skill when

Do not use this skill as the main workflow for:
- greenfield feature implementation
- architecture planning
- raw debugging
- tiny isolated edits with negligible risk

# Review mindset

Be rigorous.
Be concrete.
Do not praise weak work.
Do not nitpick trivia while missing important risks.

Focus on what materially affects:
- correctness
- trust
- maintainability
- release safety
- product quality

# Workflow

## 1. Inspect the changed area in context

Review:
- affected files
- nearby modules
- repository patterns
- changed assumptions or contracts
- possible collateral impact
- whether the implementation feels native to the repo

## 2. Evaluate critical dimensions

Check for:
- logic correctness
- missing edge-case handling
- type weakening
- missing validation
- weak error handling
- architecture drift
- duplication
- unsafe trust boundaries
- authorization concerns
- insufficient test coverage
- missing non-happy states
- poor accessibility basics
- weak responsive behavior
- UI that feels unfinished or generic
- avoidable complexity
- UX ambiguity

## 3. Classify findings

Use:
- must fix
- should fix
- nice to improve

## 4. Recommend clean corrections

For each important issue:
- identify the issue
- explain why it matters
- suggest the smallest strong correction

## 5. Final verdict

Conclude with:
- overall readiness
- top risks
- whether the change is acceptable as-is
- what should happen before merge if not ready

# Output discipline

Do not:
- mark something safe without enough evidence
- confuse taste with meaningful quality criteria
- ignore product-facing quality issues in visible UI
- treat missing validation or testing as minor when risk is material