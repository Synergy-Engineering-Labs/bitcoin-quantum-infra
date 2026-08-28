# Contributing to BPQI

BPQI welcomes contributions to the open-source Bitcoin-facing implementation and technical specifications.

## In scope

Contributions are especially useful in:

- Bitcoin Core integration;
- consensus and script/witness specification;
- deterministic parsing;
- descriptors and PSBT;
- wallet and hardware-signing support;
- migration tooling;
- public test vectors;
- fuzzing;
- benchmarking;
- differential verification;
- documentation; and
- security analysis.

## Out of scope for this repository

The proprietary Aegis implementation source is not maintained here. Do not submit pull requests that attempt to copy, reconstruct, or redistribute private Aegis source code.

## Development principles

1. Consensus behavior must be deterministic.
2. Bitcoin consensus, not runtime configuration, decides accepted algorithms and semantics.
3. Verification must fail closed.
4. Parsing and allocation must be bounded.
5. Optimizations must not change acceptance behavior.
6. Test vectors must cover invalid and boundary inputs, not only successful signatures.
7. Public claims must match demonstrated implementation evidence.

## Pull requests

Pull requests should include:

- a clear rationale;
- tests for behavior changes;
- performance impact where relevant;
- consensus compatibility considerations; and
- documentation updates for externally visible behavior.

Security-sensitive changes should first follow the process in `SECURITY.md`.
