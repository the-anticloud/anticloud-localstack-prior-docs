# Ethics — LOCALSTACK_PRIOR_DOCS

**Project:** LOCALSTACK_PRIOR_DOCS  
**Category:** SOFTWARE_DEVELOPMENT  
**Upstream:** https://github.com/localstack/localstack  
**Pinned commit:** `8b9a79f05846835cf4dff63ab7eefdde9df83783`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `6300f72a9c708e797854bd6e8128c5caf696b07e2574267311686347f9efa504`  
**Date:** October 2026

## Position

LOCALSTACK_PRIOR_DOCS is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
