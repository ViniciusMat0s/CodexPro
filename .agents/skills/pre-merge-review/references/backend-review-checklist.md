# Backend Review Checklist

## Handlers and services
- Are transport layers thin enough?
- Is business logic isolated appropriately?
- Are contracts explicit?

## Validation
- Are inputs checked?
- Are invalid states rejected early?

## Errors
- Are failure paths intentional?
- Are user-facing errors safe?
- Are internal details protected?

## Safety
- auth/authz considered
- secrets protected
- dangerous assumptions avoided