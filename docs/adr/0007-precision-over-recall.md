# 7. Precision over recall: prefer missing a risk to flagging a harmless clause

## Decision

Redline is tuned to prefer false negatives (missing a real risk) over false
positives (flagging a harmless clause). When a potential flag doesn't
clearly clear the Dangerous/Unusual bar, it is dropped, not shown with
lower confidence.

## Alternatives

- Prefer recall: flag liberally, let the User judge. Catches more real
  risk but produces more noise on the many documents that are genuinely
  fine.

## Why

ADR 0001 already commits to this bias structurally — a real risk that
can't be tied to a cited sentence is dropped, not softened into a vaguer
claim. This extends the same logic to the general error trade-off.
Over-flagging on the many documents that are genuinely fine undermines
trust in every flag Redline produces; an unbelieved tool catches nothing,
regardless of its raw recall.

## Consequences

- Redline will, by design, sometimes stay silent on a clause that later
  hurts the User — the precise harm the product exists to prevent — in
  exchange for the flags it does show being trustworthy.
- Flag-generation logic needs an explicit confidence gate, not just a
  severity score: below the gate, no flag is shown at all.
