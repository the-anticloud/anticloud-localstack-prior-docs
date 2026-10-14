# Students — LOCALSTACK_PRIOR_DOCS

**Project:** LOCALSTACK_PRIOR_DOCS  
**Category:** SOFTWARE_DEVELOPMENT  
**Upstream:** https://github.com/localstack/localstack  
**Pinned commit:** `8b9a79f05846835cf4dff63ab7eefdde9df83783`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `6300f72a9c708e797854bd6e8128c5caf696b07e2574267311686347f9efa504`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `8b9a79f05846835cf4dff63ab7eefdde9df83783`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `6300f72a9c708e797854bd6e8128c5caf696b07e2574267311686347f9efa504`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
