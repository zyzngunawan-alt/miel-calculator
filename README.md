# Miel Calculator

Cute offline-first calculator starter for Android, using Vite + Capacitor.

## Project files
- `index.html`, `style.css`, `app.js`: calculator interface and behavior.
- `package.json`, `vite.config.js`: web build setup.
- `capacitor.config.json`: Android wrapper configuration.
- `codemagic.yaml`: cloud workflow that builds a debug APK.
- `assets/miel-icon.svg`: local app icon asset.
- `sw.js` and `manifest.webmanifest`: optional browser PWA offline support.

## Build in Codemagic
1. Upload the contents of this folder to the root of a GitHub repository (not the ZIP file itself).
2. In Codemagic, connect the GitHub repository and select the `miel-android-debug` workflow.
3. Start a build. On success, download the APK from Artifacts.

The workflow generates the Android project in the cloud, builds `assembleDebug`, and collects the APK. This is a test/debug APK, not a Play Store release. For a distributable release APK, configure Android signing in Codemagic and build `assembleRelease`.

## Notes
- Core calculator files and icon are bundled locally; the app does not need a network connection for its calculator functions.
- The current Miel character is a placeholder illustration, not the final visual-novel character artwork.
- Test the APK on a real Android device before relying on it.
