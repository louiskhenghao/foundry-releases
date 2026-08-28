# Foundry releases

## 0.2.0 — 2026-08-28

- Version detection: Foundry now knows its own version and checks the release registry daily (Settings → About & updates, header pill)
- One-click self-update: docker installs update through a watchtower sidecar (new docker-compose.yml); local installs run git pull → install → rebuild with automatic rollback
- Updates drain first: active agents finish before the restart, with a force option
- Changelog shown in the update dialog; new-version notifications via Telegram/Discord (per-family switch)
- Installs that cannot self-update get the exact guided commands instead
