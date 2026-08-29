# 9. Show an explicit Clear result, never silence

## Decision

When a document trips no Dangerous or Unusual flags, Redline shows an
explicit, specific Clear result with a brief explanation of what was
checked — the standard clause set (ADR 0006) and the User's own red-lines
list. An empty flags list or silent non-result is never shown.

## Alternatives

- Show nothing when there's nothing to flag — simpler, but ambiguous:
  the User can't tell whether Redline checked thoroughly or just failed to
  find anything.

## Why

Most documents are genuinely fine, and a tool that always finds something
stops being believed (Q7/ADR 0007). But silence is equally corrosive in
the other direction — it can't be distinguished from "didn't check." A
positive, falsifiable "checked against X and Y, found nothing" claim gives
the User something to trust or push back on, unlike an absence of output.

## Consequences

- The User's red-lines list now has a second job beyond driving analysis:
  it's what makes a Clear result feel checked rather than absent.
- Clear needs its own UI/copy surface as a first-class result, not just
  an empty state derived from an empty flags list.
