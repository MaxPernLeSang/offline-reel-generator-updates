# Offline Reel Generator — updates

Public update channel for the Offline Reel Generator Mac app.

The app reads `version.json` at launch. When `version` is higher than the
installed version, it shows an "Update available" window with `notes` and a
**Download** button that opens `url`.

## Publishing an update

1. Bump `APP_VERSION` in `core/version.py` in the app and build the DMG.
2. Create a release here (tag `v1.2.0`) and attach the DMG.
3. Edit `version.json`: set `version` to `1.2.0` and write one short sentence in `notes`.

Users are told at their next launch. The DMG is useless without a valid
license key, so it is fine for it to be public.

## Format

```json
{
  "version": "1.2.0",
  "notes": "New subtitle styles and faster export.",
  "url": "https://github.com/MaxPernLeSang/offline-reel-generator-updates/releases/latest"
}
```

`version` is compared number by number (1.10.0 is newer than 1.9.0).
`url` must start with `https://`.
