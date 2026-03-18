# Implementation Checklist

Use this checklist when shipping a non-trivial feature.

## Repository fit
- Does the solution follow existing architecture?
- Are nearby conventions preserved?
- Is there any duplicated logic that should reuse an existing utility/service/component?

## Boundaries
- Are UI, validation, domain logic, and data access separated cleanly enough?
- Are server/client responsibilities placed intentionally?
- Are contracts explicit?

## States
- Loading state handled
- Empty state handled if relevant
- Error state handled
- Success feedback handled if relevant
- Disabled/submitting state handled for forms/actions
- Permission/access-denied state handled if relevant

## UX
- Is the primary action obvious?
- Is the flow understandable?
- Does the user get useful feedback after actions?
- Are labels and messaging clear?

## Type safety
- Are important contracts typed?
- Was type safety preserved?
- Was weak "any" avoided unless justified?

## Validation
- Is input validated at the right boundary?
- Are client and server expectations aligned?
- Are failure paths explicit?

## Regression awareness
- Could this break adjacent behavior?
- Should tests be added or updated?
- Are there side effects in nearby modules?

## Final quality
- Does this feel production-ready?
- Does it belong in the repository?
- Is it maintainable?