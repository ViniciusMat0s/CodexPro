---
name: auth-flow-ship
description: Implement or refine authentication and account-access flows with strong validation, safe contracts, clear UX, and production-grade security awareness.
---

# Purpose

Use this skill for authentication-related product work.

This skill is for:
- sign in
- sign up
- password reset
- magic link flows
- email verification
- session-related account access flows
- onboarding gates tied to account state
- auth-related forms and route protection

# Use this skill when

Use this skill when the request involves:
- building or updating sign-in/sign-up flows
- adding password reset or email verification
- protecting routes or product surfaces
- improving auth UX and reliability
- aligning auth forms with backend expectations
- shipping account entry flows for production

# Do not use this skill when

Do not use this skill for:
- generic forms unrelated to authentication
- dashboard-only work
- pure visual landing page work
- isolated review-only tasks

# Auth philosophy

Auth is a trust surface.
It must feel:
- safe
- clear
- reliable
- low-friction
- explicit about outcomes
- careful about errors and edge cases

# Workflow

## 1. Identify the auth flow shape

Determine:
- entry point
- success destination
- failure modes
- token/session dependencies
- email steps if any
- verification requirements
- route protection implications

## 2. Define validation and contracts

Ensure:
- inputs are validated clearly
- server/client assumptions align
- error conditions are intentional
- sensitive outcomes do not leak internal details

## 3. Implement trust-first UX

Include:
- clear field labels
- submission state feedback
- invalid credential handling
- expired or invalid token handling
- resend flows where relevant
- success confirmation
- route transitions that reduce confusion

## 4. Review security-sensitive behavior

Think through:
- auth vs authorization
- token handling
- session assumptions
- account enumeration risks
- secret exposure risks
- unsafe client trust
- redirect behavior
- replay or stale-link issues where applicable

## 5. Add validation and regression protection

When feasible:
- test critical auth behavior
- test invalid and expired cases
- verify route protection logic
- provide manual QA steps if needed

## 6. Final summary

Summarize:
- auth flow shipped or changed
- contracts and validations
- important edge cases handled
- security-sensitive considerations
- tests or QA performed

# Quality bar

The flow should feel:
- safe
- trustworthy
- calm
- production-ready
- explicit in user feedback
- resistant to obvious misuse