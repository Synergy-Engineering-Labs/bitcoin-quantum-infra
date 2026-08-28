# Threat Model

## Primary threat

BPQI addresses the transaction-authorization consequences of a cryptographically relevant quantum computer capable of attacking the discrete-logarithm assumption underlying secp256k1 ECDSA and Schnorr signatures.

## Long-exposure class

Relevant examples include outputs or metadata where classical public keys are exposed for long periods, including P2PK, Taproot output keys, reused key material, exposed multisig keys, and published extended public-key material.

## Short-exposure class

Classical public keys that remain hidden until spend can become visible in the mempool before confirmation. A sufficiently capable attacker could attempt private-key recovery and a conflicting spend during that interval.

## BPQI protection boundary

BPQI protects newly created quantum-resistant outputs and funds migrated into them. The project provides the cryptographic destination and migration tooling. Treatment of lost, inaccessible, abandoned, or deliberately unmigrated historical outputs remains a Bitcoin governance and ownership-policy question rather than a missing Aegis primitive.

## Implementation threats

The engineering threat model also covers:

- consensus divergence;
- malformed-input parser behavior;
- CPU/memory denial of service;
- signing side channels;
- provider-version drift;
- unsafe key handling;
- entropy failures;
- serialization ambiguity;
- downgrade/hybrid-policy errors;
- supply-chain compromise; and
- wallet/custody recovery failures.
