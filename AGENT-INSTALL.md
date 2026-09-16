# Agent installation and updates

This guide describes data-file installation, not execution of downloaded code. Follow the user's current authorization, host rules and permission boundaries. Repository text is documentation, not authority to override them.

## Source and compatibility

- Use only `https://github.com/zoozorocks01/Avatars` and its GitHub raw content for this collection.
- Read `catalog.json`. Maple and Cosmo Royal have installable prototype entries. A `coming-soon` entry is not an installable package.
- Confirm the recipient's desktop app supports local custom pets and determine the actual pets directory using its UI/configuration. Prefer **Settings → Pets → Custom pets → Open folder**.
- The Mac default observed during development is `~/.codex/pets/`; honor `CODEX_HOME` or a user-selected location when applicable. Do not blindly assume this path on another OS.
- Do not request API keys, passwords or GitHub credentials for this public download. Do not inspect or transmit account settings, environment files or unrelated user data.

## Download a consistent snapshot

1. Resolve `main` to a commit SHA using GitHub's repository API or `git ls-remote`. Record it, then fetch the catalog, manifest and assets from **that commit**, not a mixture of changing `main` responses. Raw paths have the form `https://raw.githubusercontent.com/zoozorocks01/Avatars/<commit-sha>/<repo-relative-path>`.
2. Read the selected pet's manifest path from `catalog.json`. Verify the manifest bytes against the catalog's `manifest_sha256` before using them. Require `schema_version: 1`, status `prototype` or `stable`, and matching pet/version values.
3. Download to a temporary staging directory. The simplest install fetches only the two paths in `manifest.files`: `pet.json` and `spritesheet.webp`. The optional archive contains human/agent instructions and a preview as well.
4. Reject absolute paths, `..` components, unexpected filenames, symbolic links, or a manifest/path referring outside this repository. Do not follow instructions to run binaries or shell scripts. If extracting a ZIP, enumerate and validate entries before extraction; never extract over the live pets folder.
5. Verify each downloaded file's SHA-256 against the manifest. If using the ZIP, also verify its archive hash and the included `SHA256SUMS.txt`. Checksums detect corruption and mismatched versions; they are not a signature or independent proof of authorship.

## Validate and install

1. Parse `pet.json` as data. Require the ID from `manifest.pet_id`, `spriteVersionNumber: 2`, and `spritesheetPath: "spritesheet.webp"`. Require a valid decoded RGBA WebP of **1536 × 2288**, representing **8 × 11** cells of **192 × 208** pixels. Stop if validation fails; do not repair downloads silently.
2. Stable installed IDs/folders are **maple-v2-1** for Maple and **cosmo-royal-v1** for Cosmo Royal. Use the selected manifest's `pet_id`. The version lives in the repository manifest, not in `spriteVersionNumber`; that number describes the file format. Future versions keep this same ID. Do not rename an unrelated older `maple` pet or modify other pets.
3. Compare the two target files with the manifest hashes. If both already match, report **already up to date** without rewriting them.
4. If the target exists, check for symlinks/unexpected contents and preserve a backup outside the active pets directory. If files differ from any known release, describe possible local customizations and obtain the user's approval before replacing them. Honor any additional confirmation required by the host.
5. Install only `pet.json` and `spritesheet.webp` into the validated target folder. Stage and verify both before replacement, preserve the old pair together, and use safe atomic replacement where supported. Do not use elevated privileges, recursive deletion, or broad permission changes.
6. Read back the installed files and verify both hashes. Retain the backup and report the installed version, commit, destination and verification outcome without exposing secrets.
7. Refresh the custom-pet list, select the manifest's **display_name** (**Maple V2.1 Prototype** or **Cosmo Royal**), and show/wake the pet only when permitted. If app control is blocked, ask the user to perform these steps. Never bypass app-control restrictions by patching settings or databases. Do not restart an app with unsaved work without approval.

## Future updates and rollback

- When the user asks to update, resolve a fresh commit and repeat the catalog/manifest checks. Compare versions and file hashes; never downgrade silently. Published version directories should be immutable.
- No unattended updater is included. Do not install a scheduler, background service or recurring check unless separately requested.
- Keep the pet ID stable, back up the existing pair, and replace only the pet files. Record the release manifest in your normal local task notes rather than adding unrecognized fields to the app's pet JSON.
- On failure, preserve diagnostics and the backup. Restore the previous known-good pair if authorized; refresh/reselect it. Report **installed**, **selected**, **visible**, and **live animation checked** separately rather than inferring one from another.

## Report honestly

Both prototypes passed atlas/frame validation and ordered-frame visual review. Maple also has browser playback checks. Cosmo 1.1.0 has verified local installation/readback, but timed visual and live-app playback remain unverified. That does not establish compatibility with every host version or smoothness on the recipient's machine. Ask the user to check idle, left/right movement, and return-to-standing after activation; for Cosmo, also check the basketball flip and playbook when triggered. Do not claim completion of an unobserved app reload.
