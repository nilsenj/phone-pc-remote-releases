# Phone PC Remote desktop companions — beta

These desktop apps work with the Phone PC Remote Android app. Ubuntu remains
beta pending real-hardware validation. No automatic desktop updater is promised.

## Windows x64

Download the Windows installer from the project's official release page.
Check its Digital Signatures tab for the expected publisher before installing.
Unsigned local test candidates are not approved public releases. Do not disable
Windows security protections to install them.

Launch Phone PC Remote and pair using the QR code from the Android app.
Allow local-network access when Windows prompts. Both devices must be able to
reach each other on the local network; guest Wi-Fi may isolate devices.

## Ubuntu amd64

For the tested Ubuntu 24.04 baseline, install the downloaded package with:

```sh
sudo apt install ./phone-pc-remote-VERSION-ubuntu-amd64.deb
```

Replace VERSION with the downloaded version. Launch from the application menu,
then scan its pairing QR code in the Android app. Camera and remote-input support
depend on kernel modules and desktop-session permissions. Report setup errors;
do not run the network-facing app as root to work around them.

## Updates and verification

Install a newer package over the existing installation; do not uninstall first
or delete the app's data directory. Verify retained pairing after updating.
Keep earlier installers available for troubleshooting, but do not assume that
downgrading across data-format changes is supported.

SHA256SUMS.txt records the exact installer hashes. Hashes detect corrupted or
mismatched downloads; they do not replace trusted download sources or signing.

Development builds, signing keys, credentials, and test packages must never be
included in a public desktop release.

