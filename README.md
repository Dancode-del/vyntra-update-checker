# Vyntra Update Checker

A responsive static website for Vyntra Android update information.

## Enable hosting
In this repository, open **Settings → Pages** and select:
- Source: Deploy from a branch
- Branch: `main`
- Folder: `/ (root)`

The page will be available at:
`https://dancode-del.github.io/vyntra-update-checker/`

## Update manifest
The checker fetches:
`https://raw.githubusercontent.com/Dancode-del/vyntra-update/main/update.json`

Optional query parameters from the app:
- `versionCode` — installed Android version code
- `versionName` — installed version name
- `abi` — device ABI

Example:
`?versionCode=10&versionName=1.0.0&abi=arm64-v8a`

## Security boundary
This website is presentation only. It does not verify APK signatures, hashes, package identity or installation permission. Those checks must be performed by the Android app itself. The initial manifest is explicitly marked as pending verification until a signing key pair is configured.
