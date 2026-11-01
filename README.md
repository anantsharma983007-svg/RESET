# Build the RE:SET APK (free, ~5 minutes, no Android Studio)

An APK could not be built in the sandbox where this project was written (no Android SDK, downloads blocked), so this folder
is a ready-to-build Capacitor project. GitHub builds it for you.

1. Create a free GitHub account and a **new empty repository** (private is fine).
2. Upload everything in this folder to it (on github.com: Add file → Upload files; include the hidden
   `.github` folder — if the web uploader skips it, use `git push` instead).
3. Open the repo's **Actions** tab → **Build RE:SET APK** → **Run workflow**.
4. When it turns green (about 4–6 minutes), open the run and download the **reset-debug-apk** artifact.
   Unzip it to get `app-debug.apk`.
5. Send the APK to your phone and install it (Android will ask you to allow "install unknown apps").

Notes
- This is a **debug-signed** APK: fine for personal use and testing, not for Google Play. A Play Store
  release needs your own signing key (`assembleRelease` + keystore).
- The app id is `com.aetherforge.reset`; change it in `capacitor.config.json` before the first build if you want another.
- Data is stored in the app's own WebView storage on the phone. Use Settings → Data & privacy → Export backup before uninstalling.
- Not yet tested on a real device: the workflow itself has not been run by me.
