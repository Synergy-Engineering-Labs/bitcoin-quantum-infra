# Security Assurance Program

## Objective

BPQI is designed to pair a public Bitcoin implementation with independently reviewed cryptographic infrastructure. The assurance program provides evidence beyond internal self-attestation.

## Independent audit scope

The planned audit includes:

- algorithm implementation correctness;
- key generation, signing, and verification;
- parameter enforcement;
- memory safety and zeroization;
- randomness requirements and failure handling;
- timing and side-channel behavior;
- deterministic verification;
- canonical parsing and serialization;
- malformed-input handling;
- consensus error mapping;
- provider equivalence;
- denial-of-service behavior;
- dependency and supply-chain review;
- release provenance and reproducibility.

## Retesting

Security findings affecting the Bitcoin-relevant boundary are remediated and independently retested. Critical or high-severity findings within the defined security boundary block a release candidate until resolved or explicitly removed from scope.

## Conformance

The project will maintain known-answer tests, negative tests, cross-provider comparison, and standards-conformance evidence for the selected standardized algorithm profile.

## Public evidence

Where contractual and security constraints permit, BPQI will publish audit summaries, remediation status, test vectors, benchmarks, conformance evidence, and the exact Bitcoin-facing interface under review.
