---
name: feature-ship
description: Plan, implement, validate, and summarize a production-grade feature in a premium web repository with strong architecture, complete states, and validation discipline.
---

# Purpose

Use this skill when the task is to deliver a non-trivial feature in a production-oriented web repository.

This skill is designed for feature work that requires discipline from start to finish:
- inspect repository context
- identify architecture boundaries
- map affected files and contracts
- implement with focused scope
- preserve repository conventions
- validate quality when feasible
- summarize clearly with assumptions and validation status

This is the default operational skill for substantial product work.

# Use this skill when

Use this skill when the request involves:
- building a new feature
- adding a new page, route, flow, or module
- implementing a non-trivial form
- creating or extending dashboard/product areas
- shipping authenticated functionality
- integrating UI, validation, and domain logic together
- implementing a production-grade capability rather than a quick prototype

# Do not use this skill when

Do not use this skill for:
- tiny one-line fixes
- isolated bug investigation without broader implementation
- pure UI refinement with no real feature delivery
- review-only work
- architecture-only planning without implementation
- purely test-writing tasks

# Operational mindset

Treat the repository as production-minded.
Do not optimize for “it renders”.
Optimize for:
- correctness
- maintainability
- architecture fit
- strong UX
- complete state handling
- good repository citizenship

# Workflow

## 1. Inspect repository context first

Before editing:
- inspect nearby files and existing conventions
- identify local architecture and file structure
- identify similar functionality that already exists
- check for reusable components, hooks, services, schemas, and utilities
- identify validation and test patterns already used in the repository
- identify whether the repository prefers server-driven, client-driven, or mixed patterns

## 2. Frame the feature

Determine:
- what user outcome is being built
- what parts of the system are affected
- what files are likely involved
- what contracts or schemas may need changes
- what states are necessary:
  - loading
  - empty
  - error
  - success
  - disabled
  - submitting
  - permission-denied if relevant

Also determine:
- auth implications
- authorization implications
- validation boundaries
- data fetching or mutation patterns
- whether the feature affects user trust or critical flows

## 3. Choose implementation shape

Prefer:
- focused changes
- repository-aligned patterns
- reusable primitives when appropriate
- strong typing
- explicit contracts
- business logic outside presentation layers when practical
- clear component boundaries
- clear mutation and error behavior

Avoid:
- broad speculative refactors
- new patterns without justification
- hidden side effects
- duplicate logic
- weak type shortcuts
- incomplete happy-path-only work

## 4. Implement with production discipline

While implementing:
- keep diffs scoped
- preserve naming conventions
- respect folder conventions
- reuse before creating
- think through side effects
- keep visible UI polished
- make forms trustworthy
- make non-happy paths feel intentional, not abandoned

## 5. Validate quality

When feasible, run or recommend:
- lint
- typecheck
- tests
- build
- concise manual QA steps

If validation cannot be run, state that clearly.

## 6. Final summary

Summarize using this structure:
- what was built
- key files changed
- important assumptions
- risks or follow-ups
- validation performed
- validation not performed

# Quality bar

The output should be:
- production-minded
- repository-consistent
- maintainable
- complete in meaningful user states
- strong in UX for visible features
- safe in validation and contracts
- honest about what was and was not verified

# Output discipline

Do not:
- claim verification that did not happen
- mark a feature complete if critical states are obviously missing
- expand scope without reason
- produce placeholder-grade implementation for real feature work