# Codex Operating Pipeline

This repository uses a structured Codex execution system designed for premium web product development.

The purpose of this pipeline is to ensure that every task is handled with:
- correct routing
- strong technical judgment
- repository consistency
- high product quality
- controlled validation
- honest completion criteria

This is not a generic assistant workflow.
This is a production execution pipeline.

---

# 1. Core Principle

Every task should pass through the following mental stages:

1. classify
2. inspect
3. route
4. plan
5. execute
6. validate
7. review
8. finalize

Not every task needs the full heavy version of the pipeline.
But every non-trivial task must follow the logic of this pipeline.

---

# 2. Execution Layers

The pipeline operates on four layers:

## Layer 1 — Global behavior
Applied from:
- global AGENTS.md
- project AGENTS.md

These define baseline operating standards.

## Layer 2 — Specialist execution
Applied from:
- custom agents

These define who should handle the task:
- architect
- builder
- tester
- ui-designer
- reviewer

## Layer 3 — Operational workflow
Applied from:
- skills

These define how the task should be executed:
- feature-ship
- premium-ui-pass
- bug-hunt
- pre-merge-review
- dashboard-build
- auth-flow-ship
- landing-page-conversion-pass
- design-system-enforcer
- form-systems
- admin-panel-ship
- billing-and-checkout
- onboarding-flow-ship
- data-table-master
- settings-page-pass

## Layer 4 — Final quality discipline
Applied by:
- validation
- review pass
- honest final summary

---

# 3. Task Classification

Before doing anything, classify the task into one of the following:

- feature
- bug
- refactor
- architecture
- review
- UI refinement
- dashboard
- auth
- billing
- onboarding
- table
- settings
- design-system
- admin

If a task spans multiple categories, choose:
- one primary category
- one secondary category if needed

Example:
- a new settings page with complex form logic:
  - primary: settings
  - secondary: form

- a pricing page with checkout flow:
  - primary: billing
  - secondary: landing page

---

# 4. Pipeline Stages

## Stage 1 — Classify

Determine:
- what kind of task this is
- whether it is small, medium, or large
- whether it is risky
- whether it is user-facing
- whether it touches security, auth, billing, or data integrity

Questions:
- Is this a feature or a fix?
- Is this visible to the user?
- Does it change architecture or only implementation?
- Does it require a premium UI pass?
- Does it require strict validation or review?

## Stage 2 — Inspect

Before editing:
- inspect relevant files
- inspect nearby modules
- identify repository conventions
- identify reusable components, hooks, services, utilities, schemas, and types
- identify related tests
- identify likely risk boundaries

Never start implementation blind.

## Stage 3 — Route

Choose:
- best agent
- best skill
- whether multiple passes are needed

Examples:
- feature → architect + builder + reviewer
- UI polish → ui-designer + reviewer
- bug → tester/builder + reviewer
- dashboard → architect + dashboard-build + builder + reviewer

## Stage 4 — Plan

Produce a short plan containing:
- task objective
- affected files or areas
- implementation approach
- assumptions
- validation approach

For small tasks, this plan can be implicit and short.
For medium and large tasks, it should be explicit.

## Stage 5 — Execute

Implement with discipline:
- keep scope focused
- preserve repository patterns
- avoid unrelated edits
- preserve type safety
- handle relevant user-facing states
- avoid introducing silent regressions

## Stage 6 — Validate

When feasible, perform:
- lint
- typecheck
- tests
- build
- manual QA

If validation was not performed, say so clearly.

## Stage 7 — Review

Before considering work complete, evaluate:
- correctness
- maintainability
- repository fit
- UX quality
- UI quality
- validation completeness
- security implications
- regression risk
- performance implications
- accessibility basics

## Stage 8 — Finalize

Final summaries should include:
- what changed
- key files affected
- assumptions
- validations performed
- validations not performed
- residual risk
- best next step if relevant

---

# 5. Pipeline Modes by Task Size

## Small task
Examples:
- copy tweak
- tiny bug fix
- minor UI adjustment
- small styling correction

Use:
- inspect
- execute
- light review
- finalize

Usually:
- builder or reviewer
- one skill at most

## Medium task
Examples:
- non-trivial form
- settings section
- table update
- dashboard module
- auth step
- substantial bug fix

Use:
- inspect
- route
- short plan
- execute
- validate
- review
- finalize

Usually:
- one primary agent
- one primary skill
- reviewer or pre-merge-review at the end

## Large task
Examples:
- new product area
- onboarding flow
- billing area
- dashboard from scratch
- major refactor
- multi-surface feature

Use:
- inspect
- route
- explicit plan
- architecture pass
- implementation pass
- validation pass
- review pass
- finalize

Usually:
- architect first
- builder second
- ui-designer/tester if needed
- reviewer last

---

# 6. Routing Matrix

## Feature
Primary agent:
- builder

Recommended support:
- architect for medium/large tasks
- reviewer at the end

Primary skill:
- feature-ship

Optional support skills:
- premium-ui-pass
- form-systems
- data-table-master
- settings-page-pass
- dashboard-build

## Bug
Primary agent:
- tester or builder

Recommended support:
- reviewer at the end

Primary skill:
- bug-hunt

Optional support skills:
- pre-merge-review

## UI refinement
Primary agent:
- ui-designer

Recommended support:
- builder if structural edits are required
- reviewer at the end

Primary skill:
- premium-ui-pass

## Architecture
Primary agent:
- architect

Primary skill:
- none required, or feature-ship planning phase

Optional support:
- reviewer for structural risk review

## Review
Primary agent:
- reviewer

Primary skill:
- pre-merge-review

## Dashboard
Primary agent:
- architect first, builder second

Primary skill:
- dashboard-build

Optional support skills:
- feature-ship
- data-table-master
- premium-ui-pass
- pre-merge-review

## Auth
Primary agent:
- builder

Recommended support:
- tester
- reviewer

Primary skill:
- auth-flow-ship

Optional support:
- form-systems
- pre-merge-review

## Billing
Primary agent:
- builder

Recommended support:
- ui-designer
- tester
- reviewer

Primary skill:
- billing-and-checkout

Optional support:
- landing-page-conversion-pass
- pre-merge-review

## Onboarding
Primary agent:
- architect first, builder second

Recommended support:
- ui-designer
- reviewer

Primary skill:
- onboarding-flow-ship

Optional support:
- feature-ship
- premium-ui-pass
- pre-merge-review

## Table
Primary agent:
- builder

Recommended support:
- ui-designer if visual polish matters
- reviewer

Primary skill:
- data-table-master

Optional support:
- pre-merge-review

## Settings
Primary agent:
- ui-designer or builder depending on task

Recommended support:
- reviewer

Primary skill:
- settings-page-pass

Optional support:
- form-systems
- pre-merge-review

## Design system
Primary agent:
- reviewer or builder

Recommended support:
- ui-designer
- architect if repo-wide changes are large

Primary skill:
- design-system-enforcer

## Admin
Primary agent:
- architect first for large surfaces, builder for direct execution

Primary skill:
- admin-panel-ship

Optional support:
- data-table-master
- premium-ui-pass
- pre-merge-review

---

# 7. Standard Playbooks

## Playbook A — New feature
1. inspect repository context
2. route to architect if medium/large
3. use feature-ship
4. execute with builder
5. validate
6. review with reviewer or pre-merge-review
7. finalize

## Playbook B — Bug fix
1. inspect broken area
2. use bug-hunt
3. identify root cause
4. apply minimal reliable fix
5. add regression protection if appropriate
6. review with reviewer
7. finalize

## Playbook C — Premium UI refinement
1. inspect current screen and design language
2. use premium-ui-pass
3. refine hierarchy, spacing, states, responsiveness
4. review with reviewer
5. finalize

## Playbook D — Dashboard
1. define dashboard purpose and information hierarchy
2. use dashboard-build
3. implement with builder
4. use data-table-master if necessary
5. polish with premium-ui-pass if necessary
6. review with pre-merge-review
7. finalize

## Playbook E — Auth flow
1. inspect entry points and validation boundaries
2. use auth-flow-ship
3. implement with builder
4. test invalid and expired states
5. review with reviewer
6. finalize

## Playbook F — Billing/checkout
1. clarify plan, price, and transaction logic
2. use billing-and-checkout
3. polish trust and UX if necessary
4. validate failure and success states
5. review with reviewer
6. finalize

## Playbook G — Settings page
1. define settings information architecture
2. use settings-page-pass
3. use form-systems where needed
4. validate save/apply/destructive states
5. review with pre-merge-review
6. finalize

---

# 8. Hooks Protocol

The following protocol should be mentally applied for all non-trivial tasks.

## Pre-task
Before starting:
- understand the goal
- classify task type
- inspect relevant files
- identify conventions
- define minimal scope

## Pre-edit
Before editing:
- read the full relevant file
- inspect related files if needed
- confirm correct modification point
- avoid inventing new patterns without reason

## Post-edit
After editing:
- review logic
- review imports and contracts
- check types
- check missing UI states
- check regression risk

## Pre-merge
Before considering complete:
- review correctness
- review repository consistency
- review validation completeness
- review UX/UI quality if relevant
- review security and performance implications
- classify issues into must fix / should fix / nice to improve

## Post-task
At the end:
- summarize honestly
- state assumptions
- state validation status
- state remaining risk

---

# 9. Model Usage Guidance

Recommended model strategy:

## High-complexity or critical tasks
Use:
- gpt-5.4

Examples:
- architecture
- complex feature implementation
- billing
- auth
- large review
- difficult refactors

## Lighter or faster supporting work
Use:
- gpt-5.4-mini when appropriate

Examples:
- exploration
- simple analysis
- small review passes
- lightweight supporting subagents

Default bias:
- choose stronger model for critical paths
- choose lighter model for secondary support work

---

# 10. Approvals and Safety Guidance

## Read-only mode
Best for:
- architecture
- exploration
- review
- initial debugging

## Workspace auto execution
Best for:
- normal implementation
- local refactors
- validation within the repo

## Explicit approval required
Use caution for:
- network access
- files outside workspace
- sensitive commands
- anything with meaningful risk beyond the repository

Never normalize unsafe behavior just for speed.

---

# 11. Completion Standard

A task is not complete because code was written.
A task is complete when:
- it fits the repository
- the solution is coherent
- important states were considered
- validation was performed when feasible
- risks are understood
- completion is reported honestly

Never mark something complete if critical issues remain obvious.

---

# 12. Final Summary Standard

Every substantial task should end with:

## Summary format
- what changed
- why
- key files touched
- assumptions made
- validation performed
- validation not performed
- remaining risks
- next best step if relevant

The final summary must be concise, concrete, and honest.

---

# 13. Daily Operating Rule

For every non-trivial task:
- do not improvise the workflow
- classify first
- route correctly
- execute with the right skill
- review before calling it done

Consistency is part of product quality.