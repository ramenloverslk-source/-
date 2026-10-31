# Shan Astrology — Sinhala Android App

Flutter starter project for a Sinhala horoscope and compatibility app.

## Current MVP features
- Sinhala UI
- Two-person birth detail form
- Manual selection of birth star (Nakshatra) and Moon sign (Rashi)
- Starter Ashtakoota (36-point) and 20-porondam comparison screens

## Important calculation limitation
This is an **MVP / prototype**, not a certified astrology calculator. Birth date, time and place are collected but the app does not yet calculate the ascendant, Moon longitude, nakshatra or planetary positions from an ephemeris. The user currently selects nakshatra and rashi manually.

The compatibility formulas and mappings in `lib/main.dart` are starter approximations. In particular, the Sinhala 20-porondam tradition can vary by regional lineage and practitioner. Before publishing for real use, have the exact rules, star mappings, scoring and exceptions reviewed by a qualified Sri Lankan astrologer. Do not use this prototype's score as the sole basis for a marriage decision.

## Requirements
- Flutter SDK (stable)
- Android Studio or VS Code
- Android SDK

## Run locally
```bash
flutter doctor
flutter pub get
flutter run
```

## Build an Android APK
```bash
flutter build apk --release
```
APK output:
`build/app/outputs/flutter-apk/app-release.apk`

## Create the full Android project
This source bundle contains the app code and configuration. Generate Flutter's standard Android wrapper files with:
```bash
flutter create --platforms=android --org lk.shan shan_astrology
```
Then copy this bundle's `lib/main.dart`, `pubspec.yaml`, and `README.md` into the generated `shan_astrology` folder (replace existing files), and run the commands above.

## Publish on GitHub
1. Create a new empty repository named `shan-astrology` on GitHub.
2. Open a terminal inside the `shan_astrology` project folder.
3. Run:
```bash
git init
git add .
git commit -m "Initial Shan Astrology app"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/shan-astrology.git
git push -u origin main
```
Replace `YOUR-USERNAME` with your GitHub username.

## Next development milestones
1. Add a reliable ephemeris library/service to calculate planetary longitudes using the selected ayanamsa and timezone.
2. Convert birth date/time/place to Moon sign and nakshatra automatically.
3. Validate all 20 porondam and Ashtakoota rules with a domain expert.
4. Add chart display, PDF export, saved profiles, and privacy controls.
