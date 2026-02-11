# Mobile App (Expo + React Native)

This folder contains the Expo (React Native) app for this course. This README is a quickstart for bootstrapping and running the app. The detailed walkthrough and explanations live in the WEBD 430 Week 3 lectures.

## Platform note

- Windows/Linux: build and test Android locally.
- macOS: build and test Android and iOS locally.

## Quickstart (dev builds)

Run these commands from the repo root unless the command includes `cd mobile`.

0) Start an emulator/simulator

- Android: start an AVD in Android Studio.
- iOS (macOS only): start iOS Simulator from Xcode.

1) Create the app in this folder

```bash
cd mobile
npx create-expo-app .
```

If `create-expo-app` prompts you about overwriting files, try not to overwrite `mobile/eas.json`. If you overwrite it anyway, recreate it using the template at the bottom of this README.

2) Install dependencies and the dev client package

```bash
cd mobile
npm install
npx expo install expo-dev-client
```

3) Create your first dev build with EAS (baseline)

```bash
cd mobile
npm install -g eas-cli@latest
eas login

# Android dev build (works on macOS/Windows/Linux)
eas build --profile development --platform android

# iOS Simulator dev build (macOS only)
eas build --profile development-simulator --platform ios
```

Install the build when prompted at the end of `eas build`, or install later with:

```bash
cd mobile
eas build:run -p android --latest
eas build:run -p ios --latest
```

Note: `eas build:run -p ios` only works for iOS Simulator builds (use the `development-simulator` profile).

4) Start Metro and run the dev client

```bash
cd mobile
npx expo start --dev-client
```

5) Day-to-day local builds (recommended after the baseline works)

```bash
cd mobile

# Android
npx expo run:android

# iOS (macOS only)
npx expo run:ios
```

## Notes

- Do not run `npm install` at the repo root.
- Do not commit generated native folders (`mobile/ios/`, `mobile/android/`) or build artifacts (`*.apk`, `*.ipa`, etc.).
- Local `expo run:*` uses prebuild to generate `mobile/ios/` and `mobile/android/`. Treat those folders as generated output and avoid hand-editing them.
- When builds fail (SDK/Gradle/CocoaPods/native deps), copy the full error into your AI code assistant and iterate on the smallest fix.

## `mobile/eas.json` profiles (quick reference)

- `development`: dev client build for Android (and iOS devices on macOS).
- `development-simulator`: dev client build specifically for iOS Simulator (macOS only).

Key settings to recognize:
- `developmentClient: true` means the build can connect to Metro.
- `credentialsSource: "remote"` means EAS manages signing credentials in the cloud.
- Android `buildType: "apk"` is easy to install on an emulator/device.
- iOS `simulator: true/false` must match where you are installing (Simulator vs device).

## Docs (when you get stuck)

- WEBD 430 Week 3 lectures (in the LMS)
- Expo environment setup: https://docs.expo.dev/get-started/set-up-your-environment/
- Expo dev builds: https://docs.expo.dev/develop/development-builds/use-development-builds/
- Expo local builds (`expo run:*`): https://docs.expo.dev/more/expo-cli/

## If You Overwrite `mobile/eas.json` (copy/paste template)

If you accidentally overwrite or delete `mobile/eas.json`, recreate it with this content:

```json
{
  "cli": {
    "appVersionSource": "local",
    "promptToConfigurePushNotifications": false
  },
  "build": {
    "development": {
      "distribution": "internal",
      "developmentClient": true,
      "credentialsSource": "remote",
      "android": {
        "buildType": "apk"
      },
      "ios": {
        "simulator": false
      }
    },
    "development-simulator": {
      "distribution": "internal",
      "developmentClient": true,
      "credentialsSource": "remote",
      "ios": {
        "simulator": true
      }
    },
    "preview": {
      "distribution": "internal",
      "channel": "preview",
      "credentialsSource": "remote"
    },
    "production": {
      "autoIncrement": true,
      "channel": "production",
      "credentialsSource": "remote",
      "ios": {
        "simulator": false
      }
    }
  },
  "submit": {
    "production": {}
  }
}
```
