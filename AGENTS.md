# Project instructions

## Scope

This repository is the source for the Vintage Story mod **Petroleum Age: Iron & Refining Patch**
(ModID `petroleumpatch`). The mod's files sit at the repository root so the release archive can be
built directly from it.

## Release rule: every change ships as a new version

Any change to the mod's files (`modinfo.json`, `assets/`, `modicon.png`) must be released as a
complete new version. Do not leave a change applied only in the working tree.

For every shipped change:

1. Bump `version` in `modinfo.json` using semantic versioning:
   - patch (`1.1.3` → `1.1.4`) for fixes and balance tweaks
   - minor (`1.1.3` → `1.2.0`) for new content or new recipes
   - major only for breaking changes that invalidate existing saves or setups
2. Add a matching section at the top of `CHANGELOG.md` headed `## <new version>`, listing what
   changed. Keep the newest version first.
3. Rebuild the release archive at the repository root, named `petroleumpatch_<version>.zip`,
   containing only:
   - `modinfo.json`
   - `modicon.png`
   - `assets/`
   Exclude development docs (`README.md`, `CHANGELOG.md`, `SUMMARY.md`, `MODDB.md`,
   `moddb-logo.png`).
4. Verify the archive: `unzip -t <zip>` reports no errors, `modinfo.json` inside the zip matches
   the repository copy, and the result is reported with its size and SHA-256.
5. Remove the previous release zip so an outdated file cannot be uploaded by mistake. Release
   zips are gitignored and are attached to GitHub releases, not committed.
6. Update `README.md`, `SUMMARY.md`, and `MODDB.md` if the change alters features, requirements,
   or automation steps, and keep `SUMMARY.md` and `MODDB.md` identical.
7. Commit the change, tag it `v<version>`, and publish a GitHub release with the zip attached.
   ModDB still needs a manual upload; copy the changelog section into the release field.

## ModID rules

The ModID must contain only lowercase letters and digits. Underscores, dashes, spaces, and
uppercase letters are rejected by Vintage Story and ModDB with "ModID ... is malformed". The
current ID is `petroleumpatch`; keep it stable once released.

## Verification

- Validate every edited `.json` file with `python3 -c "import json;json.load(...)"`.
- The server loads this repository through a bind mount at
  `/vintagestory/data/Mods/petroleumpatch` (host path `/hdd/repos/petroleumpatch`).
- A server restart is required to load changed assets: `docker restart vintagestory_1_22_7`.
  Do not restart the live server without asking first; check
  `docker logs --tail 20 vintagestory_1_22_7` afterwards for asset or patch errors.

## Packaging constraints

- ModDB logo and in-game icon are both exactly 480×480 PNG.
- Folder name does not affect mod identity; the ModID is what matters.
