---
name: billing-and-checkout
description: Build or refine billing, plan, pricing, and checkout flows with strong trust signals, clear plan logic, safe transactional UX, and production-grade payment flow quality.
---

# Purpose

Use this skill for monetization surfaces and payment-related product flows.

This skill is for:
- pricing pages
- checkout flows
- billing pages
- subscription management
- plan comparison
- upgrade and downgrade flows
- invoice/payment method areas
- transactional trust and conversion-sensitive flows

# Use this skill when

Use this skill when the request involves:
- building or improving a checkout page
- creating a billing/settings area
- clarifying pricing or plan UI
- improving plan selection UX
- refining upgrade/downgrade flows
- making payment-related flows more trustworthy and production-ready

# Do not use this skill when

Do not use this skill for:
- generic landing page work without billing logic
- non-transactional forms
- auth-only work
- pure backend billing integrations with no user-facing flow considerations

# Billing philosophy

Billing and checkout are trust surfaces.
They must feel:
- safe
- clear
- calm
- explicit
- reliable
- low-friction without being vague

The user should never feel uncertainty about:
- what they are buying
- what they will be charged
- when they will be charged
- how to change or cancel
- whether the action succeeded

# Workflow

## 1. Define the transaction model

Determine:
- what the user is selecting
- what plan/price logic exists
- whether it is one-time or recurring
- whether trial logic exists
- what billing interval choices exist
- what happens after success
- what error states are possible

## 2. Clarify plan and pricing presentation

Ensure:
- plans are easy to compare
- highlighted plans are intentional
- included features are understandable
- pricing cadence is clear
- taxes/fees ambiguity is reduced when relevant
- CTA labels reflect the actual action

## 3. Build trust-first checkout UX

Include:
- clear summary of selected plan or purchase
- explicit pricing visibility
- clear next step
- strong submit/loading protection
- obvious success/failure handling
- useful payment failure messaging
- no hidden confusion around recurring charges or renewals

## 4. Review account and billing management states

Check:
- current plan visibility
- upgrade/downgrade/cancel clarity
- payment method update behavior
- invoice history visibility if relevant
- failed payment states
- grace period or restricted access behavior if applicable

## 5. Validate transaction safety

Think through:
- duplicate submission prevention
- idempotency-sensitive flows
- stale plan state
- incorrect CTA labeling
- unsafe assumptions after redirect
- unclear success state
- poor downgrade/cancel explanation

## 6. Final summary

Summarize:
- flow improved or built
- trust/clarity changes
- billing logic represented in UI
- non-happy states handled
- residual risk if any

# Quality bar

The experience should feel:
- trustworthy
- premium
- transaction-safe
- explicit
- calm under failure cases
- aligned with real subscription/product expectations