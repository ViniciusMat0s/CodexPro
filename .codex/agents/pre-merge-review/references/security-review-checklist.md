# Security Review Checklist

## Inputs and trust boundaries
- Is user input validated?
- Is external input trusted too early?
- Are contracts explicit?

## Auth and authorization
- Does the code enforce access properly?
- Could users do something they should not?

## Secrets and sensitive data
- Any tokens or secrets exposed?
- Any sensitive data leaking to client/UI/logs?

## Dangerous patterns
- unsafe serialization/deserialization
- unverified webhooks
- insecure file handling
- unguarded mutations
- weak assumption about current user/account context