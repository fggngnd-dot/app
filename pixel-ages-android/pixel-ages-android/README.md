# Pixel Ages for Android

The whole game is one file: `www/index.html`. This project wraps it in an
Android app using Capacitor. Pick whichever way below is easiest for you.

## Option A: get the APK from GitHub (no installs)

1. Create a free GitHub account and a new empty repository.
2. Upload everything in this folder to it, including the hidden `.github` folder.
3. Open the repository's **Actions** tab, choose **Build APK**, press **Run workflow**.
4. After a few minutes, open the finished run and download **pixel-ages-apk**.
   Unzip it to get `app-debug.apk`.
5. Copy the APK to your phone and open it. Android will ask you to allow
   installs from that source the first time.

## Option B: build it with Android Studio

1. Install Node.js 20 or newer and Android Studio.
2. In this folder run:
   ```
   npm install
   npx cap add android
   npx cap sync android
   npx cap open android
   ```
3. In Android Studio choose **Build > Build APK(s)**.

## Notes

- The pixel fonts load from Google Fonts, so the first launch needs internet.
  Without it the game still works and falls back to a plain monospace font.
- Progress is saved on the device.
- This builds a debug APK, which is fine for installing on your own phone.
  Publishing to the Play Store needs a signed release build.
- To change the game, edit `www/index.html`, then run `npx cap sync android`
  (or push again if you use GitHub).
