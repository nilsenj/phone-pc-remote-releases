# Phone PC Remote — official downloads

Use your Android phone to control a Windows or Ubuntu computer on your local network. Start at the [download page](https://nilsenj.github.io/phone-pc-remote/) or choose a platform below. You need the Android app **and** a desktop companion.

## Download

| Platform | Download | Status |
| --- | --- | --- |
| Android | [Google Play](https://play.google.com/store/apps/details?id=dev.phonepcremote.app) · [GitHub APK for fresh sideloads](https://github.com/nilsenj/phone-pc-remote-releases/releases/tag/android-v0.1.32) | Use Google Play for regular updates and Pro purchases |
| Windows 11 x64 | [Microsoft Store](https://apps.microsoft.com/detail/9NP7CKV77CRK) | Free MSIX Store app; no EXE installer |
| Ubuntu 24.04+ amd64 | [`.deb` 0.1.27 beta](https://github.com/nilsenj/phone-pc-remote-releases/releases/tag/desktop-v0.1.27-beta.1) | Beta; physical-hardware and crash recovery validation incomplete |

The 0.1.32 GitHub APK uses a different signing certificate from Google Play and earlier GitHub APKs. It requires a fresh install. Uninstalling can erase pairings or app data. Keep using Google Play for an existing Play installation.

Phone-as-webcam is available in the Ubuntu beta, not in the Windows MSIX app. Bluetooth control is not offered in the current release. Read the [Ubuntu beta notes](https://github.com/nilsenj/phone-pc-remote-releases/releases/tag/desktop-v0.1.27-beta.1) before using its camera feature.

## Getting started

1. Install the Android app and the appropriate desktop companion above.
2. Connect the phone and computer to a mutually reachable local network. Guest Wi-Fi or device isolation can prevent discovery.
3. Launch Phone PC Remote on the computer and scan its pairing QR code in the Android app.
4. Follow the pairing prompts. Do not share the QR code or pairing credentials publicly.

See [installation and update instructions](INSTALL.md).

## Releases and updates

The Ubuntu release includes a versioned `.deb`, notes and `SHA256SUMS.txt`. Ubuntu updates are currently installed manually over the existing package; an APT repository or automatic updater is not available. Windows installation and updates go through Microsoft Store. Android GitHub APK updates remain separate from Google Play.

Only download installers from the official links above. Do not disable security protections to bypass an installer warning. Checksums detect corruption; they are not a substitute for signing and trusted download sources.

## Repository scope

This repository hosts public release assets and installation instructions for Phone PC Remote.

## Reporting problems

[Open an issue](https://github.com/nilsenj/phone-pc-remote-releases/issues) with the app version, operating-system version, and reproduction steps. Remove pairing codes, QR codes, private network addresses, personal files, and other sensitive information from screenshots or logs before posting.
