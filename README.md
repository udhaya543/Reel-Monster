# Reel Monster
Android app (Kotlin, zero dependencies, no internet permission).

## Get the APK (no installs needed)
1. Create a new GitHub repo, upload this whole folder (keep the .github folder).
2. Open the Actions tab -> "Build APK" -> wait ~4 min.
3. Download the `ReelMonster-apk` artifact, unzip, send app-debug.apk to your phone.

## Or build locally
Open the folder in Android Studio (Hedgehog or newer) -> Run on a USB-connected phone,
or `gradle assembleDebug` -> app/build/outputs/apk/debug/app-debug.apk

## Install + enable
1. Tap the APK, allow "install unknown apps".
2. Open Reel Monster -> "Turn on the monster" -> Installed apps -> Reel Monster -> On.
   Android 13+: if greyed out, App info -> ⋮ -> Allow restricted settings, then retry.
3. Pick Level 1 or 2. Open Instagram / YouTube.

## Tuning Level 2
Reel detection lives in MonsterService.kt (findViewer / collect). Run
`adb logcat -s Monster` while swiping: each counted reel prints "new reel: ...".
