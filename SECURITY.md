# Security Policy

BPQI contains consensus- and cryptography-adjacent software. Security reports must be handled conservatively.

## Reporting vulnerabilities

Do **not** open a public GitHub issue for a vulnerability that could affect:

- signature verification;
- consensus determinism;
- malformed-input handling;
- resource exhaustion or denial of service;
- key handling or signing;
- wallet recovery;
- migration safety;
- provider versioning or supply-chain integrity; or
- the Aegis-BTC dependency boundary.

Use GitHub Private Vulnerability Reporting when enabled for this repository. Until a dedicated public security contact is published, contact the project maintainers privately through the repository owner's established channels.

## Disclosure

The project intends to coordinate responsible disclosure, remediation, regression testing, and public advisories for confirmed issues. Findings involving proprietary Aegis internals may require coordinated handling with Synergy Engineering Labs and the relevant independent auditor.

## Audit scope

The project's assurance program is expected to cover implementation correctness, key handling, randomness requirements, memory safety, side-channel behavior, malformed inputs, deterministic verification, provider equivalence, fuzzing, denial-of-service behavior, release provenance, and standards conformance.
