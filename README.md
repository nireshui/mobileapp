# Paanam – Android app (Capacitor)

## Option A: GitHub (no Android Studio needed)
1. Create a new GitHub repo and push this folder.
2. Open the repo > Actions > "Build APK" (runs automatically on push).
3. Download `paanam-debug-apk` from the run's Artifacts, unzip, install `app-debug.apk` on your phone.

## Option B: Locally
Needs Node 20+, JDK 21, Android SDK.
    npm install
    npx cap sync android
    cd android && ./gradlew assembleDebug
APK: android/app/build/outputs/apk/debug/app-debug.apk
(or `npx cap open android` and Build > Build APK in Android Studio)

Screens live in `www/`. Edit them, then run `npx cap sync android` and rebuild.
Note: pages load Tailwind and fonts from CDNs, so the app needs internet.
