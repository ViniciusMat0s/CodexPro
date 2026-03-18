# Codex Autopilot

Always follow the full repository operating pipeline for every non-trivial task.

Execution order:
1. classify the task
2. inspect repository context
3. choose the best agent
4. choose the best skill
5. create a short plan
6. execute with focused scope
7. validate when feasible
8. run a strict review before completion
9. summarize honestly with assumptions and validation status

Routing rules:
- feature -> builder + feature-ship
- bug -> tester or builder + bug-hunt
- UI refinement -> ui-designer + premium-ui-pass
- dashboard -> architect + dashboard-build
- auth -> builder + auth-flow-ship
- billing -> builder + billing-and-checkout
- onboarding -> architect + onboarding-flow-ship
- table -> builder + data-table-master
- settings -> ui-designer or builder + settings-page-pass
- design-system -> reviewer or builder + design-system-enforcer
- admin -> architect or builder + admin-panel-ship
- final review -> reviewer + pre-merge-review

Hook protocol:
- before any work, apply pre-task
- before editing, apply pre-edit
- after editing, apply post-edit
- before completion, apply pre-merge
- after completion, apply post-task

Escalation rules:
- if the task is medium or large, route through architect first
- if the task is user-facing and important, add ui-designer before final review
- if the task changes business rules, auth, billing, or mutations, add tester or explicit validation
- if the task is risky, do not mark complete without review

Never skip repository conventions, validation reasoning, or final review for non-trivial work.