# 5. Severity test covers existential risk, not just dollar amount

## Decision

A clause is **Dangerous** when it creates either (a) open-ended financial
exposure the User can't cap in advance, or (b) existential/relationship-
ending risk (e.g. unilateral termination with no cause and no cure period)
— in both cases only where the User lacks realistic leverage to negotiate
it out. A clause is **Unusual** when it deviates from market norms but the
exposure is bounded and non-existential.

## Alternatives

- Severity defined strictly by uncapped financial exposure. Simpler to
  implement and explain, but misses clauses with no dollar figure that can
  still end the User's core business relationship — the exact pattern
  behind the research's gig-deactivation evidence (nearly half of
  deactivated workers later found blameless).

## Why

Restricting "Dangerous" to dollar-denominated exposure would under-flag a
class of clause the research shows causes real harm just as often as
financial ones: loss of a critical vendor or client relationship with no
recourse.

## Consequences

- Flagging logic needs two independent checks, not one: an exposure-
  ceiling check and a relationship-termination check. Either can qualify a
  clause as Dangerous.
- Unilateral termination / no-cause deactivation clauses are now explicitly
  in the "always evaluate for Dangerous" set even absent a dollar figure.
