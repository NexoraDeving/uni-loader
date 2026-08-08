# uni-loader

Central release catalog for the uni-loader ecosystem.

This repository now keeps a fixed app manifest in `apps.json` and a fixed naming scheme for release assets.

Updater flow:

1. The loader fetches `https://raw.githubusercontent.com/NexoraDeving/uni-loader/main/apps.json`.
2. It reads `currentVersion`, `currentAsset`, and `downloadUrl`.
3. It downloads the matching asset from `releases/latest/download/...`.
4. You only need to upload a new release asset and update the matching entry in `apps.json`.

Asset naming:

- `aclr-v1.0.0.exe` for Atlas Free Cleaner
- `atmp-v1.0.0.exe` for Atlas Free Temp
- `afn-v1.0.0.exe` for Atlas Fortnite Free
- `aperm-v1.0.0.exe` for Atlas Perm Spoofer
- `rbx-v0.9.0-beta.exe` for Atlas Roblox External
- `ul-v0.0.0-placeholder.txt` until the new Uni Loader build exists
- `cs2-v0.0.0-placeholder.txt` until the new CS2 build exists

Workflow:

1. Build the app.
2. Rename the file to the exact asset name from `apps.json`.
3. Upload the renamed file to the latest GitHub Release.
4. Update `apps.json` only when the version or asset name changes.

No local loader code is required for this repository change.
