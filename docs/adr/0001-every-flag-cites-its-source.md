# 1. Every flag cites its source

## Decision

Every risk flag Redline produces must quote the exact sentence from the
uploaded document that it is based on. A flag whose source sentence cannot
be shown is treated as a bug, not a formatting preference — it should not
reach the user.

## Alternatives

- Let the model describe risks in its own words, with no quoted sentence
  attached.
- Quote a source sentence only "when available," falling back to an
  unquoted summary otherwise.
- Cite a paragraph or section number instead of the exact sentence.

## Why

A reader can take the quoted sentence, find it in the document themselves,
and check that it says what Redline claims it says — without trusting our
summary or our judgment about severity. The verification step lives in the
document, not in us. This is the difference between "Redline says this is
risky" and "here is the sentence, judge for yourself."

## Consequences

- The model's output must be structured so each flag carries a verifiable
  quote, not free-text risk commentary.
- We need a way to confirm a quoted sentence actually appears in the
  source text before a flag is shown — a flag with a fabricated or
  paraphrased "quote" is the exact failure this decision exists to prevent.
- Any risk we believe is real but can't tie to a specific sentence has to
  be dropped, not softened into a vaguer claim. This caps recall in favor
  of trust.
- Testing has to check citation accuracy, not just whether a flag was
  produced — a flag with a wrong or missing quote is a failing test.
