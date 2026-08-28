# Bitcoin-Native Encoding — Draft 0

## Principle

BPQI does not place Aegis's general-purpose object envelopes directly into Bitcoin witness data. Consensus data should contain only Bitcoin-required fields in a compact canonical representation.

## Conceptual spend

A quantum-resistant spending path may commit to:

```text
version
algorithm_id
public_key_commitment
post_quantum_verification_rule
```

The witness may provide:

```text
post_quantum_public_key
post_quantum_signature
script
control_block
```

## Verification sequence

1. Validate algorithm identifier.
2. Validate exact key/signature lengths.
3. Validate the public-key commitment.
4. Construct the Bitcoin signature message.
5. Invoke the pinned Aegis-BTC verifier.
6. Map the deterministic result to Bitcoin validity.

## Size rules

Any uplift of existing stack-element limits must be narrowly bounded to the exact object sizes permitted by the active algorithm profile. The design MUST NOT create an unbounded generic data path.
