# Install Phone PC Remote

Install the [Android app](https://github.com/nilsenj/phone-pc-remote-releases/releases/tag/android-v0.1.26) and one desktop companion. Both devices must be able to reach each other on the same local network. The GitHub Android APK is signed differently from Google Play and cannot update an existing Play installation; switching channels may erase app data and pairings. Google Play is currently limited to testers.

## Windows 11 x64

Install the free [Windows app from Microsoft Store](https://apps.microsoft.com/detail/9NP7CKV77CRK). It is distributed as an MSIX Store app; there is no public EXE installer. The Store handles Windows updates. Phone-as-webcam is not supported in the Windows version.

Launch Phone PC Remote on Windows and scan its pairing QR code with the Android app. Allow local-network access if Windows prompts. Guest Wi-Fi or device isolation can prevent pairing. Do not share the QR code.

## Ubuntu 24.04+ amd64 beta

Download [`Phone.PC.Remote_0.1.26_amd64.deb`](https://github.com/nilsenj/phone-pc-remote-releases/releases/download/desktop-v0.1.26-beta.1/Phone.PC.Remote_0.1.26_amd64.deb) and the matching [`SHA256SUMS.txt`](https://github.com/nilsenj/phone-pc-remote-releases/releases/download/desktop-v0.1.26-beta.1/SHA256SUMS.txt) from the [Ubuntu beta release](https://github.com/nilsenj/phone-pc-remote-releases/releases/tag/desktop-v0.1.26-beta.1). In the directory containing both files, verify and install:

```sh
sha256sum -c SHA256SUMS.txt
sudo apt install ./Phone.PC.Remote_0.1.26_amd64.deb
```

Launch from the application menu, then scan the desktop app's pairing QR code with the Android app. Camera and remote-input support depend on kernel modules and desktop-session permissions. The webcam feature needs `v4l2loopback-dkms` and matching kernel headers; Secure Boot may require module signing/enrolment. Do not run the network-facing app as root to work around setup errors.

This build passed package checks and a phone-camera start/stop/restart test in an Ubuntu VirtualBox VM, not on a physical Ubuntu computer. After an unexpected app crash following camera use, the virtual camera may lose capture capability until Ubuntu is rebooted. Read the release notes before relying on it.

## Updates and verification

For Ubuntu, download and install a newer `.deb` over the existing installation; there is no APT repository or automatic desktop updater. Do not uninstall first or delete the app's data directory. Verify retained pairing after updating.
Keep earlier installers available for troubleshooting, but do not assume that
downgrading across data-format changes is supported.

`SHA256SUMS.txt` records the exact Ubuntu package hash. Hashes detect corrupted or mismatched downloads; they do not replace trusted download sources or signing.

Development builds, signing keys, credentials, and test packages must never be
included in a public desktop release.

