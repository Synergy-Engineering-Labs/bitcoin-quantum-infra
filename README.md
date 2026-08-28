# Bitcoin Post-Quantum Infrastructure (BPQI)

**Open-source post-quantum infrastructure for Bitcoin, developed by Synergy Engineering Labs and powered by Aegis PQC.**

**Repository:** `synergy-engineering-labs/bitcoin-quantum-infra`  
**Project:** Bitcoin Post-Quantum Infrastructure (BPQI)

BPQI is a Bitcoin protocol implementation project led by **Synergy Engineering Labs**. Its purpose is to provide Bitcoin with a practical, testable, independently reviewable path to post-quantum transaction authorization using **Aegis**, an independent, patent-pending post-quantum cryptography platform, as the cryptographic dependency.

The project is intentionally Bitcoin-native: Bitcoin consensus defines the accepted algorithms, encodings, signature message, resource limits, and activation semantics; Aegis performs the pinned cryptographic operations behind a narrow deterministic interface.

> **Repository boundary:** This repository contains the open-source Bitcoin-facing work. It does **not** contain the proprietary Aegis implementation source code.

## Why this project exists

Bitcoin transaction authorization currently relies on secp256k1 ECDSA and Schnorr signatures. A sufficiently capable cryptographically relevant quantum computer would threaten the discrete-logarithm assumption underlying those signatures. BPQI adds a quantum-resistant authorization path while preserving Bitcoin's UTXO model, proof-of-work consensus, SHA-256 hashing foundation, fee market, and script/witness architecture.

BPQI is an implementation and assurance program, not an effort to invent a new post-quantum signature scheme. The initial profile is designed around standardized post-quantum signatures and existing Bitcoin upgrade mechanisms.

## Initial technical direction

The first implementation profile targets:

- a dedicated **Aegis-BTC deterministic verification profile**;
- **ML-DSA-44** as the initial standardized interoperability baseline;
- a Bitcoin-native post-quantum signature verification rule;
- an opt-in quantum-resistant output/spend path;
- compatibility with **P2MR/BIP 360** if that path is adopted by Bitcoin;
- wallet, descriptor, PSBT, custody, and hardware-signing integration;
- migration tooling for existing wallet-controlled UTXOs;
- consensus-safe resource accounting and denial-of-service protections;
- independent cryptographic audit and standards-conformance testing; and
- public test vectors, benchmarks, interoperability tooling, and reference code.

## Architecture

BPQI is organized into six layers:

1. **Quantum-resistant Bitcoin output** — an opt-in output/spend path for post-quantum authorization.
2. **Bitcoin PQ signature rule** — a consensus-defined verification operation with Bitcoin-native semantics.
3. **Aegis-BTC verifier** — a narrow deterministic cryptographic dependency interface.
4. **Wallet and custody integration** — signing, descriptors, PSBT, backups, hardware devices, and institutional workflows.
5. **Migration infrastructure** — exposure classification and migration of wallet-controlled classical UTXOs.
6. **Assurance and validation** — audit, fuzzing, differential testing, conformance testing, remediation, and formal validation work where applicable.

See [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) for the detailed model.

## Open-source and Aegis licensing boundary

All Bitcoin-specific work in this repository is intended to be open source.

Aegis is a separate, pre-existing, patent-pending product maintained by Synergy Engineering Labs. Aegis is consumed through a defined dependency interface and is not relicensed by this repository's open-source license.

Synergy Engineering Labs intends to provide a separate **Bitcoin-specific, no-fee/royalty-free authorization** for Aegis so the Bitcoin ecosystem can use the Aegis dependency for defined Bitcoin purposes without creating general-purpose rights for unrelated networks, protocols, or products. The final legal instrument will govern those rights; this README is not the license grant.

See [`docs/AEGIS_DEPENDENCY_AND_LICENSING.md`](docs/AEGIS_DEPENDENCY_AND_LICENSING.md).

## Repository layout

```text
.
├── docs/                    Project architecture, security model, roadmap, and grant scope
├── spec/                    Normative Aegis-BTC and Bitcoin-facing protocol specifications
├── integration/
│   ├── aegis/               Aegis dependency boundary and adapter work
│   ├── bitcoin-core/        Bitcoin Core integration and reference patches
│   └── wallet/              Wallet, descriptor, PSBT, and signing integration
├── test/
│   ├── fuzz/                Fuzzing targets and malformed-input corpora
│   └── vectors/             Public consensus and interoperability vectors
├── contrib/signet/          Reproducible signet demonstration tooling
└── .github/                 Project governance and contribution templates
```

## Milestones

The implementation plan is structured around bounded engineering milestones:

1. **Specification freeze** — Aegis-BTC profile, encodings, sighash/domain separation, resource model, and test-vector format.
2. **Regtest implementation** — Bitcoin Core verifier, output/spend path, RPC, wallet prototype, descriptors, PSBT, and benchmark harness.
3. **Independent audit and validation** — cryptographic review, side-channel review, conformance testing, remediation, and retesting.
4. **Migration and custody tooling** — UTXO exposure classifier, migration flows, batch migration, hardware/custody interfaces.
5. **Signet and interoperability** — public test environment, independent verifier comparison, fuzzing, and long-running compatibility testing.
6. **BIP-quality release candidate** — complete specification, reference implementation, security evidence, benchmarks, and deployment package.

See [`docs/ROADMAP.md`](docs/ROADMAP.md).

## Project status

**Initial public scaffold / specification freeze.**

The public repository is being established as the canonical home for the Bitcoin-specific implementation. Aegis itself is an existing independent cryptographic product and is not being developed from scratch by this repository.

## Security

Consensus cryptography is security-critical. Please read [`SECURITY.md`](SECURITY.md) before reporting a vulnerability. Security-sensitive findings should not be opened as public issues.

## Contributing

Contributions to the open-source Bitcoin-facing implementation, specification, tests, benchmarks, wallet tooling, and documentation are welcome. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## License

Repository code and documentation are licensed under the MIT License unless a file states otherwise. See [`LICENSE`](LICENSE) and [`NOTICE.md`](NOTICE.md).

**Important:** the MIT License for this repository does not license the proprietary Aegis implementation or its patent rights. Bitcoin-specific Aegis authorization is governed by a separate instrument.
