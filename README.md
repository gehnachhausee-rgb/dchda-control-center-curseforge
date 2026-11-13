# DCHDA Control Center - CurseForge Integration

This repository documents the CurseForge integration used by the private,
non-commercial DCHDA Control Center.

## Purpose

The integration helps administrators maintain self-hosted Minecraft servers by:

- identifying locally installed mods through CurseForge fingerprints
- retrieving project and file metadata
- checking Minecraft and mod-loader compatibility
- displaying available updates
- linking administrators to the original CurseForge project pages

## Distribution

This project does not host, mirror, repackage, or independently distribute
CurseForge mod files.

Downloads are not currently performed by the integration. Any future download
support will respect the mod author's distribution settings and use only
official CurseForge download URLs.

## API usage

The integration uses the official CurseForge API:

- `POST /v1/fingerprints`
- `GET /v1/mods/{modId}`
- `GET /v1/mods/{modId}/files`
- `GET /v1/mods/{modId}/files/{fileId}`

Authentication uses the `x-api-key` header. API keys are stored outside the
application source in a protected server-side credential file.

## Privacy and security

- The dashboard is restricted to authorized administrators.
- API keys are never returned to the browser.
- No player information is transmitted to CurseForge.
- No credentials, server addresses or private configuration are included here.

## Commercial use

The project is private and non-commercial. It contains no advertisements,
subscriptions, donations or paid access.
