
## 2026-02-05: SRI Integrity Hashes Must Be Verified

**Mistake:** Used fabricated SRI integrity hashes for Bootstrap 5.3.3 CDN links. The browser downloaded the files (200 OK) but silently refused to apply them because the hash didn't match, breaking all Bootstrap styling.

**Rule:** NEVER include `integrity` attributes with unverified hashes. Either:
1. Omit integrity/crossorigin attributes entirely (safe for CDN usage), or
2. Generate hashes from the actual files using `openssl dgst -sha384 -binary | openssl base64 -A`, or
3. Copy exact CDN tags from the official project documentation

**Detection:** Test that a BS5-only class (like `visually-hidden`) applies correct styles. If it doesn't, the CSS isn't being loaded.
