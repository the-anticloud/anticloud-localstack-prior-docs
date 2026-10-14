# Educators — LOCALSTACK_PRIOR_DOCS

**Project:** LOCALSTACK_PRIOR_DOCS  
**Category:** SOFTWARE_DEVELOPMENT  
**Upstream:** https://github.com/localstack/localstack  
**Pinned commit:** `8b9a79f05846835cf4dff63ab7eefdde9df83783`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `6300f72a9c708e797854bd6e8128c5caf696b07e2574267311686347f9efa504`  
**Date:** October 2026

## Teaching with LOCALSTACK_PRIOR_DOCS

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `6300f72a9c708e797854bd6e8128c5caf696b07e2574267311686347f9efa504` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
