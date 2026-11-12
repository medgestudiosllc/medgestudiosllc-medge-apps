<p align="center">
  <img src="assets/medge-mark.png" width="48" alt="MEdge">
</p>

<h1 align="center">MEdge Apps</h1>

<p align="center">
  Android test builds of the apps made by <a href="https://medgecreatives.com">MEdge Studios</a>.<br>
  Install them straight from the APK files here, before they reach the Play Store.
</p>

<p align="center">
  <a href="https://medgecreatives.com/products#apps">medgecreatives.com/products</a> ·
  <a href="https://github.com/medgestudiosllc/medgestudiosllc-medge-apps/releases">All releases</a>
</p>

---

## Download

| | App | Version | Size | Download |
|---|---|---|---|---|
| <img src="assets/icons/coinbuddy.png" width="56" alt=""> | **CoinBuddy**<br>Buy and sell crypto with Mobile Money in Ghana, with app lock and order updates. | 1.4.0 (beta) | 137 MB | [**Download APK**](https://github.com/medgestudiosllc/medgestudiosllc-medge-apps/releases/download/coinbuddy-v1.4.0/CoinBuddy-1.4.0.apk) |
| <img src="assets/icons/homescout.png" width="56" alt=""> | **HomeScout**<br>Browse verified rental homes across Ghana and message owners directly. | 1.0.0 (test build) | 105 MB | [**Download APK**](https://github.com/medgestudiosllc/medgestudiosllc-medge-apps/releases/download/homescout-v1.0.0/HomeScout-1.0.0.apk) |
| <img src="assets/icons/whisper.png" width="56" alt=""> | **Whisper**<br>A calm Telegram client with folders, stories and an app lock. | 0.1.0, build 6 (test build) | 129 MB | [**Download APK**](https://github.com/medgestudiosllc/medgestudiosllc-medge-apps/releases/download/whisper-v0.1.0-build6/Whisper-0.1.0-build6.apk) |

Short links you can share, which always point to the newest build:

- `medgecreatives.com/download/coinbuddy`
- `medgecreatives.com/download/homescout`
- `medgecreatives.com/download/whisper`

All apps need **Android 7 or later**. iPhone versions go out through TestFlight; ask us for an invite at hello@medgecreatives.com.

## How to install

1. **Download the APK.** Open a download link on your Android phone. Chrome may warn that the file can harm your device; tap **Download anyway**.
2. **Allow installs from your browser.** Open the file from your notifications or the Downloads app. The first time, Android asks for permission: tap **Settings**, turn on **Allow from this source**, then go back.
3. **Install and open.** Tap **Install**, then **Open**, or find the app on your home screen. If Play Protect asks to scan the app, tap **Scan app** or **Install anyway**.
4. **Updating later.** Download the newer APK and install it over the old one. Your sign-in and settings stay. If Android says the package conflicts, uninstall the old version first.

Only install APKs from this page or from medgecreatives.com.

## Checking a download

Each release lists the file's SHA-256 checksum. To check a file on a computer:

```sh
shasum -a 256 CoinBuddy-1.4.0.apk
```

The result should match the checksum in the release notes.

## Notes

- These are test builds. They can have bugs; tell us what you find at hello@medgecreatives.com.
- Whisper is an unofficial app built on the Telegram API. It is not affiliated with Telegram.
- This repository holds the release files only. The apps' source code is private.

## For the MEdge team: publishing a new build

1. Build the APK with EAS (`eas build --profile preview --platform android`) and download it.
2. Add an entry to `releases.json` with the tag (`<app>-v<version>`, for example `coinbuddy-v1.5.0`), the file name, the EAS artifact URL and the APK's SHA-256 (`shasum -a 256 file.apk`). Push to `main`: the **Publish releases** workflow downloads the APK, checks the checksum and creates the release.
3. Update `apkUrl` and `version` for the app in `src/lib/apps-data.ts` in the medge-creatives-web repo. The `/download/<app>` link then points to the new file.
4. Update the table above.

---

<p align="center">
  <sub>© 2026 MEdge Studios LLC · <a href="https://medgecreatives.com">medgecreatives.com</a></sub>
</p>
