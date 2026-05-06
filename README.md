# plume-trade-ledger-forge

`plume-trade-ledger-forge` keeps a focused Zig implementation around trading systems. The project goal is to design a Zig verification harness for ledger systems, covering diagnostic reporting, negative fixtures, and failure-oriented tests.

## Purpose

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Plume Trade Ledger Forge Review Notes

`edge` and `stress` are the cases worth reading first. They show the optimistic and cautious ends of the fixture.

## What Is Covered

- `fixtures/domain_review.csv` adds cases for spread pressure and fill risk.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/plume-trade-ledger-walkthrough.md` walks through the case spread.
- The Zig code includes a review path for `portfolio drift` and `fill risk`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Implementation Notes

The repository has two validation layers: the original compact policy fixture and the domain review fixture. They are separate so one can change without hiding failures in the other.

The added Zig path is deliberately direct, with fixtures doing most of the explaining.

## Command

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Audit Path

The same command runs the local verification path. The highest-scoring domain case is `edge` at 220, which lands in `ship`. The most cautious case is `stress` at 141, which lands in `ship`.

## Limits

This remains a local project with deterministic fixtures. It does not depend on credentials, hosted services, or live data. Future work should add richer malformed inputs before widening the public API.
