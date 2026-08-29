# Redline

Redline reviews a contract a user is about to sign: a plain-English summary, severity-ranked risk flags with source citations, and a counter-offer per flag.

## Language

**User**:
A small business owner deciding whether to sign a contract someone else has presented to them, before they sign it. Not a freelancer, not a renter, and not someone who already signed and is now dealing with the consequences.
_Avoid_: Customer, client, subscriber

**Incoming paper**:
A contract or agreement someone else has presented to the User for signature. This is what Redline reviews.
_Avoid_: Document, contract (use Incoming paper when the distinction from Outgoing paper matters)

**Outgoing paper**:
A contract or agreement the User drafts or issues to someone else. Out of scope for v1 — Redline does not review it.

**Dangerous** (severity tier):
A clause that creates either open-ended financial exposure the User can't cap in advance, or existential risk to the business relationship (e.g. termination with no cause and no cure period) — in both cases only where the User has no realistic leverage to negotiate it out.
_Avoid_: High-risk, red flag

**Unusual** (severity tier):
A clause that deviates from typical market terms but the exposure is bounded, non-existential, or standard practice in that industry.
_Avoid_: Minor, low-risk, notable

**Clear** (result state):
The explicit, positive result shown when a document trips no Dangerous or Unusual flags against the standard clause checks and the User's own red lines. Always shown with a brief explanation of what was checked — never rendered as silence or an empty list.
_Avoid_: No issues found, all clear
