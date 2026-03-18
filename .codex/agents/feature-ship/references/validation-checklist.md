# Validation Checklist

## Inputs
- Are important inputs validated?
- Are required fields explicit?
- Are data formats enforced?

## Contracts
- Are request/response shapes predictable?
- Do UI assumptions match backend expectations?
- Are nullable/optional fields handled intentionally?

## Error handling
- Are validation failures surfaced clearly?
- Are unsafe values rejected early?
- Are failure cases predictable to the caller?

## Security
- Is input trusted too easily anywhere?
- Are auth/authorization boundaries respected?
- Are secrets and sensitive values kept out of client paths?