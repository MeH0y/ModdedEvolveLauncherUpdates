# Modded Evolve Launcher Updates

Static update files for the Modded Evolve Launcher.

## Files

- `version.json` tells the launcher what the latest available build is.
- `news.json` can be used by the launcher for remote news later.

## Update Manifest URL

After this repo is pushed to GitHub, the launcher can read `version.json` from:

```text
https://raw.githubusercontent.com/YOUR_USERNAME/ModdedEvolveLauncherUpdates/main/version.json
```

Replace `YOUR_USERNAME` with the GitHub account or organization that owns the repo.

## Release Flow

1. Build the launcher as x64.
2. Zip the launcher output as `ModdedEvolveLauncher.zip`.
3. Create a GitHub release.
4. Use a tag like `v0.0.6`.
5. Upload `ModdedEvolveLauncher.zip` as the release asset.
6. Update `version.json` so `latestVersion`, `downloadUrl`, and `changelogUrl` match the new release.

Example release asset URL:

```text
https://github.com/YOUR_USERNAME/ModdedEvolveLauncherUpdates/releases/download/v0.0.6/ModdedEvolveLauncher.zip
```

## Example version.json

```json
{
  "latestVersion": "0.0.6",
  "minimumVersion": "0.0.5",
  "downloadUrl": "https://github.com/YOUR_USERNAME/ModdedEvolveLauncherUpdates/releases/download/v0.0.6/ModdedEvolveLauncher.zip",
  "changelogUrl": "https://github.com/YOUR_USERNAME/ModdedEvolveLauncherUpdates/releases/tag/v0.0.6",
  "message": "Launcher update available."
}
```
