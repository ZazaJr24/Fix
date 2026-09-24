# Fixes

Fix archives for ResonanceTools.

- `fixes.json` — catalog the app reads (App ID, game name, fixes).
- `fixes/<appid>/<n>.<ext>` — the archive files (stored with Git LFS).

## Adding a fix

1. Put the archive in `fixes/<appid>/`, e.g. `fixes/449800/2.zip`.
2. Add an entry to that game's `fixes` list in `fixes.json` (or a new game object):

```json
{ "appid": "449800", "name": "Game name", "fixes": [
  { "filename": "Name shown in the app.zip", "path": "fixes/449800/2.zip", "size": "4.2 MB", "badges": [] }
] }
```

3. Commit and push. The app picks it up on the next refresh.
