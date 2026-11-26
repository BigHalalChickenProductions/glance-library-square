# Glance Library Square

A modified build of [Glance Library](https://github.com/shak18/glance-library) (MIT, by Michael Palma) for Steam Deck Game Mode, installed through Decky Loader.

## Changes from the original
- Portrait capsules are shown square everywhere (info panel, collection covers, capsule-only grid cards). Works with SteamGridDB square capsules.
- Background image is shown at full brightness (no dimming filter or vignette).
- The grid runs to the bottom of the screen (no space reserved for the footer).
- Updates come from this repository, not the original one.
- Built-in tab manager (no TabMaster needed): Quick Access menu > Glance Library > Library Tabs > **Edit library tabs**. Add tabs for any Steam collection or the built-in lists, then rename, hide, reorder or delete them. Per-tab options: installed games only, hide when empty. Existing TabMaster tabs can be imported.

## Updating from the Deck
Quick Access menu > Glance Library > Updates. When a newer release exists it shows **Update to X**; Decky asks you to confirm, installs it and reloads.

## Publishing a new version (browser only)
1. Change the files you need (for example `dist/index.js`).
2. Raise the `version` in `package.json` **and** `plugin.json` (for example `1.1.2.2`). Keep both the same.
3. Commit to `main`. The `release` workflow builds `glance-library.zip` and publishes release `v<version>` automatically. If that version already has a release, nothing happens.

The updater only offers versions higher than the installed one, so always raise the number.

## Notes
- The repository must stay public so the Deck can read releases.
- Original license and third-party notices are kept in `LICENSE` and `THIRD_PARTY_LICENSES.md`.
