# Auto Router

For every incoming task, classify it first.

Classification rules:
- if the user asks to build something new -> feature
- if the user asks to fix or investigate breakage -> bug
- if the user asks to improve visuals, layout, hierarchy, responsiveness, or polish -> UI refinement
- if the user asks for a dashboard or overview page -> dashboard
- if the user asks for login, signup, reset, verification, or route protection -> auth
- if the user asks for pricing, plans, subscriptions, or checkout -> billing
- if the user asks for first-run setup, activation, or guided steps -> onboarding
- if the user asks for filters, sorting, rows, pagination, or table UX -> table
- if the user asks for account, workspace, preferences, or configuration -> settings
- if the user asks for shared UI consistency or primitives -> design-system
- if the user asks for internal management or backoffice -> admin

Then select:
- one primary skill
- one primary agent
- one secondary skill only if clearly needed
- mandatory reviewer pass for medium/large tasks