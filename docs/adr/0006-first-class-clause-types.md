# 6. First-class clause types: personal guarantee, indemnification, auto-renewal

## Decision

v1 builds specific detection heuristics and specific counter-offer language
for three clause types: personal guarantee, indemnification, and
auto-renewal. Arbitration/class-action waivers and liability caps get
generic catch-all detection only.

## Alternatives

- Prioritize by evidence strength instead: arbitration/class-action
  waivers are the research's single highest-confidence, most cross-cutting
  finding (it removes the remedy for every other flagged clause). Building
  deep logic for it first would follow the evidence more directly than
  building for personal guarantee and indemnification, which the research
  rates low-to-medium confidence with no verified dollar-figure cases.

## Why

The three chosen clause types map directly onto what this User (a small
business owner reviewing incoming paper — vendor/service contracts,
commercial leases) actually signs. Non-compete and IP assignment skew
toward individual employees/freelancers (out of scope per ADR 0002);
data-privacy overreach and unilateral-deactivation patterns skew toward
consumer/platform contracts this User doesn't sign. This is a deliberate
bet on document-type fit over evidence strength.

## Consequences

- Arbitration/class-action waivers get only generic detection in v1,
  despite being the best-evidenced, most cross-cutting finding in the
  research — a document could contain a real arbitration trap that
  Redline under-flags relative to its actual danger.
- If usage data later shows arbitration clauses appearing often in what
  Users actually upload, this prioritization should be revisited.
