# Commercial HTTP surface (does not fork the verifier)

Public verifier remains the only verdict function.

```
POST /verify          → identical to quantumguard cmd/qg-http
GET  /health          → {"ok":true,"contract":"v1","alg":"ed25519"}
GET  /license         → {"sku":"OEG-SEAL|OEG-LINE","exp":"YYYY-MM-DD"}  (commercial only)
```

Rules:
- `/verify` must call the same package as CLI.
- License middleware wraps the *server*, never the verdict function.
- No wall-clock in the verdict path. License expiry is an HTTP concern only.
