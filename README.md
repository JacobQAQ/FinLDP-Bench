# FinLDP-Bench

This build contains 50,000 augmented benchmark samples constructed from 419
unique source reports in five financial verticals.

## Construction

1. Source reports are sorted chronologically within each vertical.
2. The earlier approximately 90% form the training source pool; the later
   approximately 10% form the held-out source pool.
3. Each vertical contains 9,000 training augmented-report samples. Each sample
   is derived from one training source report by paragraph drop and optional
   paragraph-order reversal.
4. Each vertical contains 1,000 test instances in `(q, H, Y)` format. `H`
   contains two augmented reports from two distinct training source reports.
   `Y` is an unmodified held-out source report and is used only for evaluation.
5. `q` is generated from domain, report type, target date, target objects, and
   output requirements; it is not generated from `Y`.

See `manifest.json` for parameters and `audits/leakage_report.json` for checks.
