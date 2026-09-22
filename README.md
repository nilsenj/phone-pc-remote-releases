# Phone PC Remote — desktop downloads

Windows and Ubuntu companion apps for Phone PC Remote on Android.

## Download status

**No desktop installers have been published here yet.** Release candidates are being validated. Windows signing is pending; Ubuntu remains beta pending real-hardware validation. This page is not a claim that the builds are production-ready.

| Platform | Package | Status |
| --- | --- | --- |
| Windows x64 | `.exe` installer | Signing and release validation pending |
| Ubuntu amd64 | `.deb` package | Ubuntu 24.04 baseline; beta validation pending |
| Android | Google Play | Separately managed; availability depends on testing access and region |

[View desktop releases](https://github.com/nilsenj/phone-pc-remote-releases/releases) · [Android on Google Play](https://play.google.com/store/apps/details?id=dev.phonepcremote.app)

## Getting started

1. Install the appropriate desktop companion when a release becomes available.
2. Connect the phone and computer to a mutually reachable local network. Guest Wi-Fi or device isolation can prevent discovery.
3. Launch Phone PC Remote on the computer and scan its pairing QR code in the Android app.
4. Follow the pairing prompts. Do not share the QR code or pairing credentials publicly.

See [installation and update instructions](INSTALL.md).

## Releases and updates

Published releases will include versioned installers, release notes, and SHA-256 checksums. Initially, updates are installed manually over the existing version. Automatic desktop updates are not currently promised.

Only download installers from releases linked by this repository. Do not disable security protections to bypass an installer warning. Checksums detect corruption; they are not a substitute for signing and trusted download sources.

## Repository scope

This repository is for desktop distribution documentation and release assets. It does not contain the application's private source repository, development builds, test packages, or signing credentials. Android publishing is managed separately.

## Reporting problems

[Open an issue](https://github.com/nilsenj/phone-pc-remote-releases/issues) with the app version, operating-system version, and reproduction steps. Remove pairing codes, QR codes, private network addresses, personal files, and other sensitive information from screenshots or logs before posting.
