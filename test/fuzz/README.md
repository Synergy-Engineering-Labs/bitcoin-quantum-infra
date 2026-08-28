# Fuzzing

Planned fuzz targets include:

- PQ key/signature parsing;
- algorithm identifiers;
- witness/script decoding;
- public-key commitments;
- invalid verification paths;
- resource accounting;
- descriptors;
- PSBT parsing;
- migration metadata;
- provider-interface error mapping.

Fuzzing should emphasize rejection paths and worst-case resource behavior, not only valid cryptographic inputs.
