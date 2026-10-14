# YT DLP

![license](https://img.shields.io/badge/license-Unlicense-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-social_media-lightgrey)

> Anticloud-hardened packaging of the upstream project `YT_DLP` in category **SOCIAL MEDIA**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SOCIAL MEDIA · **Upstream:** https://github.com/yt-dlp/yt-dlp · **Upstream pin:** `51bab8a0116f4d8004c315706d809782607d5847` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
<div align="center">

[![YT-DLP](https://raw.githubusercontent.com/yt-dlp/yt-dlp/master/.github/banner.svg)](#readme)

[![Release version](https://img.shields.io/github/v/release/yt-dlp/yt-dlp?color=brightgreen&label=Latest&style=for-the-badge)](#installation "Installation")
[![Python Version](https://img.shields.io/python/required-version-toml?tomlFilePath=https%3A%2F%2Fraw.githubusercontent.com%2Fyt-dlp%2Fyt-dlp%2Frefs%2Fheads%2Fmaster%2Fpyproject.toml&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/blob/master/pyproject.toml "Python Version")
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp "PyPI")
[![Discord](https://img.shields.io/badge/Discord-%235865F2.svg?&logo=discord&logoColor=white&style=for-the-badge)](https://discord.gg/H5MNcFW63r "Discord")
[![License: Unlicense](https://img.shields.io/badge/-Unlicense-red.svg?style=for-the-badge)](LICENSE "License")
[![Commits](https://img.shields.io/github/commit-activity/m/yt-dlp/yt-dlp?label=commits&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/commits "Commit History")

</div>
<!-- MANPAGE: END EXCLUDED SECTION -->

yt-dlp is a feature-rich command-line audio/video downloader with support for [thousands of sites](supportedsites.md). The project is a fork of [youtube-dl](https://github.com/ytdl-org/youtube-dl) based on the now inactive [youtube-dlc](https://github.com/blackjack4494/yt-dlc).

<!-- MANPAGE: MOVE "USAGE AND OPTIONS" SECTION HERE -->

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
* [INSTALLATION](#installation)
    * [Detailed instructions](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
    * [Release Files](#release-files)
    * [Update](#update)
    * [Dependencies](#dependencies)
    * [Compile](#compile)
* [USAGE AND OPTIONS](#usage-and-options)
    * [General Options](#general-options)
    * [Network Options](#network-options)
    * [Geo-restriction](#geo-restriction)
    * [Video Selection](#video-selection)
    * [Download Options](#download-options)
    * [Filesystem Options](#filesystem-options)
    * [Thumbnail Options](#thumbnail-options)
    * [Internet Shortcut Options](#internet-shortcut-options)
    * [Verbosity and Simulation Options](#verbosity-and-simulation-options)
    * [Workarounds](#workarounds)
    * [Video Format Options](#video-format-options)
    * [Subtitle Options](#subtitle-options)
    * [Authentication Options](#authentication-options)
    * [Post-processing Options](#post-processing-options)
    * [SponsorBlock Options](#sponsorblock-options)
    * [Extractor Options](#extractor-options)
    * [Preset Aliases](#preset-aliases)
* [CONFIGURATION](#configuration)
    * [Configuration file encoding](#configuration-file-encoding)
    * [Authentication with netrc](#authentication-with-netrc)
    * [Notes about environment variables](#notes-about-environment-variables)
* [OUTPUT TEMPLATE](#output-template)
    * [Output template examples](#output-template-examples)
* [FORMAT SELECTION](#format-selection)
    * [Filtering Formats](#filtering-formats)
    * [Sorting Formats](#sorting-formats)
    * [Format Selection examples](#format-selection-examples)
* [MODIFYING METADATA](#modifying-metadata)
    * [Modifying metadata examples](#modifying-metadata-examples)
* [EXTRACTOR ARGUMENTS](#extractor-arguments)
* [PLUGINS](#plugins)
    * [Installing Plugins](#installing-plugins)
    * [Developing Plugins](#developing-plugins)
* [EMBEDDING YT-DLP](#embedding-yt-dlp)
    * [Embedding examples](#embedding-examples)
* [CHANGES FROM YOUTUBE-DL](#changes-from-youtube-dl)
    * [New features](#new-features)
    * [Differences in default behavior](#differences-in-default-behavior)
    * [Deprecated options](#deprecated-options)
* [CONTRIBUTING](CONTRIBUTING.md#contributing-to-yt-dlp)
    * [Opening an Issue](CONTRIBUTING.md#opening-an-issue)
    * [Developer Instructions](CONTRIBUTING.md#developer-instructions)
* [WIKI](https://github.com/yt-dlp/yt-dlp/wiki)
    * [FAQ](https://github.com/yt-dlp/yt-dlp/wiki/FAQ)
<!-- MANPAGE: END EXCLUDED SECTION -->

# INSTALLATION

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
[![Windows](https://img.shields.io/badge/-Windows_x64-blue.svg?style=for-the-badge&logo=windows)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)
[![Unix](https://img.shields.io/badge/-Linux/BSD-red.svg?style=for-the-badge&logo=linux)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)
[![MacOS](https://img.shields.io/badge/-MacOS-lightblue.svg?style=for-the-badge&logo=apple)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos)
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp)
[![Source Tarball](https://img.shields.io/badge/-Source_tar-green.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)
[![Other variants](https://img.shields.io/badge/-Other-grey.svg?style=for-the-badge)](#release-files)
[![All versions](https://img.shields.io/badge/-All_Versions-lightgrey.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases)
<!-- MANPAGE: END EXCLUDED SECTION -->

You can install yt-dlp using [the binaries](#release-files), [pip](https://pypi.org/project/yt-dlp) or one using a third-party package manager. See [the wiki](https://github.com/yt-dlp/yt-dlp/wiki/Installation) for detailed instructions

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
## RELEASE FILES

#### Recommended

File|Description
:---|:---
[yt-dlp](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)|Platform-independent [zipimport](https://docs.python.org/3/library/zipimport.html) binary. Needs Python (recommended for **Linux/BSD**)
[yt-dlp.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)|Windows (Win8+) standalone x64 binary (recommended for **Windows**)
[yt-dlp_macos](https:/

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python** (manifests: pyproject.toml; scanned in UPSTREAM_CLONE)
- Top-level source layout: `bundle/`, `devscripts/`, `test/`, `yt_dlp/`
- Snapshot size: **1149 files**, **229578 lines of code** (measured; see Benchmarks)
- Primary languages: `.py` (1070), `.yml` (30), `.txt` (18), `.md` (8), `(none)` (7), `.in` (3)
- Upstream commit pinned for this packaging: `51bab8a0116f4d8004c315706d809782607d5847`

---

## Installation

[![Python Version](https://img.shields.io/python/required-version-toml?tomlFilePath=https%3A%2F%2Fraw.githubusercontent.com%2Fyt-dlp%2Fyt-dlp%2Frefs%2Fheads%2Fmaster%2Fpyproject.toml&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/blob/master/pyproject.toml "Python Version")
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp "PyPI")
[![Discord](https://img.shields.io/badge/Discord-%235865F2.svg?&logo=discord&logoColor=white&style=for-the-badge)](https://discord.gg/H5MNcFW63r "Discord")
[![License: Unlicense](https://img.shields.io/badge/-Unlicense-red.svg?style=for-the-badge)](LICENSE "License")
[![Commits](https://img.shields.io/github/commit-activity/m/yt-dlp/yt-dlp?label=commits&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/commits "Commit History")

</div>
<!-- MANPAGE: END EXCLUDED SECTION -->

yt-dlp is a feature-rich command-line audio/video downloader with support for [thousands of sites](supportedsites.md). The project is a fork of [youtube-dl](https://github.com/ytdl-org/youtube-dl) based on the now inactive [youtube-dlc](https://github.com/blackjack4494/yt-dlc).

<!-- MANPAGE: MOVE "USAGE AND OPTIONS" SECTION HERE -->

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
* [INSTALLATION](#installation)
    * [Detailed instructions](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
    * [Release Files](#release-files)
    * [Update](#update)
    * [Dependencies](#dependencies)
    * [Compile](#compile)
* [USAGE AND OPTIONS](#usage-and-options)
    * [General Options](#general-options)
    * [Network Options](#network-options)
    * [Geo-restriction](#geo-restriction)
    * [Video Selection](#video-selection)
    * [Download Options](#download-options)
    * [Filesystem Options](#filesystem-options)
    * [Thumbnail Options](#thumbnail-options)
    * [Internet Shortcut Options](#internet-shortcut-options)
    * [Verbosity and Simulation Options](#verbosity-and-simulation-options)
    * [Workarounds](#workarounds)
    * [Video Format Options](#video-format-options)
    * [Subtitle Options](#subtitle-options)
    * [Authentication Options](#authentication-options)
    * [Post-processing Options](#post-processing-options)
    * [SponsorBlock Options](#sponsorblock-options)
    * [Extractor Options](#extractor-options)
    * [Preset Aliases](#preset-aliases)
* [CONFIGURATION](#configuration)
    * [Configuration file encoding](#configuration-file-encoding)
    * [Authentication with netrc](#authentication-with-netrc)
    * [Notes about environment variables](#notes-about-environment-variables)
* [OUTPUT TEMPLATE](#output-template)
    * [Output template examples](#output-template-examples)
* [FORMAT SELECTION](#format-selection)
    * [Filtering Formats](#filtering-formats)
    * [Sorting Formats](#sorting-formats)
    * [Format Selection examples](#format-selection-examples)
* [MODIFYING METADATA](#modifying-metadata)
    * [Modifying metadata examples](#modifying-metadata-examples)
* [EXTRACTOR ARGUMENTS](#extractor-arguments)
* [PLUGINS](#plugins)
    * [Installing Plugins](#installing-plugins)
    * [Developing Plugins](#developing-plugins)
* [EMBEDDING YT-DLP](#embedding-yt-dlp)
    * [Embedding examples](#embedding-examples)
* [CHANGES FROM YOUTUBE-DL](#changes-from-youtube-dl)
    * [New features](#new-features)
    * [Differences in default behavior](#differences-in-default-behavior)
    * [Deprecated options](#deprecated-options)
* [CONTRIBUTING](CONTRIBUTING.md#contributing-to-yt-dlp)
    * [Opening an Issue](CONTRIBUTING.md#opening-an-issue)
    * [Developer Instructions](CONTRIBUTING.md#developer-instructions)
* [WIKI](https://github.com/yt-dlp/yt-dlp/wiki)
    * [FAQ](https://github.com/yt-dlp/yt-dlp/wiki/FAQ)
<!-- MANPAGE: END EXCLUDED SECTION -->

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
* [INSTALLATION](#installation)
    * [Detailed instructions](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
    * [Release Files](#release-files)
    * [Update](#update)
    * [Dependencies](#dependencies)
    * [Compile](#compile)
* [USAGE AND OPTIONS](#usage-and-options)
    * [General Options](#general-options)
    * [Network Options](#network-options)
    * [Geo-restriction](#geo-restriction)
    * [Video Selection](#video-selection)
    * [Download Options](#download-options)
    * [Filesystem Options](#filesystem-options)
    * [Thumbnail Options](#thumbnail-options)
    * [Internet Shortcut Options](#internet-shortcut-options)
    * [Verbosity and Simulation Options](#verbosity-and-simulation-options)
    * [Workarounds](#workarounds)
    * [Video Format Options](#video-format-options)
    * [Subtitle Options](#subtitle-options)
    * [Authentication Options](#authentication-options)
    * [Post-processing Options](#post-processing-options)
    * [SponsorBlock Options](#sponsorblock-options)
    * [Extractor Options](#extractor-options)
    * [Preset Aliases](#preset-aliases)
* [CONFIGURATION](#configuration)
    * [Configuration file encoding](#configuration-file-encoding)
    * [Authentication with netrc](#authentication-with-netrc)
    * [Notes about environment variables](#notes-about-environment-variables)
* [OUTPUT TEMPLATE](#output-template)
    * [Output template examples](#output-template-examples)
* [FORMAT SELECTION](#format-selection)
    * [Filtering Formats](#filtering-formats)
    * [Sorting Formats](#sorting-formats)
    * [Format Selection examples](#format-selection-examples)
* [MODIFYING METADATA](#modifying-metadata)
    * [Modifying metadata examples](#modifying-metadata-examples)
* [EXTRACTOR ARGUMENTS](#extractor-arguments)
* [PLUGINS](#plugins)
    * [Installing Plugins](#installing-plugins)
    * [Developing Plugins](#developing-plugins)
* [EMBEDDING YT-DLP](#embedding-yt-dlp)
    * [Embedding examples](#embedding-examples)
* [CHANGES FROM YOUTUBE-DL](#changes-from-youtube-dl)
    * [New features](#new-features)
    * [Differences in default behavior](#differences-in-default-behavior)
    * [Deprecated options](#deprecated-options)
* [CONTRIBUTING](CONTRIBUTING.md#contributing-to-yt-dlp)
    * [Opening an Issue](CONTRIBUTING.md#opening-an-issue)
    * [Developer Instructions](CONTRIBUTING.md#developer-instructions)
* [WIKI](https://github.com/yt-dlp/yt-dlp/wiki)
    * [FAQ](https://github.com/yt-dlp/yt-dlp/wiki/FAQ)
<!-- MANPAGE: END EXCLUDED SECTION -->

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

<a id="update-channels"></a>

There are currently three release channels for binaries: `stable`, `nightly` and `master`.

* `stable` is the default channel, which offers releases published on a (mostly) monthly schedule. While it is named `stable` due to many of its changes having been tested by users of the `nightly` or `master` release channels, the latest `stable` release is often "stale" and prone to external breakage (i.e. sites changing things on their end and breaking yt-dlp).
* The `nightly` channel offers releases that publish shortly before midnight UTC on any day that sees changes to the codebase. This channel serves as a snapshot of the project's development, and it is the **recommended channel for regular users** of yt-dlp. The `nightly` releases are available from [yt-dlp/yt-dlp-nightly-builds](https://github.com/yt-dlp/yt-dlp-nightly-builds/releases) or as development releases of the `yt-dlp` PyPI package (which can be installed with pip's `--pre` flag).
* The `master` channel offers "canary" releases that publish after each push to the master branch. This channel will always provide the very latest fixes and features, but may be prone to bugs or regressions. The `master` releases are available from [yt-dlp/yt-dlp-master-builds](https://github.com/yt-dlp/yt-dlp-master-builds/releases).

When using `--update`/`-U`, a release binary will only update to its current channel.
`--update-to CHANNEL` can be used to switch to a different channel when a newer version is available. `--update-to [CHANNEL@]TAG` can also be used to upgrade or downgrade to specific tags from a channel.

You may also use `--update-to <project>` (`<owner>/<project>`) to update to a channel on a completely different project. Be careful with what project you are updating to though, there is no verification done for binaries from different projects.

Example usage:

* `yt-dlp --update-to master` switch to the `master` channel and update to its latest release
* `yt-dlp --update-to stable@2023.07.06` upgrade/downgrade to release to `stable` channel tag `2023.07.06`
* `yt-dlp --update-to 2023.10.07` upgrade/downgrade to tag `2023.10.07` if it exists on the current channel
* `yt-dlp --update-to example/yt-dlp@2023.09.24` upgrade/downgrade to the release from the `example/yt-dlp` project, tag `2023.09.24`

**Important**: Any user experiencing an issue with the `stable` release should install or update to the `nightly` release before submitting a bug report:
```
# To update to nightly from stable executable/binary:
yt-dlp --update-to nightly

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python |
| Manifests detected | pyproject.toml |
| Files in snapshot | 1149 |
| Lines of code | 229578 |
| Dependency references | 0 |
| Upstream license | Unlicense |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
* [INSTALLATION](#installation)
    * [Detailed instructions](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
    * [Release Files](#release-files)
    * [Update](#update)
    * [Dependencies](#dependencies)
    * [Compile](#compile)
* [USAGE AND OPTIONS](#usage-and-options)
    * [General Options](#general-options)
    * [Network Options](#network-options)
    * [Geo-restriction](#geo-restriction)
    * [Video Selection](#video-selection)
    * [Download Options](#download-options)
    * [Filesystem Options](#filesystem-options)
    * [Thumbnail Options](#thumbnail-options)
    * [Internet Shortcut Options](#internet-shortcut-options)
    * [Verbosity and Simulation Options](#verbosity-and-simulation-options)
    * [Workarounds](#workarounds)
    * [Video Format Options](#video-format-options)
    * [Subtitle Options](#subtitle-options)
    * [Authentication Options](#authentication-options)
    * [Post-processing Options](#post-processing-options)
    * [SponsorBlock Options](#sponsorblock-options)
    * [Extractor Options](#extractor-options)
    * [Preset Aliases](#preset-aliases)
* [CONFIGURATION](#configuration)
    * [Configuration file encoding](#configuration-file-encoding)
    * [Authentication with netrc](#authentication-with-netrc)
    * [Notes about environment variables](#notes-about-environment-variables)
* [OUTPUT TEMPLATE](#output-template)
    * [Output template examples](#output-template-examples)
* [FORMAT SELECTION](#format-selection)
    * [Filtering Formats](#filtering-formats)
    * [Sorting Formats](#sorting-formats)
    * [Format Selection examples](#format-selection-examples)
* [MODIFYING METADATA](#modifying-metadata)
    * [Modifying metadata examples](#modifying-metadata-examples)
* [EXTRACTOR ARGUMENTS](#extractor-arguments)
* [PLUGINS](#plugins)
    * [Installing Plugins](#installing-plugins)
    * [Developing Plugins](#developing-plugins)
* [EMBEDDING YT-DLP](#embedding-yt-dlp)
    * [Embedding examples](#embedding-examples)
* [CHANGES FROM YOUTUBE-DL](#changes-from-youtube-dl)
    * [New features](#new-features)
    * [Differences in default behavior](#differences-in-default-behavior)
    * [Deprecated options](#deprecated-options)
* [CONTRIBUTING](CONTRIBUTING.md#contributing-to-yt-dlp)
    * [Opening an Issue](CONTRIBUTING.md#opening-an-issue)
    * [Developer Instructions](CONTRIBUTING.md#developer-instructions)
* [WIKI](https://github.com/yt-dlp/yt-dlp/wiki)
    * [FAQ](https://github.com/yt-dlp/yt-dlp/wiki/FAQ)
<!-- MANPAGE: END EXCLUDED SECTION -->

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# CONTRIBUTING TO YT-DLP

- [NO AI / NO LLM POLICY](#no-ai--no-llm-policy)
- [OPENING AN ISSUE](#opening-an-issue)
    - [Is the description of the issue itself sufficient?](#is-the-description-of-the-issue-itself-sufficient)
    - [Are you using the latest version?](#are-you-using-the-latest-version)
    - [Is the issue already documented?](#is-the-issue-already-documented)
    - [Why are existing options not enough?](#why-are-existing-options-not-enough)
    - [Have you read and understood the changes, between youtube-dl and yt-dlp](#have-you-read-and-understood-the-changes-between-youtube-dl-and-yt-dlp)
    - [Is there enough context in your bug report?](#is-there-enough-context-in-your-bug-report)
    - [Does the issue involve one problem, and one problem only?](#does-the-issue-involve-one-problem-and-one-problem-only)
    - [Is anyone going to need the feature?](#is-anyone-going-to-need-the-feature)
    - [Is your question about yt-dlp?](#is-your-question-about-yt-dlp)
    - [Are you willing to share account details if needed?](#are-you-willing-to-share-account-details-if-needed)
    - [Is the website primarily used for piracy](#is-the-website-primarily-used-for-piracy)
- [DEVELOPER INSTRUCTIONS](#developer-instructions)
    - [Adding new feature or making overarching changes](#adding-new-feature-or-making-overarching-changes)
    - [Adding support for a new site](#adding-support-for-a-new-site)
    - [yt-dlp coding conventions](#yt-dlp-coding-conventions)
        - [Mandatory and optional metafields](#mandatory-and-optional-metafields)
        - [Provide fallbacks](#provide-fallbacks)
        - [Regular expressions](#regular-expressions)
        - [Long lines policy](#long-lines-policy)
        - [Quotes](#quotes)
        - [Inline values](#inline-values)
        - [Collapse fallbacks](#collapse-fallbacks)
        - [Trailing parentheses](#trailing-parentheses)
        - [Use convenience conversion and parsing functions](#use-convenience-conversion-and-parsing-functions)
    - [My pull request is labeled pending-fixes](#my-pull-request-is-labeled-pending-fixes)
- [EMBEDDING YT-DLP](README.md#embedding-yt-dlp)

# NO AI / NO LLM POLICY

This project strictly forbids the usage of LLMs, agents, or any other AI tools for any kind of contribution.

This means:

- No AI / no LLMs for issues or bug reports.

- No AI / no LLMs for patches or pull requests (including PR descriptions).

- No AI / no LLMs for issue tracker comments or code review comments.

- N

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Unlicense** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Unlicense terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Unlicense` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `YT_DLP` (category: SOCIAL MEDIA)
- **Upstream URL:** https://github.com/yt-dlp/yt-dlp
- **Pinned commit (SHA):** `51bab8a0116f4d8004c315706d809782607d5847`
- **Branch:** master
- **Pin provenance:** resolved during the second documentation pass. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`fa40326f772d45c4302ce21f42e30de276b10d1d16bd6984324d49ee07179c81`.

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

