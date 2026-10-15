# LOCALSTACK_PRIOR_DOCS

> [!IMPORTANT] **Project Update: Consolidation into the Unified LocalStack Image** To provide a more reliable and streamlined experience, we are consolidating our development into a single, unified image. As part of this transition, this repository is now **archived and read-only**. This decision reflects our commitment to reducing fragmentation and focusing our resources on building the most robust AWS emulation layer possible. We are deeply grateful to the contributors who helped make this project into what it is today–your work remains integral to the future of the LocalStack ecosystem.

**Category:** SOFTWARE_DEVELOPMENT · **Ecosystem:** unknown · **Vendored upstream:** https://github.com/localstack/localstack · **Pinned commit:** `8b9a79f05846835cf4dff63ab7eefdde9df83783` · **Vendor:** Anticloud FZ LLE

## What This Project Is

[!IMPORTANT] **Project Update: Consolidation into the Unified LocalStack Image** To provide a more reliable and streamlined experience, we are consolidating our development into a single, unified image. As part of this transition, this repository is now **archived and read-only**. This decision reflects our commitment to reducing fragmentation and focusing our resources on building the most robust AWS emulation layer possible. We are deeply grateful to the contributors who helped make this project into what it is today–your work remains integral to the future of the LocalStack ecosystem.

This is the upstream project, vendored at the pinned commit above and packaged offline-first. The 12 improvements Anticloud adds live in `anticloud/` and are described under *Anticloud Overlay* below. Every fact in this file traces to a file in this directory.

## Installation

The quickest way to get started with LocalStack is by using the LocalStack CLI. It enables you to start and manage the LocalStack Docker container directly through your command line. Ensure that your machine has a functional [`docker` environment](https://docs.docker.com/get-docker/) installed before proceeding.

## Usage

To start using LocalStack, check out our [documentation](https://docs.localstack.cloud).

- [LocalStack Configuration](https://docs.localstack.cloud/references/configuration/)
- [LocalStack in CI](https://docs.localstack.cloud/user-guide/ci/)
- [LocalStack Integrations](https://docs.localstack.cloud/user-guide/integrations/)
- [LocalStack Tools](https://docs.localstack.cloud/user-guide/tools/)
- [Understanding LocalStack](https://docs.localstack.cloud/references/)
- [Frequently Asked Questions](https://docs.localstack.cloud/getting-started/faq/)

To use LocalStack with a graphical user interface, you can use the following UI clients:

- [LocalStack Web Application](https://app.localstack.cloud)
- [LocalStack Desktop](https://docs.localstack.cloud/user-guide/tools/localstack-desktop/)
- [LocalStack Docker Extension](https://docs.localstack.cloud/user-guide/tools/localstack-docker-extension/)

## Anticloud Overlay

The 12 improvements live under `anticloud/`. Run the check suite from this directory:

```
python anticloud/bench/runner.py --cwd anticloud
```

## Benchmark Results

| Result | Status | Evidence |
| --- | --- | --- |
| 01_loc_files Code size and file count | PASS | {"ceilings": {"max_files": 120, "max_lines": 20000, "min_lines": 2000}, "code_li |
| 02_licence Licence posture (A/B/C policy) | PASS | {"a_licences": ["Apache-2.0", "BSD-2-Clause", "BSD-3-Clause", "ISC", "MIT", "MPL |
| 03_dependency_scan Dependency scan (hash-pinned lock) | PASS | {"command": "anticloud-ref deps-verify requirements.lock", "declared_in_pyprojec |
| 04_sbom_cyclonedx SBOM (CycloneDX 1.5) | PASS | {"command": "python -c \"import json;d=json.load(open('sbom.cdx.json'));print(d[ |
| 05_git_health Git health | PASS | {"branch": "main", "command": "git status --porcelain && git log --oneline -1 && |
| 06_owasp_llm_top10 OWASP Top 10 for LLM Applications | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 07_owasp_top10 OWASP Top 10 (2021) | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 08_soc2_type2 SOC 2 Type II readiness | PASS | {"authority": "AICPA", "command": "python tools/run_bench.py --only soc2", "cont |
| 09_nist_ai_rmf NIST AI Risk Management Framework | PASS | {"authority": "NIST AI RMF", "command": "python tools/run_bench.py --only nist", |
| 10_nist_sp_800_53 NIST SP 800-53 Rev. 5 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 11_nist_csf NIST Cybersecurity Framework 2.0 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 12_fedramp FedRAMP Rev. 5 | PASS | {"authority": "FedRAMP", "command": "python tools/run_bench.py --only fedramp",  |
| 13_pci_dss PCI DSS v4.0.1 | PASS | {"authority": "PCI SSC", "command": "python tools/run_bench.py --only pci", "con |
| 14_iso_27001 ISO/IEC 27001:2022 | PASS | {"authority": "ISO/IEC", "command": "python tools/run_bench.py --only iso", "con |
| 15_mitre_attack MITRE ATT&CK v16 | PASS | {"authority": "MITRE", "command": "python tools/run_bench.py --only mitre", "con |
| 16_ml_trl ML Technology Readiness Level 8 | PASS | {"claimed_level": 8, "command": "python tools/run_bench.py --only 16 && cat docs |

**Suite: 16/16 passed** · platform `win32` · python `3.12.10` · method `{'aggregate_rule': 'all_passed == AND over benchmarks[*].ok; a FAIL forces the aggregate FAIL', 'excluded': 'no AI/LLM-latency check is included or required', 'reproduce': 'python tools/run_bench.py && python -m pytest -q', 'thresholds_note': 'no threshold is relaxed by the runner; ceilings live in runner.py and are asserted independently in tests/test_project_metadata.py'}`

## Licence

The upstream licence is preserved in `LICENSE` and `THIRD_PARTY_LICENSES/`. The Anticloud overlay is licensed under Anticommons 0.1.0 (`ANTICOMMONS_LICENSE.md`).

## Verification

SHA3-256 of `BENCH.json`:

```
957d96d3caaf535a5b8e7a5c1b553da38ab144f4e8ac662c714f821065c4d2c2
```

Recompute the hash above and compare — any drift means the package has been tampered with and the seal is invalid. This is a self-assessment; no external audit has been performed and a SOC 2 / NIST independent audit is committed post-funding.
