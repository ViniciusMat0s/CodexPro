# Regression Checklist

## After fixing the issue
- Could this break a nearby flow?
- Does this alter a shared contract?
- Does this affect loading/error/success states?
- Does this affect permissions or auth?
- Does this affect form validation?
- Does this affect responsive or conditional UI behavior?

## Protection
- Should a test be added?
- Should validation be tightened?
- Are manual QA steps needed?
- Is there another code path with the same defect pattern?