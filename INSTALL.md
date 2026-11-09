# Install Phone PC Remote

Install Phone PC Remote for [Android from Google Play](https://play.google.com/store/apps/details?id=dev.phonepcremote.app) and one desktop companion. Both devices must be able to reach each other on the same local network. Use Google Play for Android updates and Pro purchases. The GitHub 0.1.32 APK is for a fresh sideload and cannot update earlier GitHub or Play installations.

## Windows 11 x64

Install the free [Windows app from Microsoft Store](https://apps.microsoft.com/detail/9NP7CKV77CRK). It is distributed as an MSIX Store app; there is no public EXE installer. The Store handles Windows updates. Phone-as-webcam is not supported in the Windows version.

Launch Phone PC Remote on Windows and scan its pairing QR code with the Android app. Allow local-network access if Windows prompts. Guest Wi-Fi or device isolation can prevent pairing. Do not share the QR code.

## Ubuntu 24.04+ amd64 beta

Download [`Phone.PC.Remote_0.1.27_amd64.deb`](https://github.com/nilsenj/phone-pc-remote-releases/releases/download/desktop-v0.1.27-beta.1/Phone.PC.Remote_0.1.27_amd64.deb) and the matching [`SHA256SUMS.txt`](https://github.com/nilsenj/phone-pc-remote-releases/releases/download/desktop-v0.1.27-beta.1/SHA256SUMS.txt) from the [Ubuntu beta release](https://github.com/nilsenj/phone-pc-remote-releases/releases/tag/desktop-v0.1.27-beta.1). In the directory containing both files, verify and install:

```sh
sha256sum -c SHA256SUMS.txt
sudo apt install ./Phone.PC.Remote_0.1.27_amd64.deb
```

Launch from the application menu, then scan the desktop app's pairing QR code with the Android app. Camera and remote-input support depend on kernel modules and desktop-session permissions. The webcam feature needs `v4l2loopback-dkms` and matching kernel headers; Secure Boot may require module signing/enrolment. Do not run the network-facing app as root to work around setup errors.

This build passed package checks on Ubuntu 24.04. Pairing and mirroring were exercised with the Ubuntu companion in WSL. Native Wayland and webcam behavior remain unverified for this build. The previous beta could require a reboot to restore the webcam after a crash.

## Updates and verification

For Ubuntu, download and install a newer `.deb` over the existing installation; there is no APT repository or automatic desktop updater. Do not uninstall first or delete the app's data directory. Verify retained pairing after updating.
Keep earlier installers available for troubleshooting, but do not assume that
downgrading across data-format changes is supported.

`SHA256SUMS.txt` records the exact Ubuntu package hash. Hashes detect corrupted or mismatched downloads; they do not replace trusted download sources or signing.

Development builds, signing keys, credentials, and test packages must never be
included in a public desktop release.
