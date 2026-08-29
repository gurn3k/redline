# 10. Position as document literacy, not legal advice

## Decision

Redline is positioned everywhere — first run, every output screen, footer
copy — as explaining what a document says and flagging patterns grounded
in citations, not as legal advice, a lawyer, or a determination of what a
User should do or whether a clause is enforceable in their jurisdiction.
This applies to summaries, flags, the counter-offer drafts, the Q&A box,
and the Clear result alike.

## Alternatives

- No explicit positioning beyond standard ToS boilerplate — cheaper, but
  leaves Redline exposed to the same regulatory read DoNotPay got: an FTC
  settlement ($193K, Sept 2024) plus a 1.8/5 Trustpilot score for
  overstating what its "robot lawyer" could actually do.
- Hedge the product itself (softer language, lower-confidence framing) to
  reduce UPL exposure — rejected, since it directly conflicts with ADR
  0008's confidence-in-the-gate decision.

## Why

Every decision made in this session pushes Redline toward sounding more
authoritative, not less: confident unhedged language (ADR 0008), a drafted
counter-offer per flag, severity framed around "danger." The more
precisely Redline nails the confident-and-correct case, the more it reads
as practicing law rather than summarizing one. ADR 0001's citation
requirement is the load-bearing mitigation here, not an add-on disclaimer:
Redline's structural claim is "here is the sentence, judge for yourself,"
not "trust our legal judgment" — the positioning just needs to say that
plainly rather than leave it implicit.

Rather than softening the product to reduce this risk, the fix is in
framing: counter-offer drafts are "example language you could propose,"
not "the legally correct fix"; flags describe what the text says and a
pattern it matches, not whether it's enforceable; nothing is phrased as a
guarantee of outcome.

## Consequences

- Every flag, counter-offer, and Q&A answer needs copy that references the
  cited sentence as the thing being explained, not a freestanding verdict.
- Jurisdiction is an open gap: clause patterns are flagged the same way
  regardless of state, and enforceability genuinely varies by state. This
  ADR does not resolve that — it should be revisited before launch,
  either with per-jurisdiction caveats or an explicit "patterns, not
  jurisdiction-specific enforceability" disclaimer.
- Existing competitors' "0–100 risk score" framing (Pact, ClauseGuard) is
  deliberately not adopted — false numeric precision is its own overclaim
  risk; Dangerous/Unusual/Clear (ADR 0005, 0009) stays qualitative.
