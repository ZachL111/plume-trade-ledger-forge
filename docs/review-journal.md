# Review Journal

The repository goal stays the same: design a Zig verification harness for ledger systems, covering diagnostic reporting, negative fixtures, and failure-oriented tests. This note explains the added review angle.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its trading systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `spread pressure`, score 153, lane `ship`
- `stress`: `fill risk`, score 141, lane `ship`
- `edge`: `portfolio drift`, score 220, lane `ship`
- `recovery`: `quote width`, score 211, lane `ship`
- `stale`: `spread pressure`, score 159, lane `ship`

## Note

This file is intentionally plain so the fixture remains the source of truth.
