# Shared Stock Selection Logic

Use this stock selection filter for all active tradebooks unless a setup explicitly overrides it.

For deciding what tradebooks apply to this stock today before checking stock filters, use [`tradebooks/shared/tradebook-decision.md`](tradebook-decision.md).

## Required filters

- Fresh news catalyst
- Market cap > $1 billion
- Elevated premarket volume
  - Must be over 1 million shares traded in premarket. Hard rule is more than 0.9 million shares to allow some buffer. And 1 million shares requirement is already very basic. If the premarket volume is low, it's not good for my open momentum style, large players will not be playing this stock at the open, no matter how good is other condition. 
  - If the stock traded less than 0.9 million shares during premarket, it should not be allowed for stock selection.

## Notes

- If a setup adds stricter stock selection conditions, those are additive (not replacements).
- If a setup-specific rule conflicts with this file, the setup-specific rule wins for that setup.
