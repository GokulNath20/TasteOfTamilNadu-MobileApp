# 📑 Technical Notes — Taste of Tamil Nadu Mobile App

This file holds the developer details that were moved out of the main README: versions, setup steps, and how the app is built.

---

## 1. Overview

The app is a single React Native codebase that runs on Android and iOS. The source lives in the `taste-of-tamilnadu` project folder.

---

## 2. Versions

| Component | Version | Notes |
|:---|:---|:---|
| **React Native** | `0.80.2` | `0.81` was skipped because of JSI linking issues with Reanimated and Worklets |
| **React** | `19.1.0` | |
| **TypeScript** | `5.8` | |
| **Android Compile / Target SDK** | `35` (Android 15) | |
| **Android Min SDK** | `23` (Android 6.0) | |
| **Gradle** | `8.13` | |
| **Android Gradle Plugin (AGP)** | `8.12.0` | |
| **Java JDK** | `17` (LTS) | |
| **iOS Deployment Target** | `15.1+` | |
| **Xcode** | `16.1+` | |
| **CocoaPods** | `1.16.2` | |
| **Ruby** | `3.3.9` | Used by CocoaPods on macOS |
| **Node.js** | `24.x` (`>= 18` supported) | |
| **Yarn** | `1.22.17` | |

---

## 3. Main Libraries

* **Navigation:** `@react-navigation/native`, native stack, and bottom tabs
* **Layout:** `react-native-safe-area-context` for notches and gesture bars
* **Animation and carousels:** `react-native-reanimated`, `react-native-reanimated-carousel`, `react-native-basic-carousel`
* **Firebase:** `@react-native-firebase/app` and `storage` are installed, but the home screen no longer loads from Firebase. Promotions and menu photos are bundled with the app.
* **Splash screen:** `react-native-splash-view`
* **Testing and quality:** Jest, ESLint, Prettier

---

## 4. Build Notes

* **Android:** Release builds have code shrinking (ProGuard/R8) configured in Gradle.
* **Hermes:** Enabled as the JavaScript engine on Android.
* **Native layers:** Android uses Kotlin (`MainActivity.kt`, `MainApplication.kt`). iOS uses `AppDelegate.swift`.

---

## 5. Running the App for Development

From the `taste-of-tamilnadu` folder:

```bash
yarn install
yarn start --port 8082          # start Metro (the JavaScript dev server)
npx react-native run-android --port 8082   # build and install on a running emulator or device
```

* Use a port other than the default `8081` if another project is already using it. The app must connect to the same port its Metro server runs on.
* Start the emulator before running the Android command.
* For iOS, run `cd ios && pod install`, then `yarn ios`.

**Release build (no dev server needed):** run `./gradlew :app:assembleRelease` from the `android` folder. The JavaScript is bundled into the APK.

---

## 6. Known Issues

* Menu items are sample data in `src/data/menuCategories.ts`. Photos are in `src/assets/images/Menu/`, with authors and licenses in `CREDITS.md` in the same folder.
* Dark mode is not implemented. The app uses a fixed dark theme.
* Auth is a placeholder in `src/context/AuthContext.tsx`. Sign up and login use a phone number, but no SMS is sent and the verification code is not checked (dummy bypass). The session is kept in memory only. Replace it with a real phone-auth backend (for example Firebase Phone Auth) before release.
* The birthdate field is typed as DD/MM/YYYY. A date picker is not added yet.
* Feedback submission in `src/screens/Main/AboutUsScreen.tsx` is simulated and not stored anywhere yet.

---

## 7. Environment Managers (Optional)

* **Node.js:** `nvm`
* **Yarn:** `yvm`
* **Ruby:** `rvm` or `rbenv`
* **Java:** `sdkman`
