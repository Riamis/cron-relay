# cron-relay

Scheduled HTTP triggers. This repository contains workflow definitions only —
no application code, no data, and no credentials.

Every target URL and token is stored as a repository secret. Workflow logs
intentionally print HTTP status codes only, never response bodies.

| Workflow | Schedule | Purpose |
| --- | --- | --- |
| `track-hourly` | hourly | full scan trigger |
| `track-hot` | every 5 min | short-interval trigger |
| `keepalive` | monthly | keeps scheduled workflows enabled |
