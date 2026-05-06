# Field Notes

I would read this project from the data inward: cases first, implementation second.

The domain cases cover `spread pressure`, `fill risk`, `portfolio drift`, and `quote width`. They sit beside the smaller starter fixture so the project has both a compact scoring check and a domain-flavored review check.

`edge` is the strongest case at 220 on `portfolio drift`. `stress` is the cautious anchor at 141 on `fill risk`.

The extra check gives the repository a behavior path that can fail for a domain reason, not only a syntax reason.
