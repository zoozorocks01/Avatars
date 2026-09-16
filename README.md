# Avatars — Codex / Desktop Pets

Small animated companions for desktop apps that support local custom pets.

| Pet | Version | Status |
| --- | --- | --- |
| [Maple](maple/README.md) | 2.1.0 | Downloadable prototype |
| [Cosmo Royal](cosmo/README.md) | — | Coming later; no release yet |

## Get Maple

[Download Maple V2.1](https://github.com/zoozorocks01/Avatars/raw/refs/heads/main/maple/v2.1/Maple-v2.1.0-Prototype.zip) · [Preview](maple/v2.1/preview.gif)

![Maple trotting](maple/v2.1/preview.gif)

- **Installing yourself?** Follow [Install and update](INSTALL.md).
- **Asking an agent?** Give it this repository link and [Agent installation instructions](AGENT-INSTALL.md).
- **Checking updates?** [catalog.json](catalog.json) points to each pet's current version and checksum manifest.

You can tell your agent:

> Install Maple from https://github.com/zoozorocks01/Avatars using AGENT-INSTALL.md. Verify the files and preserve a backup of any existing Maple before replacing it. Ask me to select/show the pet if you cannot control the app.

These are pet assets, not standalone applications. The pet itself is a JSON description and a WebP sprite sheet: no executable installer, API key, password, or subscription is included or required by this repository. A compatible host app is required. This is not an official OpenAI repository.

## Versions and updates

Each published version gets its own folder. Published version files are not silently replaced: later changes get a new version and updated catalog entry. The installation folder and pet ID stay stable across updates. Checking this repository does **not** automatically install updates or change application settings.

Mac local-folder installation is the documented path. Windows/Linux and other app versions have not been verified; use the host app's own custom-pet folder control, and stop if it lacks that feature.

## About this collection

Maintainer: [zoozorocks01](https://github.com/zoozorocks01). Personal project, created 2026-09-16. Repository contents are Markdown, JSON, PNG/WebP/GIF assets and ZIP packages. No blanket software or artwork license is specified; third-party character rights are not implied by hosting a file here.
