# BPQI Specifications

This directory contains the normative Bitcoin-facing technical specifications for BPQI.

The specification set is intentionally separate from implementation code so independent implementations can reproduce consensus behavior without relying on undocumented Aegis internals.

Planned normative documents:

- `aegis-btc-profile.md` — cryptographic profile and algorithm registry;
- `consensus-interface.md` — deterministic Bitcoin/Aegis verifier boundary;
- `encoding.md` — canonical Bitcoin-native encodings;
- `wallet-psbt.md` — wallet, descriptor, and PSBT semantics;
- `test-vectors.md` — machine-readable interoperability requirements.
