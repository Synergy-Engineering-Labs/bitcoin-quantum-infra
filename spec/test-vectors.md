# Test Vector Requirements — Draft 0

Public machine-readable vectors will cover at least:

- valid post-quantum spends;
- invalid signatures;
- wrong public keys;
- wrong public-key commitments;
- altered transaction fields;
- wrong algorithm identifiers;
- truncated keys/signatures;
- oversized objects;
- malformed witness structures;
- sighash/domain-separation failures;
- hybrid-policy failures;
- resource-limit boundaries;
- provider/version incompatibilities.

A compatible independent implementation should be able to reproduce acceptance behavior using only the public specification and vectors.
