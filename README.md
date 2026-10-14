# LOCALSTACK PRIOR DOCS

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-software_development-lightgrey)

> Anticloud-hardened packaging of the upstream project `LOCALSTACK_PRIOR_DOCS` in category **SOFTWARE DEVELOPMENT**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SOFTWARE DEVELOPMENT · **Upstream:** https://github.com/localstack/localstack · **Upstream pin:** `8b9a79f05846835cf4dff63ab7eefdde9df83783` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

> [!IMPORTANT]
> **Project Update: Consolidation into the Unified LocalStack Image**
>
> To provide a more reliable and streamlined experience, we are consolidating our development into a single, unified image. As part of this transition, this project is now **archived and read-only**.
>
> This decision reflects our commitment to reducing fragmentation and focusing our resources on building the most robust AWS emulation layer possible. We are deeply grateful to the contributors who helped make this project into what it is today–your work remains integral to the future of the LocalStack ecosystem.
>
> What this means for your workflow:
>
> - LocalStack for AWS offers a [range of options](https://www.localstack.cloud/pricing) including a free Hobby plan for non-commercial use with the same capabilities as this project.
> - Your input is still vital to us. Please continue to share [bug reports here](https://github.com/orgs/localstack/discussions/categories/bugs) and [submit feature requests here](https://github.com/orgs/localstack/discussions/categories/feature-requests) or join our [Slack Community](https://slack.localstack.cloud).
>
> Thank you for your continued support as we grow together.

<p align="center">
  <img src="docs/localstack-readme-banner.svg" alt="LocalStack - The Leading Platform for Local Cloud Development">
</p>

<p align="center">
  <a href="https://github.com/localstack/localstack/actions/workflows/aws-main.yml?query=branch%3Amain"><img alt="GitHub Actions" src="https://github.com/localstack/localstack/actions/workflows/aws-main.yml/badge.svg?branch=main"></a>
  <a href="https://coveralls.io/github/localstack/localstack?branch=main"><img alt="Coverage Status" src="https://coveralls.io/projects/github/localstack/localstack/badge.svg?branch=main"></a>
  <a href="https://pypi.org/project/localstack/"><img alt="PyPI Version" src="https://img.shields.io/pypi/v/localstack?color=blue"></a>
  <a href="https://hub.docker.com/r/localstack/localstack"><img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/localstack/localstack"></a>
  <a href="https://pypi.org/project/localstack"><img alt="PyPi downloads" src="https://static.pepy.tech/badge/localstack"></a>
  <a href="https://img.shields.io/pypi/l/localstack.svg"><img alt="PyPI License" src="https://img.shields.io/pypi/l/localstack.svg"></a>
  <a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
  <a href="https://github.com/astral-sh/ruff"><img alt="Ruff" src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json"></a>
  <a href="https://bsky.app/profile/localstack.cloud"><img alt="Bluesky" src="https://img.shields.io/badge/bluesky-Follow-blue?logo=bluesky"></a>
</p>

<p align="center">
  LocalStack is a cloud software development framework to develop and test your AWS applications locally.
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#install">Install</a> •
  <a href="#quickstart">Quickstart</a> •
  <a href="#running">Run</a> •
  <a href="#usage">Usage</a> •
  <a href="#releases">Releases</a> •
  <a href="#contributing">Contributing</a>
  <br/>
  <a href="https://docs.localstack.cloud" target="_blank">📖 Docs</a> •
  <a href="https://www.localstack.cloud/localstack-for-aws" target="_blank">💻 LocalStack for AWS</a> •
  <a href="https://docs.localstack.cloud/references/coverage/" target="_blank">☑️ LocalStack coverage</a>
</p>

---

# Overview

[LocalStack](https://localstack.cloud) is a cloud service emulator that runs in a single container on your laptop or in your CI environment. With LocalStack, you can run your AWS applications or Lambdas entirely on your local machine without connecting to a remote cloud provider! Whether you are testing complex CDK applications or Terraform configurations, or just beginning to learn about AWS services, LocalStack helps speed up and simplify your testing and development workflow.

LocalStack supports a growing number of AWS services, like AWS Lambda, S3, DynamoDB, Kinesis, SQS, SNS, and many more! The [Pro version of LocalStack](https://localstack.cloud/pricing) supports additional APIs and advanced features. You can find a comprehensive list of supported APIs on our [☑️ Feature Coverage](https://docs.localstack.cloud/user-guide/aws/feature-coverage/) page.

LocalStack also provides additional features to make your life as a cloud developer easier! Check out LocalStack's [User Guides](https://docs.localstack.cloud/user-guide/) for more information.

## Install

The quickest way to get started with LocalStack is by using the LocalStack CLI. It enables you to start and manage the LocalStack Docker container directly through your command line. Ensure that your machine has a functional [`docker` environment](https://docs.docker.com/get-docker/) installed before proceeding.

### Brew (macOS or Linux with Homebrew)

Install the LocalStack CLI through our [official LocalStack Brew Tap](https://github.com/localstack/homebrew-tap):

```bash
brew install localstack/tap/localstack-cli
```

### Binary download (macOS, Linux, Windows)

If Brew is not installed on your machine, you can download the pre-built LocalStack CLI binary directly:

- Visit [localstack/localstack-cli](https://github.com/localstack/localstack-cli/releases/latest) and download the latest release for your platform.
- Extract the downloaded archive to a directory included in your `PATH` variable:
  - For macOS/Linux, use the command: `sudo tar xvzf ~/Downloads/localstack-cli-*-darwin-*-onefile.tar.gz -C /usr/local/bin`

### PyPI (macOS, Linux, Windows)

LocalStack is developed using Python. To install the LocalStack CLI using `pip`, run the following command:

```bash
python3 -m pip install localstack
```

The `localstack-cli` installation enables you to run the Docker image containing the LocalStack runtime. To interact with the local AWS services, you need

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python** (manifests: pyproject.toml; scanned in UPSTREAM_CLONE)
- Top-level source layout: `bin/`, `localstack-core/`, `scripts/`, `tests/`
- Snapshot size: **3692 files**, **468178 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (1939), `.json` (645), `.json5` (545), `.yaml` (177), `.yml` (142), `(none)` (70)
- Upstream commit pinned for this packaging: `8b9a79f05846835cf4dff63ab7eefdde9df83783`

---

## Installation

>
> What this means for your workflow:
>
> - LocalStack for AWS offers a [range of options](https://www.localstack.cloud/pricing) including a free Hobby plan for non-commercial use with the same capabilities as this project.
> - Your input is still vital to us. Please continue to share [bug reports here](https://github.com/orgs/localstack/discussions/categories/bugs) and [submit feature requests here](https://github.com/orgs/localstack/discussions/categories/feature-requests) or join our [Slack Community](https://slack.localstack.cloud).
>
> Thank you for your continued support as we grow together.

<p align="center">
  <img src="docs/localstack-readme-banner.svg" alt="LocalStack - The Leading Platform for Local Cloud Development">
</p>

<p align="center">
  <a href="https://github.com/localstack/localstack/actions/workflows/aws-main.yml?query=branch%3Amain"><img alt="GitHub Actions" src="https://github.com/localstack/localstack/actions/workflows/aws-main.yml/badge.svg?branch=main"></a>
  <a href="https://coveralls.io/github/localstack/localstack?branch=main"><img alt="Coverage Status" src="https://coveralls.io/projects/github/localstack/localstack/badge.svg?branch=main"></a>
  <a href="https://pypi.org/project/localstack/"><img alt="PyPI Version" src="https://img.shields.io/pypi/v/localstack?color=blue"></a>
  <a href="https://hub.docker.com/r/localstack/localstack"><img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/localstack/localstack"></a>
  <a href="https://pypi.org/project/localstack"><img alt="PyPi downloads" src="https://static.pepy.tech/badge/localstack"></a>
  <a href="https://img.shields.io/pypi/l/localstack.svg"><img alt="PyPI License" src="https://img.shields.io/pypi/l/localstack.svg"></a>
  <a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
  <a href="https://github.com/astral-sh/ruff"><img alt="Ruff" src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json"></a>
  <a href="https://bsky.app/profile/localstack.cloud"><img alt="Bluesky" src="https://img.shields.io/badge/bluesky-Follow-blue?logo=bluesky"></a>
</p>

<p align="center">
  LocalStack is a cloud software development framework to develop and test your AWS applications locally.
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#install">Install</a> •
  <a href="#quickstart">Quickstart</a> •
  <a href="#running">Run</a> •
  <a href="#usage">Usage</a> •
  <a href="#releases">Releases</a> •
  <a href="#contributing">Contributing</a>
  <br/>
  <a href="https://docs.localstack.cloud" target="_blank">📖 Docs</a> •
  <a href="https://www.localstack.cloud/localstack-for-aws" target="_blank">💻 LocalStack for AWS</a> •
  <a href="https://docs.localstack.cloud/references/coverage/" target="_blank">☑️ LocalStack coverage</a>
</p>

---

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

> - Your input is still vital to us. Please continue to share [bug reports here](https://github.com/orgs/localstack/discussions/categories/bugs) and [submit feature requests here](https://github.com/orgs/localstack/discussions/categories/feature-requests) or join our [Slack Community](https://slack.localstack.cloud).
>
> Thank you for your continued support as we grow together.

<p align="center">
  <img src="docs/localstack-readme-banner.svg" alt="LocalStack - The Leading Platform for Local Cloud Development">
</p>

<p align="center">
  <a href="https://github.com/localstack/localstack/actions/workflows/aws-main.yml?query=branch%3Amain"><img alt="GitHub Actions" src="https://github.com/localstack/localstack/actions/workflows/aws-main.yml/badge.svg?branch=main"></a>
  <a href="https://coveralls.io/github/localstack/localstack?branch=main"><img alt="Coverage Status" src="https://coveralls.io/projects/github/localstack/localstack/badge.svg?branch=main"></a>
  <a href="https://pypi.org/project/localstack/"><img alt="PyPI Version" src="https://img.shields.io/pypi/v/localstack?color=blue"></a>
  <a href="https://hub.docker.com/r/localstack/localstack"><img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/localstack/localstack"></a>
  <a href="https://pypi.org/project/localstack"><img alt="PyPi downloads" src="https://static.pepy.tech/badge/localstack"></a>
  <a href="https://img.shields.io/pypi/l/localstack.svg"><img alt="PyPI License" src="https://img.shields.io/pypi/l/localstack.svg"></a>
  <a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
  <a href="https://github.com/astral-sh/ruff"><img alt="Ruff" src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json"></a>
  <a href="https://bsky.app/profile/localstack.cloud"><img alt="Bluesky" src="https://img.shields.io/badge/bluesky-Follow-blue?logo=bluesky"></a>
</p>

<p align="center">
  LocalStack is a cloud software development framework to develop and test your AWS applications locally.
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#install">Install</a> •
  <a href="#quickstart">Quickstart</a> •
  <a href="#running">Run</a> •
  <a href="#usage">Usage</a> •
  <a href="#releases">Releases</a> •
  <a href="#contributing">Contributing</a>
  <br/>
  <a href="https://docs.localstack.cloud" target="_blank">📖 Docs</a> •
  <a href="https://www.localstack.cloud/localstack-for-aws" target="_blank">💻 LocalStack for AWS</a> •
  <a href="https://docs.localstack.cloud/references/coverage/" target="_blank">☑️ LocalStack coverage</a>
</p>

---

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

The upstream API surface is defined by the `LOCALSTACK_PRIOR_DOCS` source tree vendored in `UPSTREAM_CLONE/` (Python ecosystem). Public entry points:

- Source modules: `bin/`, `localstack-core/`, `scripts/`, `tests/`
- The snapshot declares 37 dependency references across 4 ecosystem(s); see Dependencies below.
- Overlay API: `anticloud/cli.py` exposes 13 subcommands with JSON stdout; `anticloud/bench/runner.py` runs the 16-check suite; `anticloud/provenance/chain.py` exposes the SHA3-256 + Ed25519 provenance chain.

---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python |
| Manifests detected | pyproject.toml |
| Files in snapshot | 3692 |
| Lines of code | 468178 |
| Dependency references | 37 |
| Dependencies by ecosystem | cargo: 18, go: 4, npm: 2, pypi: 13 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| pypi | asn1crypto | >=1.5.1 | pyproject.toml |
| pypi | click | >=8.2.0 | pyproject.toml |
| pypi | cachetools | >=5.0 | pyproject.toml |
| pypi | cryptography | - | pyproject.toml |
| pypi | dnslib | >=0.9.10 | pyproject.toml |
| pypi | dnspython | >=1.16.0 | pyproject.toml |
| pypi | plux | >=1.14.0 | pyproject.toml |
| pypi | psutil | >=5.4.8 | pyproject.toml |
| pypi | python-dotenv | >=0.19.1 | pyproject.toml |
| pypi | pyyaml | >=5.1 | pyproject.toml |
| pypi | rich | >=12.3.0 | pyproject.toml |
| pypi | requests | >=2.20.0 | pyproject.toml |
| pypi | semver | >=2.10 | pyproject.toml |
| cargo | name | bootstrap | tests/aws/services/lambda_/functions/rust-lambda/Cargo.toml |
| cargo | version | 0.1.0 | tests/aws/services/lambda_/functions/rust-lambda/Cargo.toml |
| ... | (22 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

> - Your input is still vital to us. Please continue to share [bug reports here](https://github.com/orgs/localstack/discussions/categories/bugs) and [submit feature requests here](https://github.com/orgs/localstack/discussions/categories/feature-requests) or join our [Slack Community](https://slack.localstack.cloud).
>
> Thank you for your continued support as we grow together.

<p align="center">
  <img src="docs/localstack-readme-banner.svg" alt="LocalStack - The Leading Platform for Local Cloud Development">
</p>

<p align="center">
  <a href="https://github.com/localstack/localstack/actions/workflows/aws-main.yml?query=branch%3Amain"><img alt="GitHub Actions" src="https://github.com/localstack/localstack/actions/workflows/aws-main.yml/badge.svg?branch=main"></a>
  <a href="https://coveralls.io/github/localstack/localstack?branch=main"><img alt="Coverage Status" src="https://coveralls.io/projects/github/localstack/localstack/badge.svg?branch=main"></a>
  <a href="https://pypi.org/project/localstack/"><img alt="PyPI Version" src="https://img.shields.io/pypi/v/localstack?color=blue"></a>
  <a href="https://hub.docker.com/r/localstack/localstack"><img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/localstack/localstack"></a>
  <a href="https://pypi.org/project/localstack"><img alt="PyPi downloads" src="https://static.pepy.tech/badge/localstack"></a>
  <a href="https://img.shields.io/pypi/l/localstack.svg"><img alt="PyPI License" src="https://img.shields.io/pypi/l/localstack.svg"></a>
  <a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
  <a href="https://github.com/astral-sh/ruff"><img alt="Ruff" src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json"></a>
  <a href="https://bsky.app/profile/localstack.cloud"><img alt="Bluesky" src="https://img.shields.io/badge/bluesky-Follow-blue?logo=bluesky"></a>
</p>

<p align="center">
  LocalStack is a cloud software development framework to develop and test your AWS applications locally.
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#install">Install</a> •
  <a href="#quickstart">Quickstart</a> •
  <a href="#running">Run</a> •
  <a href="#usage">Usage</a> •
  <a href="#releases">Releases</a> •
  <a href="#contributing">Contributing</a>
  <br/>
  <a href="https://docs.localstack.cloud" target="_blank">📖 Docs</a> •
  <a href="https://www.localstack.cloud/localstack-for-aws" target="_blank">💻 LocalStack for AWS</a> •
  <a href="https://docs.localstack.cloud/references/coverage/" target="_blank">☑️ LocalStack coverage</a>
</p>

---

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `LOCALSTACK_PRIOR_DOCS` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE.txt` in the upstream snapshot).

License file excerpt:

```text
Copyright (c) 2017+ LocalStack contributors
Copyright (c) 2016 Atlassian Pty Ltd

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `LOCALSTACK_PRIOR_DOCS` (category: SOFTWARE DEVELOPMENT)
- **Upstream URL:** https://github.com/localstack/localstack
- **Pinned commit (SHA):** `8b9a79f05846835cf4dff63ab7eefdde9df83783`
- **Branch:** main
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`b48d8dad6108d7b3875376a4f489ab6658b3162fa0dd61522a6404d6341f1519`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

