# Consensus Interface — Draft 0

## Conceptual API

```text
aegis_btc_verify(
    algorithm_id,
    public_key,
    signature,
    bitcoin_signature_message
) -> VALID | INVALID
```

This is a semantic interface, not yet a final ABI.

## Required properties

The verification boundary MUST provide:

- no entropy input;
- no secret/private input;
- no network access;
- no dynamic algorithm negotiation;
- bounded memory;
- bounded parsing;
- deterministic execution;
- exact input-length validation;
- fixed error-to-invalid mapping;
- fail-closed behavior.

## Consensus ownership

Bitcoin defines algorithm acceptance, signature-message semantics, resource pricing, and canonical encodings. Aegis supplies only the pinned cryptographic operation requested by the Bitcoin-defined profile.

## Version pinning

Bitcoin implementations MUST pin an exact Aegis-BTC interface/profile revision. An ordinary Aegis software update MUST NOT silently alter Bitcoin consensus behavior.
