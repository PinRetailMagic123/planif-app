# Planif – publication iOS / Android (Capacitor)

## Préparation (une fois)
- Installer Node.js (https://nodejs.org)
- Android : Android Studio. iOS : un Mac avec Xcode.
- Dans ce dossier : `npm install`

## Modifier l'app
Éditer `www/index.html`, puis : `npx cap sync`

## Android (Google Play)
1. `npx cap open android` (ouvre Android Studio)
2. Build > Generate Signed App Bundle (.aab) → créer une clé (à conserver !)
3. Publier le .aab sur https://play.google.com/console (compte 25 $, une fois)

## iOS (App Store)
1. Sur Mac : `npx cap open ios` (ouvre Xcode)
2. Signing & Capabilities → choisir votre Team (compte Apple Developer, 99 $/an)
3. Product > Archive → Distribute App → App Store Connect
4. Finaliser sur https://appstoreconnect.apple.com

## À adapter
- Identifiant de l'app : `appId` dans `capacitor.config.json` (ex. ch.votrenom.planif), avant le premier envoi.
- Icône : remplacer `assets/icon.png` (1024×1024) puis `npx capacitor-assets generate`.
- Version : `versionCode`/`versionName` dans `android/app/build.gradle`, et dans Xcode pour iOS.
