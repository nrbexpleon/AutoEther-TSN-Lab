# Threat model

| Threat | Current control | Production work |
|---|---|---|
| Malformed/oversized topology | strict validation and hard limits | JSON Schema and fuzzing |
| Spoofed captures/topology | explicit identity fields | signed topology/capture provenance |
| Evidence tampering | SHA-256 and optional RSA signature | HSM/KMS and immutable evidence store |
| Unauthorized API | loopback and optional bearer token | OIDC, roles, audit and tenant isolation |
| Resource exhaustion | body/topology/duration/run bounds | rate limits and worker isolation |
| Unsafe switch changes | no device configuration API | reviewed read/write gateway and change control |
| Sensitive capture leakage | no captures committed | encryption, redaction and retention governance |

Never commit production PCAPs, MAC addresses tied to customers, credentials, keys or proprietary network designs.
