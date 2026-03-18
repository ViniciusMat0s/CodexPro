# Auth Security Checklist

## Sensitive boundaries
- No secrets in client code
- No unsafe trust in client claims
- Route protection enforced properly

## Error handling
- Avoid leaking internal auth details
- Avoid user enumeration signals when possible

## Token/session behavior
- Expiration handled
- Invalid links handled
- Stale state handled
- Redirects not overly permissive

## Review
- Auth is not authorization
- Protected actions checked server-side where needed