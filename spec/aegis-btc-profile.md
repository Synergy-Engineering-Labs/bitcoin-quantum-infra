# Aegis-BTC Profile — Draft 0

**Status:** Initial specification scaffold; not a consensus proposal.

## 1. Purpose

The Aegis-BTC profile defines the exact post-quantum cryptographic behavior that a Bitcoin implementation may request from Aegis. It prevents generic runtime algorithm agility from becoming Bitcoin consensus ambiguity.

## 2. Initial algorithm registry

Provisional registry for development and interoperability testing:

| ID | Algorithm | Status |
|---|---|---|
| `0x01` | ML-DSA-44 | Initial development baseline |
| `0x02` | SLH-DSA-128s | Diversified recovery / low-frequency profile |
| `0x03` | Reserved | Future activation only |
| `0x04` | Reserved | Future activation only |

An algorithm identifier is invalid until Bitcoin consensus or the selected test profile explicitly activates it.

## 3. Consensus requirements

The profile MUST freeze:

- exact algorithm revision and parameter set;
- canonical public-key encoding;
- canonical signature encoding;
- accepted byte lengths;
- Bitcoin signature-message construction;
- domain separation;
- verifier return semantics;
- malformed-input behavior;
- memory/allocation bounds;
- resource-cost model;
- conformance vectors.

## 4. Provider behavior

A provider MAY be replaced by an optimized implementation only when it is behaviorally equivalent at the consensus interface. Provider selection MUST NOT alter accepted Bitcoin transactions.

## 5. Verification properties

Consensus verification MUST be deterministic and MUST NOT require entropy, private key material, network access, or runtime algorithm negotiation.
