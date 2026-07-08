# Modded Evolve Launcher Updates

Static update files for the Modded Evolve Launcher.

## Files

- `version.json` tells the launcher what the latest available build is.
- `news.json` can be used by the launcher for remote news later.

## Update Manifest URL

After this repo is pushed to GitHub, the launcher can read `version.json` from:

```text
https://raw.githubusercontent.com/MeH0y/ModdedEvolveLauncherUpdates/main/version.json
```

## Release Flow

1. Build the launcher as x64.
2. Confirm the output folder contains `ModdedEvolveUpdater.exe` beside `ModdedEvolveLauncher.exe`.
3. Zip the launcher output as `ModdedEvolveLauncher.zip`.
4. Create or update the GitHub release.
5. Use the tag `Launcher_Update` for the current update channel.
6. Upload `ModdedEvolveLauncher.zip` as the release asset.
7. Update `version.json` so `latestVersion`, `minimumVersion`, `downloadUrl`, and `changelogUrl` match the release.
8. Optional: fill `sha256` with the final zip hash after the release asset is stable.

Current release page:

```text
https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/tag/Launcher_Update
```

Current release asset URL:

```text
https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/download/Launcher_Update/ModdedEvolveLauncher.zip
```

## Auto-Updater Notes

The launcher downloads `ModdedEvolveLauncher.zip`, starts `ModdedEvolveUpdater.exe`, closes itself, and lets the updater replace the launcher files. The updater supports either package shape:

```text
ModdedEvolveLauncher.zip
  ModdedEvolveLauncher.exe
  Assets/
```

or:

```text
ModdedEvolveLauncher.zip
  ModdedEvolveLauncher/
    ModdedEvolveLauncher.exe
    Assets/
```

## Example version.json

```json
{
  "latestVersion": "0.0.7",
  "minimumVersion": "0.0.5",
  "downloadUrl": "https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/download/Launcher_Update/ModdedEvolveLauncher.zip",
  "changelogUrl": "https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/tag/Launcher_Update",
  "sha256": "",
  "message": "Launcher update available."
}
```
