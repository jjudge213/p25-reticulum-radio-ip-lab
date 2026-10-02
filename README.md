# P25 Reticulum Radio IP Lab

Private portfolio case study. Do not publish until evidence review, redaction, and claim review are complete.

## Purpose

This repository documents an investigation into the APCO P25 Common Air Interface (CAI), how P25 data/IP behavior is implemented across radio brands, and what it takes to connect radio equipment to laptop/Linux networking workflows.

The current focus is Motorola Astro-series P25 behavior. Harris XG-100M testing is included as a comparison point, and EFJohnson 5100/5300 testing is planned future work.

The project was motivated by the rise of MANET-style tactical radio equipment and the expanding use of the TAK ecosystem in DoD/DoW fielding. The underlying question was:

> What radio systems are available to civilians that support encrypted digital modulation and IP networking well enough to act as a transport layer for TAK-style field operations?

The portfolio goal is to show practical tactical-radio research: reading standards, comparing vendor behavior, testing radio-to-terminal workflows, and documenting where constrained IP networking is realistic versus where the radio system architecture imposes hard limits.

## Current Findings

| Area | Finding | Portfolio Value |
|---|---|---|
| P25 CAI research | Project centers on P25 CAI behavior and vendor implementation differences | Shows standards-driven research and protocol literacy |
| Motorola Astro testing | IP networking between radios appears possible with manual routing configuration on connected terminals | Shows hands-on radio-to-computer networking investigation |
| Harris XG-100M testing | IP networking path appears to require trunked-system implementation | Shows vendor comparison and honest negative/constraint finding |
| EFJohnson 5100/5300 | Planned future comparison target | Shows a structured multi-vendor test plan |
| Reticulum over IP-over-P25 | Used as a basic proof-of-concept over an established IP-over-P25 link | Shows transport-layer-agnostic messaging over constrained radio-linked IP |

## Problem

MANET products show what modern field networking can look like when radios, encryption, routing, and tactical software are designed as one system. Civilian-accessible equipment is more fragmented. P25 radios are available on the secondary market and support encrypted digital voice in lawful configurations, but that does not automatically mean they are practical IP transports.

In practice, the useful question is narrower:

- What does the P25 CAI standard actually support?
- Which capabilities are implemented differently by vendor and product line?
- When can two radios support data/IP behavior directly?
- When does IP networking depend on trunked infrastructure or system-side services?
- What terminal-side routing, addressing, and interface configuration are required?
- Can any civilian-accessible radio path become a realistic transport layer for TAK-style field workflows?

This repo captures that investigation without presenting it as a finished operational network.

## Approach

1. Start with the P25 CAI standard and public technical references.
2. Compare brand behavior rather than assuming all P25 radios expose the same data features.
3. Test Motorola Astro-series workflows first because current evidence supports radio-to-laptop terminal work.
4. Use Harris XG-100M testing as a comparison point for trunked-system dependency.
5. Use Reticulum as a transport-layer-agnostic, decentralized messaging proof of concept over an established IP-over-P25 link.
6. Preserve screenshots and short evidence clips for private review, then redact before any public release.

## Evidence Structure

### Motorola Astro / Radio-To-Terminal Workflow

The strongest current evidence supports Motorola Astro-series P25 experimentation with connected terminals. Current testing indicates that IP networking between radios is possible when connected computers are configured with manual routing.

This supports a resume claim around practical protocol research, Linux/networking configuration, and tactical-radio experimentation.

Representative evidence:

- Source: https://www.instagram.com/p/CjJsYT0jVB5IxzQSpVl7jvjsNyL5eP1poPWTp40/

<img src="assets/p25-radio-laptop-terminal-evidence-missed-by-caption-2022-10-01-01.gif" alt="Motorola Astro P25 radio-to-laptop terminal workflow evidence, 2022-10-01" width="48%">

- Source: https://www.instagram.com/p/CjHmIVEj8k8pzLazGRw1xb9GYOW-VUecDM5uwI0/

<img src="assets/p25-radio-laptop-terminal-evidence-missed-by-caption-2022-09-30-01.gif" alt="Motorola Astro P25 radio-to-laptop terminal workflow evidence, 2022-09-30" width="48%">

### Reticulum Proof Of Concept

Reticulum was used because it is transport-layer agnostic and decentralized: it can operate above whatever link can move packets, rather than requiring a normal LAN-like environment. In this project, Reticulum was tested as a basic messaging proof of concept over an already established IP-over-P25 link.

That distinction matters. The claim is not that Reticulum directly implements P25 CAI or that a production Reticulum-over-P25 network is complete. The claim is that once an IP path over P25 existed, Reticulum provided a useful application-layer test of decentralized messaging behavior over that constrained transport.

### Harris XG-100M Comparison

Harris XG-100M testing produced an important constraint: the IP networking path appears to require trunked-system implementation rather than a simple direct radio-to-radio terminal network.

This is useful evidence because it shows disciplined testing and willingness to document negative results instead of forcing a generic "P25 IP works" claim.

### Future EFJohnson Comparison

Future work should include EFJohnson 5100/5300 testing to compare another major P25 vendor family against the Motorola and Harris findings.

## What This Demonstrates

- P25 CAI standards research.
- Multi-vendor radio behavior comparison.
- Motorola Astro-series P25 familiarity.
- Harris XG-100M constraint testing.
- Reticulum proof-of-concept testing over an established IP-over-P25 link.
- Linux terminal networking and manual routing awareness.
- Constrained-networking judgment: bandwidth, routing, infrastructure dependency, and operational limits.
- Evidence discipline for sensitive communications topics.

## What This Is Not

This repository does not claim:

- a production P25 IP deployment
- trunked-system administration access
- published operational frequencies, talkgroups, radio IDs, codeplugs, or encryption material
- a complete Reticulum-over-P25 field network
- Reticulum as a native P25 CAI implementation
- a completed TAK-over-P25 transport layer
- universal P25 vendor behavior

The claim is narrower: this is a documented research and test effort around P25 CAI implementation differences and constrained radio-linked IP workflows.

## Current Evidence

- Active media assets: 7
- JPG stills: 3
- Animated GIFs: 4
- Source posture: private review assets only; publication requires redaction and fit review.

See [docs/evidence-gallery.md](docs/evidence-gallery.md) for the private review gallery and [evidence-manifest.md](evidence-manifest.md) for the current asset list.

## Sensitive Material Boundary

This repository must not publish:

- encryption keys, key-fill files, or key IDs
- proprietary radio programming files, codeplugs, or restricted manuals
- operational frequencies, talkgroups, radio IDs, serials, or unit IDs
- private routing details tied to real systems
- screenshots exposing sensitive radio configuration
- trunked-system details that imply access to non-public infrastructure
- credentials, certificates, tokens, or private network identifiers

Public diagrams should use placeholders and recreated examples only.

## Next Work

- Write a short P25 CAI research note summarizing standard-level findings in public-safe terms.
- Add a sanitized Motorola Astro test topology diagram showing radios, terminals, and manual routing at a high level.
- Add a sanitized Harris XG-100M comparison note explaining the trunked-system dependency finding.
- Build an EFJohnson 5100/5300 test plan before adding that vendor to the comparison.
- Add a "terminal routing checklist" using placeholder addresses only.
- Review every GIF/still for visible radio IDs, frequencies, serials, terminal hostnames, paths, and private network details.

## Review Docs

- [Evidence gallery](docs/evidence-gallery.md)
- [Evidence manifest](evidence-manifest.md)
- [Sanitization notes](docs/sanitization-notes.md)
