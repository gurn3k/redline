# 4. Pre-signing only, not post-signing

## Decision

Redline v1 is used before the User signs, to decide whether to sign or push
back. It is not for someone who already signed and is now dealing with the
consequences.

## Alternatives

- Post-signing: help the User understand what they're now bound by and
  what leverage they have. This is where the research's best-quantified
  harms live (auto-renewal lock-in, arbitration blocking remedies, gig
  deactivation) and where demand is acute and motivated — a classic
  painkiller moment, versus pre-signing's vitamin/prevention framing.

## Why

The counter-offer feature only makes sense pre-signing — you can't
counter-offer a contract you already executed. Choosing pre-signing is a
bet that habit-building (getting Users to route documents through Redline
*before* they sign) is worth more long-term than capturing the acute,
easier-to-sell demand of someone already in trouble.

## Consequences

- Redline does not address the moment of highest documented harm (people
  discovering a bad clause after signing) or the moment of highest
  motivated willingness to pay.
- Product must actively build the pre-signing habit rather than rely on
  users arriving already in pain — this is a harder distribution problem
  than post-signing crisis-driven demand.
