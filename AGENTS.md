# Project Operating Manual

This repository is a premium web product codebase.
All work in this project must optimize for product quality, engineering quality, maintainability, and polished user experience.

This is not a prototype-first repository.
This is a production-minded codebase.

---

# 1. Project Identity

## Product standard
The product should feel:
- premium
- modern
- intentional
- reliable
- fast
- visually refined
- architecturally coherent

## Engineering standard
The code should be:
- production-grade
- strongly typed
- modular
- readable
- testable
- safe by default
- consistent across the repository

## Delivery standard
A task is not complete just because the code renders.
A task is complete when:
- it fits existing architecture
- it respects product direction
- it preserves or improves maintainability
- states and edge cases were considered
- quality checks were performed when feasible

---

# 2. Primary Stack Assumptions

Unless the repository explicitly indicates otherwise, prefer the following patterns.

## Frontend
- Next.js with App Router
- TypeScript
- Tailwind CSS
- reusable UI components
- server-first patterns when appropriate
- client components only when needed
- React Hook Form for non-trivial forms
- Zod for schema validation
- composable hooks and utilities

## Backend
- route handlers or server actions depending on project conventions
- thin transport layer
- service-oriented business logic
- explicit validation at boundaries
- typed request/response contracts
- predictable error handling

## Data and contracts
- domain types should be clear
- input validation should be explicit
- avoid shape ambiguity between layers
- keep contracts stable and understandable

---

# 3. Repository Priorities

When making decisions, prioritize in this order:

1. correctness
2. consistency with repository conventions
3. maintainability
4. product quality
5. clarity
6. performance
7. implementation speed

Do not choose faster implementation paths that create weak architecture or ugly user experience unless explicitly requested.

---

# 4. Repository Structure Philosophy

## High-level structure
The repository should remain easy to navigate and reason about.

Prefer clear separation between:
- app routes and page-level composition
- UI components
- domain/business logic
- data access and API integration
- shared utilities
- validation schemas
- types and contracts

## Recommended conceptual boundaries
- `app/` for routes, layouts, and page entry points
- `components/` for reusable UI and page sections
- `lib/` for utilities, helpers, integrations, and cross-cutting modules
- `services/` for business/domain logic when applicable
- `schemas/` for Zod schemas and validation logic when helpful
- `types/` for shared domain types if needed
- `hooks/` for reusable custom hooks
- `constants/` for stable, shared constants
- `styles/` only when necessary beyond Tailwind conventions

Do not force structure mechanically.
Use the current repository’s established layout if it is already coherent.

---

# 5. Rules for Working in Existing Code

Before making edits:
- inspect nearby files
- identify local patterns
- follow naming conventions
- check whether utilities/components/hooks already exist
- avoid introducing a new pattern if the current one is already solid

When editing:
- keep diffs focused
- preserve local consistency
- avoid unnecessary churn
- do not rename or move files casually
- do not “clean up” unrelated code unless it directly improves the task

After editing:
- review imports, contracts, and affected states
- check whether related files also need updates
- consider regression risk
- run relevant validation steps when feasible

---

# 6. Frontend Architecture Rules

## Component design
Prefer:
- small and composable components
- clear prop APIs
- predictable rendering logic
- separation between layout, presentation, and business concerns
- reusable UI primitives when reuse is likely

Avoid:
- giant page files with too much logic
- over-generic abstraction with unclear value
- deeply nested JSX when structure can be clarified
- copy-pasted sections that should be reusable
- putting business rules directly into visual components when avoidable

## Client vs server components
Default to server-oriented design where appropriate.
Use client components only when necessary for:
- interactivity
- local state
- browser-only APIs
- event-driven UI behavior

Do not mark components as client unnecessarily.

## State management
Prefer the lightest viable state approach.

Priority order:
1. server data patterns where appropriate
2. local component state
3. lifted state for shared page-local behavior
4. custom hooks for reusable state logic
5. heavier state solutions only when truly justified

Avoid global state unless there is a real cross-tree need.

---

# 7. UI and Design System Rules

## Design direction
This project should maintain a premium web product aesthetic.

Default visual characteristics:
- clean layout
- strong hierarchy
- deliberate spacing
- balanced density
- refined typography
- restrained use of color
- elegant cards, panels, tables, sections, and forms
- polished interaction states
- cohesive composition across pages

## UI consistency
Maintain consistency in:
- spacing scale
- typography scale
- corner radius
- shadows
- input/button sizing
- card density
- panel composition
- icon sizing
- empty state treatment
- loading state treatment

Do not create visually inconsistent one-off components without a strong reason.

## Page composition
Pages should feel designed, not merely assembled.

Always think about:
- hero/entry hierarchy
- section rhythm
- alignment
- emphasis of primary actions
- grouping of related information
- scanability
- whitespace quality
- responsive composition

## Tailwind usage
Use Tailwind intentionally.
Prefer:
- readable class composition
- utility reuse patterns where practical
- extracted components when markup repeats
- consistent spacing and sizing decisions

Avoid:
- class chaos
- arbitrary values everywhere
- visual inconsistency from ad hoc styling
- giant unreadable class strings when component extraction would help

---

# 8. Premium Interface Standards

Every user-facing area should consider the following states when relevant:
- default
- hover
- focus
- active
- disabled
- loading
- empty
- error
- success

At premium quality level, the interface should not feel unfinished in secondary states.

## Tables
Tables should be:
- easy to scan
- aligned properly
- visually clean
- responsive or gracefully degraded
- clear in empty/loading/error conditions

## Forms
Forms should be:
- visually structured
- easy to complete
- explicit in validation feedback
- resistant to accidental misuse
- clear about required actions and submission results

## Cards and panels
Cards should:
- have a real information hierarchy
- avoid visual clutter
- avoid arbitrary padding differences
- support action discoverability without noise

## Dashboards
Dashboards should:
- prioritize the most important information first
- avoid equal visual weight for all widgets
- use hierarchy and grouping intentionally
- feel operational, not decorative

## Landing pages
Landing pages should:
- communicate value fast
- preserve premium aesthetics
- use strong copy hierarchy
- support conversion with clear flow
- avoid generic template feel

---

# 9. UX Rules

Prefer flows that are:
- obvious
- low-friction
- trustworthy
- consistent
- reversible when appropriate

Always consider:
- what the user needs to understand first
- what action should feel primary
- where confusion might occur
- what can be simplified
- whether feedback is clear after important actions

Avoid:
- ambiguous labels
- weak CTA hierarchy
- noisy interfaces
- hidden critical actions
- poor feedback after submission or mutation

---

# 10. Accessibility Baseline

All UI work should preserve or improve accessibility.

Minimum expectations:
- semantic HTML
- proper button/link usage
- labels for form controls
- visible focus states
- reasonable contrast
- keyboard reachability where applicable
- meaningful text for actions and status

Do not sacrifice accessibility for visual style.

---

# 11. Form Standards

For non-trivial forms:
- prefer React Hook Form
- prefer Zod for schema validation
- keep validation rules explicit
- align client and server validation concepts when possible
- surface field errors clearly
- prevent ambiguous submission states

Form implementations should include:
- valid default values
- loading/submitting feedback
- server failure handling
- success feedback when appropriate
- disabled states when necessary

Do not build fragile forms with scattered uncontrolled logic if a structured form layer is more appropriate.

---

# 12. Validation and Schema Rules

Use explicit validation at boundaries.

Prefer:
- Zod schemas for important inputs
- reusable schema fragments when they meaningfully reduce duplication
- schema names that reflect domain meaning
- alignment between UI validation and backend expectations

Do not:
- trust client input blindly
- spread validation rules across many unrelated files without reason
- use loose validation for important flows

---

# 13. Backend and Server Rules

## Handlers and actions
Keep transport layers thin.
Handlers, route functions, and server actions should:
- validate input
- delegate business rules
- return predictable output
- handle failure paths intentionally

Do not pack complex business logic directly into transport entry points.

## Services and business logic
Business/domain logic should:
- be isolated enough to test
- be understandable without UI context
- avoid hidden coupling to rendering layers
- preserve clean contracts

## Error handling
- fail clearly
- return safe errors
- log appropriately when relevant
- avoid swallowing failures
- do not leak secrets or internals to clients

---

# 14. Security Rules

Every implementation should consider security implications.

Always think about:
- auth
- authorization boundaries
- input validation
- secret handling
- sensitive data exposure
- unsafe client trust
- injection risks
- upload risks
- third-party API trust boundaries
- webhook verification when relevant

Never:
- commit secrets
- expose private keys in client code
- skip authorization checks on sensitive operations
- trust request payloads without validation
- introduce insecure convenience shortcuts casually

---

# 15. API and Contract Rules

API shapes should be:
- explicit
- stable
- typed
- predictable
- well-validated

Prefer:
- consistent response patterns
- domain-meaningful field names
- narrow and explicit input types
- safe defaults

Avoid:
- inconsistent payload shapes
- weak typing between layers
- ambiguous nullable behavior
- magical response formats that require guesswork

---

# 16. Data Fetching Rules

Data fetching should be:
- intentional
- efficient
- easy to reason about
- aligned with framework patterns

Prefer:
- server data fetching where it makes sense
- clear loading behavior
- clear error behavior
- minimizing duplicate requests
- cache-aware decisions when relevant

Avoid:
- unnecessary client-side fetching
- duplicate fetching across layers
- unclear ownership of data
- inconsistent loading logic

---

# 17. TypeScript Rules

Use TypeScript as a safety and design tool, not just a compiler requirement.

Prefer:
- explicit types where they improve clarity
- strong domain types
- narrowed unions when useful
- typed contracts between modules
- avoiding `any` unless there is a justified boundary case

Do not:
- suppress type errors casually
- weaken important contracts for convenience
- introduce vague shared types that hide domain meaning

Types should make the system easier to understand.

---

# 18. Reuse and Abstraction Rules

Extract abstractions when they:
- reduce real duplication
- improve clarity
- create a useful reusable primitive
- reduce future change cost

Do not extract abstractions when they:
- only save a few lines
- make code harder to follow
- introduce indirection with weak value
- prematurely generalize future needs

Good abstractions should feel obvious in hindsight.

---

# 19. Dependency Rules

Before adding a dependency, ask:
- is this already solved in the repo?
- can the framework or platform handle it?
- is the dependency worth the cost?
- does it fit the architecture and quality bar?

Prefer fewer dependencies when the value is low.

Avoid adding libraries for:
- trivial formatting
- small helper behavior
- things already solved by framework primitives
- short-term convenience with long-term maintenance cost

---

# 20. Testing Rules

## Testing philosophy
Tests in this project should protect important behavior and reduce regression risk.

## When tests are expected
Tests should be strongly considered when changing:
- business rules
- auth flows
- billing or payments
- critical forms
- mutations
- validation logic
- non-trivial data transforms
- bug fixes with clear regression risk

## Test priorities
Prefer testing:
- real behavior
- success path
- failure path
- edge cases
- user-visible outcomes
- domain rules

Avoid:
- brittle implementation-detail tests
- excessive mocking when realism is practical
- shallow tests that provide false confidence

## Manual QA
When automated coverage is absent or insufficient, provide concise manual QA steps.

---

# 21. Performance Rules

Performance matters, but not through pointless micro-optimization.

Pay attention when work affects:
- page rendering
- repeated components
- long lists
- heavy client logic
- image/media delivery
- bundle size
- server latency
- expensive data operations

Prefer:
- avoiding unnecessary rerenders
- keeping client logic lean
- sensible lazy loading
- stable memoization only when justified
- efficient fetch patterns
- keeping the critical path clean

Avoid:
- premature optimization
- complex optimization with negligible gain
- sacrificing readability for hypothetical performance wins

---

# 22. Error, Empty, and Loading State Rules

No meaningful user-facing flow should feel unfinished in non-happy paths.

Always consider whether the feature needs:
- loading UI
- error messaging
- retry affordances
- empty state copy
- zero-data guidance
- disabled state behavior
- skeletons or placeholders

A polished product handles absence and failure gracefully.

---

# 23. Copy and Microcopy Rules

UI text should be:
- clear
- concise
- intentional
- useful
- aligned with product tone

Prefer:
- direct labels
- helpful validation messages
- action-oriented CTA text
- empty states that guide next steps
- status messages that reduce uncertainty

Avoid:
- vague wording
- robotic text
- verbose buttons
- generic “something went wrong” when better guidance is possible

---

# 24. Code Review Standard for This Repository

When reviewing changes, evaluate:
- architecture fit
- local consistency
- type safety
- UI quality
- UX quality
- regression risk
- validation quality
- security implications
- edge-case handling
- maintainability

Mentally classify issues as:
- must fix
- should fix
- nice to improve

Default to rigor, not politeness.

---

# 25. Non-Trivial Task Workflow

For medium or large tasks in this repo, follow this sequence:

1. inspect surrounding code and conventions
2. identify architecture boundaries
3. map affected files and contracts
4. choose a clean implementation path
5. implement focused changes
6. review edge cases and side effects
7. validate via lint, typecheck, tests, or build when feasible
8. summarize changes, assumptions, and validations

---

# 26. UI Task Workflow

For UI-heavy work in this repo, follow this sequence:

1. understand the user flow
2. inspect current design language
3. define hierarchy and layout
4. build structure
5. refine spacing, typography, and composition
6. implement states
7. verify responsiveness
8. verify accessibility basics
9. polish toward premium quality

---

# 27. Bug Fix Workflow

For bug fixes:
1. identify likely failure boundary
2. inspect related code paths
3. infer best-supported root cause
4. implement minimal reliable fix
5. add regression protection if appropriate
6. review for collateral impact
7. summarize cause, fix, and remaining risk

---

# 28. Change Discipline

Do not:
- mix unrelated refactors into focused tasks
- make speculative rewrites
- add dead code
- leave placeholder logic in production paths
- create duplicate utility layers
- degrade readability to save a few lines
- hide defects with weak fallback logic

Do:
- keep changes coherent
- leave the touched area stronger than before
- preserve repository consistency
- make future extension easier when practical

---

# 29. Validation Checklist

When relevant, validate through some combination of:
- lint
- typecheck
- tests
- build
- manual flow verification

Never state that something is verified unless it actually was.

If validation could not be run, state that clearly.

---

# 30. What Excellent Work Looks Like in This Repo

Excellent work in this codebase usually:
- feels native to the repository
- improves product quality, not just code output
- uses strong engineering judgment
- preserves simplicity where possible
- creates polished user-facing results
- handles non-happy paths
- keeps architecture healthy
- reduces future maintenance burden

---

# 31. Final Instruction

Work like a high-agency senior engineer building a premium web product.

Every task should move this repository toward:
- better architecture
- better product quality
- better UI/UX
- better reliability
- better maintainability

Do not produce merely functional output.
Produce strong, production-worthy work.

---

# 32. SaaS Product Bias

This repository builds a premium SaaS-style web product.

Default product expectations:
- premium perceived value
- polished onboarding and activation flows
- professional dashboards
- clean settings/account areas
- trustworthy forms and transactional flows
- strong CTA hierarchy
- excellent empty/loading/error states
- visually refined operational interfaces

## SaaS UI expectations
- cards should feel premium, not template-generated
- tables should feel operational and clean
- settings pages should be calm and structured
- forms should feel trustworthy and efficient
- dashboards should emphasize decision-making and action
- landing pages should convert without visual noise

## SaaS UX expectations
- reduce friction in key actions
- make primary workflows obvious
- preserve clarity around account, plan, billing, and data actions
- create confidence in every critical interaction
- avoid cluttered “feature dump” interfaces

## SaaS engineering expectations
- preserve scalability of UI patterns
- favor reusable primitives for repeated product surfaces
- keep business logic portable and testable
- protect important user and account flows with stronger validation and testing