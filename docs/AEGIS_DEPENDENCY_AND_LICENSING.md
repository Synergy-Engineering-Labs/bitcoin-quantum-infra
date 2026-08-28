# Aegis Dependency and Licensing Boundary

## Product boundary

Aegis is an independent, pre-existing, patent-pending post-quantum cryptography product maintained by Synergy Engineering Labs. Its core source repositories are private and are not part of BPQI's public repository.

BPQI consumes Aegis through a narrowly defined Bitcoin-specific dependency interface.

## Open-source boundary

The BPQI Bitcoin-facing implementation is intended to be fully open source, including:

- Bitcoin Core integration;
- Aegis-BTC adapter/interface code that is distributable independently of Aegis internals;
- specifications;
- test harnesses and vectors;
- benchmarks;
- wallet integration;
- PSBT and descriptor work;
- migration tooling;
- signet/regtest tooling; and
- documentation.

## Bitcoin-specific Aegis authorization

Synergy Engineering Labs intends to issue a separate Bitcoin-specific authorization permitting Aegis to be used for defined Bitcoin purposes without licensing fees or royalties.

The intended scope may include Bitcoin node operation, transaction verification, transaction signing, wallets, custody, hardware signing, mining infrastructure, protocol research, mainnet, testnet, signet, regtest, interoperability testing, and directly supporting Bitcoin infrastructure as defined by the final instrument.

The authorization is intended to be limited to Bitcoin-related use and not to create general-purpose rights for unrelated blockchains, protocols, applications, or products.

## Important legal note

This document describes the intended technical and licensing architecture. **It is not itself the Aegis license grant.** The final legal instrument issued by the Aegis rights holder controls the actual authorization, scope, duration, patent rights, redistribution conditions, termination rules, and other legal terms.

This separation prevents the repository's MIT license from accidentally granting rights in proprietary Aegis technology beyond the intended Bitcoin scope.
