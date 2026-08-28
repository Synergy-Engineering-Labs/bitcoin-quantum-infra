# Bitcoin Core Integration

This directory will contain the open-source Bitcoin Core reference integration for BPQI.

Planned work includes:

- post-quantum verification rule;
- script/witness semantics;
- consensus and policy validation;
- resource accounting;
- verification caching;
- RPC support;
- regtest/signet configuration;
- wallet hooks;
- consensus test fixtures.

The integration must keep Bitcoin consensus semantics independent from Aegis runtime configuration.
