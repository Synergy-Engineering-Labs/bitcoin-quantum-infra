# Wallet, Descriptor, and PSBT Profile — Draft 0

## Goals

BPQI wallet tooling must support creation, backup, observation, signing, recovery, fee estimation, and migration of quantum-resistant Bitcoin outputs.

## Wallet requirements

The profile will define:

- PQ key generation/derivation semantics;
- domain separation from secp256k1 material;
- backup metadata;
- watch-only representation;
- output/address representation;
- descriptor extensions;
- fee estimation using actual PQ witness size;
- recovery and hybrid policies.

## PSBT requirements

The profile will define fields for:

- algorithm identifier;
- PQ public-key information;
- key origin/derivation metadata;
- post-quantum signature;
- hybrid policy metadata;
- signer/provider metadata required for interoperability.

Experimental fields should have a documented transition path to standardized assignments through the Bitcoin proposal process.
