# Aegis Integration Boundary

This directory contains only the distributable BPQI-side adapter/interface work needed to consume Aegis as a dependency.

The proprietary Aegis implementation source is not stored here.

The adapter will implement the exact Aegis-BTC profile defined under `spec/` and expose deterministic verification/signing operations required by the Bitcoin-facing implementation.

Auditors and validation laboratories may receive separate controlled access to Aegis source as required for the independent assurance program.
