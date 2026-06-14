# Open Business Bundle Architecture Foundation

This organization develops and maintains the **Open Business Bundle (OBB)** specification ecosystem: an open, style-agnostic, and cryptographically secure document standard used to preserve, render, and migrate business records across decoupled computing environments without external platform dependencies.

The core objective is to establish a data interchange standard independent of specialized hardware environments, operating system file variations, or proprietary enterprise applications.

---

## Repository Structure

The ecosystem is decoupled into distinct repositories to separate the normative standard from concrete software implementations:

* **[`spec`](https://github.com/obbiz/spec)** — Contains the definitive technical specification text, architectural diagrams, and production-grade JSON Schema definitions.
* **[`core`](https://github.com/obbiz/core)** — The official TypeScript reference implementation, containing the compilers, soft-drain asset ledgers, and normalizers.
* **[`conformance`](https://github.com/obbiz/conformance)** — Automated validation tooling and compliance test fixtures used to certify third-party runtime implementations.

---

## Technical Foundations

Every implementation under the `obbiz` banner must execute according to the following systems design constraints:

* **Semantic Decoupling:** Business data remains style-agnostic. Visual templates, layout flows, and print dimensions are isolated purely within separate view configuration files.
* **Cross-Platform Hash Determinism:** Employs mandatory Unicode normalization on text assets and archive paths to eliminate raw byte discrepancies caused by platform-specific file systems, guaranteeing identical cryptographic hashes globally.
* **Decoupled Integrity Verification:** The raw ZIP container wrapper is ignored during security checks. Systems calculate individual file content hashes paired with a manifest self-hash to maintain clear validation boundaries.
* **Soft-Drain Memory Management:** Designed for concurrent asynchronous frontend lifecycles, utilizing a state-tracked reference counting ledger that gracefully revokes memory allocations and Blob URLs after active components completely unmount.

---

## Governance & Licensing

* **Specification Licensing:** The technical specification documentation and directory schemas are licensed under the **Creative Commons Attribution 4.0 International License (CC-BY-4.0)**.
* **Software Licensing:** The official TypeScript reference implementation codebases are distributed under the permissive **MIT License**.

Technical errata, formal inquiries, or Format Change Requests must be submitted as tracked issues directly within the `spec` repository.

---

*Copyright © 2026 obbiz Project Authors. Distributed under open-source standards.*
