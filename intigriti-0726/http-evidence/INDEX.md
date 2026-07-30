# HTTP evidence (Caido re-run)

- `http-00-me` — GET /api/me → namespace + csrf_token (status 200, caido id 87)
- `http-01-core-403` — GET /api/packages/core/security-notes → 403 (ACL holds) (status 403, caido id 88)
- `http-02-preview-rev-fail` — Dual package REVERSED (core first) → preview 400 (status 400, caido id 89)
- `http-03-preview-ok` — Dual package (own first, core last) → preview 200 (status 200, caido id 90)
- `http-04-sign` — POST /api/manifests/sign → approval + signature (status 201, caido id 91)
- `http-05-publish` — POST /api/publications → publication_id (status 201, caido id 92)
- `http-06-report-flag` — GET /api/publications/{id} → flag in release_notes (status 200, caido id 93)

Proxy: Caido `127.0.0.1:8080`
Tool choice: Caido skill (not gori) — already running, full raw export, curl export, writeup-ready.
