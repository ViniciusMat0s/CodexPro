---
name: form-systems
description: Build or refine complex forms with strong structure, validation, submission behavior, error handling, and trustworthy transactional UX.
---

# Purpose

Use this skill when the task centers on building or improving important forms.

This skill is for:
- multi-field forms
- settings/account forms
- onboarding forms
- transactional forms
- forms with validation complexity
- forms that mutate important product data

# Use this skill when

Use this skill when the request involves:
- creating a serious form flow
- improving validation or submission behavior
- making a form feel more trustworthy and robust
- aligning client and server validation
- handling success/error/submitting states well

# Do not use this skill when

Do not use this skill for:
- auth-specific work when auth-flow-ship is the better fit
- tiny one-field edits
- pure page layout changes with no form complexity
- review-only tasks

# Form philosophy

A serious form is a trust surface.
It must feel:
- clear
- stable
- predictable
- safe to submit
- explicit in feedback
- resilient to invalid input and retries

# Workflow

## 1. Define form intent

Determine:
- what data is collected
- what user outcome depends on it
- whether submission is reversible
- what fields are critical
- what validation rules matter
- what success/failure means

## 2. Structure the form clearly

Prefer:
- logical grouping
- good labels
- explicit required/optional expectations
- concise helper text where needed
- clear primary action
- reduced cognitive load

## 3. Align validation and contracts

Ensure:
- validation rules are explicit
- client and server expectations align
- field-level and form-level errors are handled intentionally
- disabled/submitting behavior prevents bad UX

## 4. Handle transactional states

Include:
- loading defaults if relevant
- submit-in-progress state
- success feedback
- failure feedback
- retry path
- unsaved changes behavior if relevant

## 5. Review trust and usability

Check:
- completion ease
- error clarity
- field grouping quality
- keyboard flow
- mobile usability
- accidental duplicate submit prevention

## 6. Final summary

Summarize:
- form purpose
- validation approach
- states handled
- UX trust improvements
- remaining risk if any

# Quality bar

The form should feel:
- trustworthy
- clear
- structured
- resilient
- product-grade