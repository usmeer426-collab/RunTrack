# RunTrack — Android GPS workout tracker (starter project)

This is a starter Android Studio project for an English-language walking, jogging and running tracker.

## Included
- GPS-based distance and elapsed time
- Average pace estimate (min/km)
- Foreground location service with ongoing notification
- Pause/resume and finish/save
- Spoken kilometer split announcements using Android Text-to-Speech
- Recent workout history stored locally on the phone
- Conservative GPS filtering (accuracy >25 m and implausible speed jumps are ignored)

## Important limitations in this starter
- This starter stores workout summary and split text; it does not yet render a route map or save full route coordinates to a map screen. Coordinates are collected in memory during the workout. Add Google Maps SDK and persist route points to show/review maps.
- GPS distance can be inaccurate around tall buildings, trees, indoors, or with battery-saving restrictions. Test outdoors on a known route.
- This source project has not been compiled or tested on your particular phone. Build it in Android Studio and fix any SDK/Gradle compatibility prompts it shows.
- For a release/public app, review Android background-location policy, privacy disclosures, data deletion/export, and test across Android versions.
- Android 13+ may ask for notification permission. Allow location permission and enable Location on the phone.

## Build an APK
1. Install Android Studio from https://developer.android.com/studio
2. Extract this ZIP.
3. In Android Studio choose **Open** and select the extracted `RunTrackAndroid` folder (the folder containing `settings.gradle.kts`).
4. Let Gradle sync. Install a compatible JDK if Android Studio asks; JDK 17 is commonly used with Android Gradle Plugin 8.x.
5. If prompted, install Android SDK Platform 35 from SDK Manager.
6. Connect an Android phone with USB debugging enabled, or use an emulator. For GPS testing, a real phone outdoors is better.
7. Press **Run** to install and test.
8. To create an APK: **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
9. Android Studio shows a notification with **locate**. The debug APK is normally at `app/build/outputs/apk/debug/app-debug.apk`.
10. Transfer the APK to your phone and install it. Android may ask you to allow installation from that file manager. Only install APKs you built or trust.

## First outdoor test
- Open RunTrack outdoors, enable Location, and grant location permission.
- Tap Start workout and wait for GPS to settle.
- Walk a measured route of at least 500 m to 1 km.
- Compare distance against a trusted route or known measured track.
- Check that screen-off tracking works on your phone; disable battery optimization for the app if your device aggressively stops background activity.
