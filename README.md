# Trackion — Desktop App Downloads

Trackion is the desktop companion app for Trackion services. This repository hosts the official release artifacts (macOS, Windows) for installation and distribution.

Downloads and release assets are published on GitHub Releases:
https://github.com/trackionio/trackion-apps/releases

## Description

Trackion Desktop provides native functionality for activity monitoring, screenshots, system information and background helpers used by Trackion services. This repo contains the signed installers and compressed packages for each supported OS.

## Installation

Important: download the appropriate release file from the Releases page linked above.

### macOS (Intel / Apple Silicon)

Options: ZIP or DMG (signed)

- From ZIP:

  1. Download `Trackion-darwin-<arch>-<version>.zip`.
  2. Unzip and move the app to the Applications folder:
     ```
     unzip Trackion-darwin-<arch>-<version>.zip
     mv Trackion.app /Applications/
     ```
  3. Open Trackion from Applications. If macOS blocks opening due to Gatekeeper, right-click → Open and confirm.

- From DMG:
  1. Download `Trackion-<version>-<arch>.dmg`.
  2. Double-click to mount, drag `Trackion.app` to Applications, then eject the mounted volume.

### Windows (x64)

- Download `Trackion-<version>-Setup.exe`.
- Run the installer and follow the on-screen steps.
- For silent install (enterprise automation):
  ```
  Trackion-<version>-Setup.exe /S
  ```

<!-- Linux support removed: distribution packages are no longer published here. -->

## Verifying Downloads

Release pages include checksums for each artifact. Verify file integrity after download:

```
# Example (SHA256)
shasum -a 256 Trackion-darwin-x64-1.0.0.zip
```

Compare the output with the checksum published in the Release notes.

## Auto-Update

Trackion ships with a built-in updater that checks the public releases. Updates can be configured per-channel (stable/beta). Contact the maintainers for channel access or custom update server configuration.

## Support

If you encounter issues installing or updating the app, contact: support@trackion.io

When contacting support, please include:

- OS and version (e.g., macOS 14.1, Windows 11)
- App version you installed
- Exact file downloaded (filename)
- Any error messages or logs

## Privacy & Security

- All release artifacts are code-signed and served over HTTPS.
- Update manifests are published on the public repo and verified by the app on download.

## Licensing

See the LICENSE file included in each release artifact for licensing details.

---

For repository issues related to the releases themselves (missing assets, checksum mismatches, tagging problems), open an issue in this repository or email support@trackion.io.
