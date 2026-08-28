# 📑 Technical & Architectural Notes — Taste of Tamil Nadu Mobile App

## 1. Overview & Objectives

The primary engineering goal of the **Taste of Tamil Nadu** mobile application was to deliver a responsive, visually engaging, and reliable mobile experience for restaurant customers across both iOS and Android platforms with a single unified codebase.

---

## 2. Platform Compatibility & Matrix

| Component | Target Version | Release / Documentation Reference |
|:---|:---|:---|
| **React Native** | `0.81.0` | [React Native Releases](https://reactnative.directory/) |
| **React** | `19.1.0` | [React 19 Documentation](https://react.dev/) |
| **Android Compile / Target SDK** | `35` (Android 15) | [Android API Levels](https://apilevels.com/) |
| **Android Min SDK** | `23` (Android 6.0) | Supports >99% active Android devices |
| **Gradle** | `8.13` | [Gradle Compatibility Guide](https://docs.gradle.org/8.13/userguide/compatibility.html) |
| **Android Gradle Plugin (AGP)**| `8.12.0` | [AGP Release Notes](https://developer.android.com/build/releases/gradle-plugin) |
| **Java JDK** | `17` (LTS) | Safest LTS build for Gradle 8.x |
| **iOS Deployment Target** | `iOS 15.1+` | Minimum standard for React Native 0.81 |
| **Xcode** | `16.1+` | [Apple Developer Xcode Support](https://developer.apple.com/support/xcode/) |
| **CocoaPods** | `1.16.2` | [CocoaPods Gem Releases](https://rubygems.org/gems/cocoapods/versions/1.16.2) |
| **Ruby** | `3.3.9` | Required for macOS CocoaPods runtime |

---

## 3. Key Architecture & Engineering Decisions

### 📱 UI & Screen Adaptation
* **Edge-to-Edge Navigation:** Utilizing `react-native-safe-area-context` for dynamic handling of camera notches, iOS Dynamic Island, and Android gesture navigation bars.
* **Theme Switching:** Adaptive color palette supporting system-level Dark and Light mode presets.

### ⚡ Performance & Build Optimizations
* **Android ProGuard & R8:** Pre-configured ProGuard rules for code shrinking and obfuscation on release builds.
* **Hermes Engine:** JavaScript engine enabled for optimized startup time, lower memory footprint, and smaller APK/IPA sizes.
* **Modern Kotlin Integration:** Android native layer structured with Kotlin (`MainActivity.kt`, `MainApplication.kt`) for better native bridge support.
* **Swift Native Entry on iOS:** `AppDelegate.swift` configured with Xcode 16 compatibility.

---

## 4. Environment Version Managers Reference

Recommended CLI tooling for reproducible development environments:
* **Node.js:** `nvm` (Node Version Manager)
* **Yarn:** `yvm` (Yarn Version Manager)
* **Ruby:** `rvm` / `rbenv` (Ruby Version Manager)
* **Java:** `sdkman` (Software Development Kit Manager)
