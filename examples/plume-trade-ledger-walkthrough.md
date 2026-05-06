# Plume Trade Ledger Forge Walkthrough

The fixture is intentionally compact, so the review starts with the cases that pull farthest apart.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | spread pressure | 153 | ship |
| stress | fill risk | 141 | ship |
| edge | portfolio drift | 220 | ship |
| recovery | quote width | 211 | ship |
| stale | spread pressure | 159 | ship |

Start with `edge` and `stress`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

If `stress` becomes less cautious without a clear reason, I would inspect the drag input first.
