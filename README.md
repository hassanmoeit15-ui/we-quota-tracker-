# WE Home Wi-Fi Tracker (350 GB Egypt Quota)

Private family Android app built with **Kotlin + Jetpack Compose + Material 3 + Firebase Firestore + GitHub Actions**.

## Features
- **WE 350 GB Package Card**: Tracks total quota (350 GB), used/remaining GB, progress bar, and renewal day countdown synced via a shared **Home Group Code**.
- **Wi-Fi Only Per-Device Tracking**: Uses `NetworkStatsManager.querySummaryForDevice(ConnectivityManager.TYPE_WIFI, ...)` so 4G/5G mobile data is completely ignored.
- **Router Subnet Scanner (`192.168.1.1 - 192.168.1.254`)**: Detects online TVs, laptops, consoles, and phones on the WE home router and computes estimated **Other / Unmonitored Devices** usage.
- **Bilingual Arabic (RTL) & English (LTR)** with Light and Dark Material 3 themes.
- **Cloud APK Builds via GitHub Actions**: Compiles and signs `app-release.apk` directly in GitHub Actions without needing Android Studio or a PC.

## Quick Setup from a Mobile Phone
1. Create a free Firebase project at `console.firebase.google.com`, register an Android app with package name `com.wequota.tracker`, enable **Firestore Database** and **Anonymous Authentication**, and download `google-services.json`.
2. Upload these project files to a GitHub repository and place `google-services.json` inside the `app/` folder.
3. Open the **Actions** tab on GitHub -> **Build Signed Release APK** -> wait ~3 minutes -> download **app-release-apk** -> extract and install `app-release.apk`.
