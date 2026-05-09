# Tradebook Index

## Purpose

This folder contains the active trading setup definitions used by Codex for trade review, tradebook maintenance, and broader trading analysis.

Each tradebook file should describe one setup clearly enough that Codex can:

- identify the setup
- distinguish valid vs invalid examples
- review execution quality
- separate A+ conditions from lower-quality conditions
- preserve the user's terminology and edge

## Active tradebooks

- `gap_and_go.md`
- `gap_give_and_go.md`
- `gap_and_crap.md`

Add new files here as the system grows.

## Shared reference docs

- [`shared/trading-philosophy.md`](shared/trading-philosophy.md)
- [`shared/stock-selection.md`](shared/stock-selection.md)
- [`shared/tradebook-decision.md`](shared/tradebook-decision.md)

## Standard structure for each tradebook

Each tradebook should try to include the following sections:

1. **Setup summary**
  What the setup is in plain language.
2. **Core idea**
  Why the setup works and what market behavior it is trying to capture.
3. **Market context**
  Conditions where the setup is most relevant.
4. **Key reference levels**
  Important price levels used to validate or invalidate the setup.
5. **Entry criteria**
  What must happen before entry is valid.
6. **A+ conditions**
  What makes the setup especially high quality.
7. **Lower-quality conditions**
  Signs the setup is weaker, less clean, or more likely to fail.
8. **Invalidation criteria**
  What behavior weakens or disables the setup thesis.
9. **Risk and stop logic**
  How risk should be defined using structure.
10. **Management rules**
  How the trade should be managed after entry.
11. **Exit logic**
  What conditions justify reducing or closing the trade.
12. **Common failure modes**
  Frequent mistakes or misreads associated with the setup.
13. **Review checklist**
  Questions to ask when reviewing a trade from this setup.
14. **Notes**
  Extra nuance, future refinements, screenshots to add later, or examples.

## Naming rules

- Use one file per setup.
- Use lowercase kebab-case filenames.
- Keep names aligned with the actual terminology used in reviews and data files.

Examples:

- `gap_and_go.md`
- `gap_give_and_go.md`
- `gap_and_crap.md`
- `vwap-bounce-fail.md`
- `key-level-open-vwap-breakout.md`

## Writing rules

When updating a tradebook:

- preserve the user's actual setup logic
- do not replace specific rules with generic trading advice
- separate hard rules from softer contextual clues
- keep invalidation rules explicit
- keep long and short logic separate unless the setup is intentionally dual-sided

## Source of truth

If there is a conflict:

1. the current active tradebook file is the main source of truth
2. older notes should be treated as historical context, not automatic authority
3. ambiguous rules should be rewritten more clearly rather than loosely interpreted

## Future expansion

This folder may later include:

- screenshot examples
- annotated charts
- setup-specific review templates
- archived versions of older tradebooks
- setup metadata in JSON or YAML
