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
2. Zip the launcher output as `ModdedEvolveLauncher.zip`.
3. Create or update the GitHub release.
4. Use the tag `Launcher_Update` for the current update channel.
5. Upload `ModdedEvolveLauncher.zip` as the release asset.
6. Update `version.json` so `latestVersion`, `downloadUrl`, and `changelogUrl` match the release.

Current release page:

```text
https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/tag/Launcher_Update
```

Current release asset URL:

```text
https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/download/Launcher_Update/ModdedEvolveLauncher.zip
```

## Example version.json

```json
{
  "latestVersion": "0.0.6",
  "minimumVersion": "0.0.5",
  "downloadUrl": "https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/download/Launcher_Update/ModdedEvolveLauncher.zip",
  "changelogUrl": "https://github.com/MeH0y/ModdedEvolveLauncherUpdates/releases/tag/Launcher_Update",
  "message": "Launcher update available."
}
```
