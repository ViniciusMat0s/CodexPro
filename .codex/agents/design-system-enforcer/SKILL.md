---
name: design-system-enforcer
description: Enforce consistency across components, spacing, typography, tokens, primitives, and UI APIs so the product behaves like a coherent design system.
---

# Purpose

Use this skill to strengthen and protect design-system consistency in a premium web product.

This skill is for:
- inconsistent component APIs
- spacing drift
- typography drift
- duplicated primitives
- ad hoc visual decisions
- one-off components that should align with shared patterns
- strengthening reusable UI foundations

# Use this skill when

Use this skill when the request involves:
- cleaning up UI inconsistency
- standardizing repeated components
- tightening primitives and component patterns
- aligning buttons, inputs, cards, badges, tables, and panels
- improving repository-wide UI cohesion

# Do not use this skill when

Do not use this skill for:
- pure feature implementation with no design-system concern
- auth-only logic
- isolated bug fixes unless they expose consistency debt
- landing page conversion work as the main task

# Design system philosophy

Consistency compounds quality.
A strong product should feel like one system, not many disconnected pages.

# Workflow

## 1. Inspect the repeated patterns

Check:
- buttons
- inputs
- selects
- cards
- tables
- panels
- badges
- headings
- spacing patterns
- radius/shadow usage
- empty states
- form structure

## 2. Identify drift

Look for:
- duplicate components with slight differences
- inconsistent prop APIs
- repeated class patterns that should become primitives
- typography inconsistency
- arbitrary spacing/radius/shadow variations
- inconsistent interaction states

## 3. Strengthen system foundations

Prefer:
- shared primitives where reuse is real
- predictable component APIs
- coherent sizing and spacing
- consistent interaction states
- reduced visual drift
- repository-wide reuse of the best patterns

Avoid:
- premature over-abstraction
- giant UI frameworks inside the repo
- breaking changes without clear benefit

## 4. Protect ergonomics

A design system should improve speed, not slow it down.

Ensure:
- components remain easy to use
- APIs stay expressive and predictable
- primitives do not become over-configured monsters

## 5. Final summary

Summarize:
- inconsistencies found
- primitives or patterns improved
- APIs or tokens aligned
- remaining debt if any

# Quality bar

The result should move the repository toward:
- stronger cohesion
- faster UI implementation
- fewer one-off visual decisions
- more premium consistency