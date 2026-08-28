# Roadmap

## Phase 1 — Specification freeze (Months 1–2)

Deliverables:

- Aegis-BTC v1 profile;
- ML-DSA-44 initial profile;
- deterministic verifier contract;
- canonical key/signature encoding;
- Bitcoin sighash/domain-separation rules;
- resource model;
- machine-readable vector format;
- public repository and contribution process.

Exit condition: every consensus-relevant cryptographic behavior is machine-testable.

## Phase 2 — Regtest implementation (Months 2–4)

Deliverables:

- Bitcoin Core integration;
- post-quantum verifier;
- output/spend path;
- RPC support;
- wallet prototype;
- descriptors;
- PSBT prototype;
- benchmark harness.

Exit condition: complete quantum-resistant transactions execute deterministically on regtest.

## Phase 3 — Independent audit and validation (Months 2–7, parallel)

Deliverables:

- auditor source access;
- cryptographic review;
- implementation and side-channel review;
- conformance testing;
- remediation;
- independent retest;
- validation-package work where applicable.

Exit condition: no unresolved critical/high finding affecting the defined Bitcoin security boundary.

## Phase 4 — Migration and custody tooling (Months 4–7)

Deliverables:

- UTXO exposure classifier;
- migration planner;
- wallet migration flow;
- batch migration;
- hardware-signing interface;
- institutional custody guidance.

Exit condition: wallet-controlled classical regtest holdings can be classified and migrated end-to-end into PQ outputs.

## Phase 5 — Signet and interoperability (Months 6–9)

Deliverables:

- public signet demonstration;
- independent verifier comparison;
- public test vectors;
- fuzz corpus;
- performance results;
- interoperability documentation.

Exit condition: independent implementations produce matching consensus results across the public test suite.

## Phase 6 — BIP-quality release candidate (Months 9–12)

Deliverables:

- BIP-quality technical specification;
- reference implementation;
- audit/remediation evidence;
- conformance/validation evidence;
- final benchmarks;
- deployment and migration guidance.

Exit condition: complete technical package is ready for Bitcoin developer review and potential consensus deployment.

Mainnet activation is not a project-controlled success criterion because activation belongs to Bitcoin's decentralized consensus process.
