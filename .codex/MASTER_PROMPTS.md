# Master Prompts

## 1. New feature
Use the correct pipeline for a production-grade feature in this repository.

Process:
- classify the task
- inspect relevant files and patterns
- route to the appropriate agent and skill
- create a short implementation plan
- implement with focused scope
- validate when feasible
- review before completion
- summarize honestly

Use:
- architect first if the task is medium or large
- builder for implementation
- reviewer or pre-merge-review before finalizing

## 2. Bug fix
Use the bug pipeline for this issue.

Process:
- classify as bug or regression
- inspect related code paths
- identify the best-supported root cause
- apply the smallest reliable fix
- add regression protection if appropriate
- review for collateral risk
- summarize cause, fix, validation, and residual risk

Use:
- bug-hunt
- reviewer before finalizing

## 3. Premium UI
Use the premium UI pipeline for this screen.

Process:
- inspect the current design language
- identify hierarchy, spacing, and state issues
- refine the interface to premium SaaS quality
- verify responsiveness and accessibility basics
- review before finalizing

Use:
- ui-designer
- premium-ui-pass
- reviewer

## 4. Dashboard
Use the dashboard pipeline for this work.

Process:
- define dashboard purpose and information hierarchy
- structure KPIs, actions, tables, and sections intentionally
- implement with strong scanability and product states
- apply table refinement if needed
- review before finalizing

Use:
- architect
- dashboard-build
- builder
- data-table-master if needed
- reviewer

## 5. Auth
Use the auth pipeline for this flow.

Process:
- inspect validation and route protection boundaries
- implement the flow with strong trust UX
- handle invalid, expired, and failure states
- validate and review before finalizing

Use:
- builder
- auth-flow-ship
- tester if needed
- reviewer

## 6. Billing
Use the billing pipeline for this flow.

Process:
- inspect plan, price, and transaction logic
- implement trustworthy plan and checkout UX
- handle success, failure, and billing-management states
- review before finalizing

Use:
- builder
- billing-and-checkout
- ui-designer if needed
- reviewer

## 7. Settings
Use the settings pipeline for this work.

Process:
- define settings information architecture
- group sections clearly
- refine trust, clarity, and destructive-action safety
- validate save/apply flows
- review before finalizing

Use:
- settings-page-pass
- form-systems if needed
- reviewer