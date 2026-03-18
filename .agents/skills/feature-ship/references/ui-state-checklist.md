# UI State Checklist

For user-facing features, verify whether these states exist and feel intentional.

## Default state
- Clear hierarchy
- Obvious primary action
- Clean composition

## Loading state
- Not abrupt or confusing
- Skeleton, spinner, or loading feedback is appropriate
- Layout does not feel broken while loading

## Empty state
- Explains absence of data
- Suggests next step when possible
- Does not feel like an error

## Error state
- Explains what went wrong in useful terms
- Offers recovery path when possible
- Does not leak internal details

## Success state
- Gives clear completion feedback when relevant
- Confirms the action result
- Reduces uncertainty

## Disabled/submitting state
- Prevents accidental duplicate actions
- Clearly signals temporary non-interactivity

## Responsive state
- Layout still works at narrower widths
- Important actions remain accessible
- Hierarchy stays readable