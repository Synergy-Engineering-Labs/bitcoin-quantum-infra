# BPQI Architecture

## Design objective

BPQI adds a Bitcoin-native post-quantum authorization path without replacing Bitcoin's UTXO model, proof-of-work consensus, SHA-256 foundation, fee market, or peer-to-peer consensus architecture.

The system deliberately separates **Bitcoin consensus semantics** from **Aegis cryptographic implementation**.

## Six-layer model

### 1. Quantum-resistant Bitcoin output

An opt-in output/spend path commits to a post-quantum authorization condition. The implementation is intended to remain compatible with P2MR/BIP 360 if Bitcoin adopts that structure while preserving the ability to target another accepted witness/script upgrade path.

### 2. Bitcoin post-quantum signature rule

Bitcoin defines the consensus-visible verification rule, including algorithm identifier, key/signature encoding, sighash semantics, resource accounting, and failure behavior.

### 3. Aegis-BTC deterministic verifier

Bitcoin calls a narrow verification-only API. No runtime configuration may alter consensus. The verifier has no entropy input, no secret input, bounded memory, bounded parsing, and deterministic failure mapping.

### 4. Wallet and custody integration

The project defines post-quantum key generation/backup semantics, descriptors, PSBT data, watch-only representations, fee estimation, hardware signing, HSM integration, and institutional workflows.

### 5. Migration infrastructure

Open-source tooling classifies wallet-controlled UTXOs by quantum exposure and constructs migrations into quantum-resistant outputs.

### 6. Assurance and validation

The Aegis capabilities used by Bitcoin are subjected to independent source review, conformance testing, malformed-input testing, fuzzing, differential validation, side-channel review, remediation, and independent retesting.

## Consensus boundary

Bitcoin decides:

- which algorithms are active;
- which exact revisions and parameter sets are valid;
- canonical encodings;
- signature-message construction;
- script/witness semantics;
- resource costs;
- activation and deactivation rules.

Aegis supplies:

- the pinned cryptographic operation;
- deterministic verification;
- provider implementation behind the fixed interface;
- versioned evidence and lifecycle metadata.

A local Aegis configuration change must never change what a Bitcoin node accepts.

## Initial profile

The initial research/interoperability profile targets ML-DSA-44, with SLH-DSA available as a diversified low-frequency/recovery option and FN-DSA reserved for future consideration after final standardization and independent evidence.
