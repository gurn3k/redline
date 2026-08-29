# 8. Confidence lives in the gate, not in the wording

## Decision

A flag that clears the Dangerous/Unusual bar and has a valid citation
(ADR 0001) is stated in plain, direct language with no hedge words. There
is no lower-confidence, softer-worded tier — a flag either clears the bar
and is shown plainly, or it doesn't and is not shown at all (ADR 0007).

## Alternatives

- Hedge proportionally to model confidence ("may potentially", "could be
  interpreted as"). Reflects uncertainty honestly but reintroduces the
  problem ADR 0007 exists to solve: hedged language is safe and useless.

## Why

If a flag is shown, it already met the criteria to be addressed — hedging
its wording afterward only undermines the validity of a flag that already
passed the bar. Confidence is a per-flag binary decided once, at
generation time, not a dial the model turns per sentence.

## Consequences

- Redline will occasionally state something plainly and be wrong — a
  citation can be accurate but the severity judgment on top of it still
  mistaken. Plain language raises the cost of that failure mode, since a
  confidently wrong flag reads as more authoritative than a hedged one.
- No UI or copy should introduce a "possible risk" or "worth checking"
  middle tier — that would recreate hedging outside the prose.
