# Street Racer 3D — Android project

This is a starter Android project for a mobile 3D racing game. It contains a Three.js WebGL game wrapped in a native Android WebView and a GitHub Actions workflow to compile a debug APK.

## Features in this prototype
- Real-time 3D scene rendered with Three.js/WebGL
- Procedurally modeled sports cars and traffic
- An original illustrated driver portrait and a simple visible driver model in the player's car
- Three selectable environments: city streets, mountain pass, neon night
- Touch steering, nitro, collision/restart loop, score and speed HUD
- Landscape immersive Android shell

## Important limitations
- **This ZIP is source code, not a compiled APK.** An Android SDK/build environment is required to produce an installable APK.
- The Three.js module is loaded from jsDelivr, so the current prototype requires internet access when the game starts.
- Cars are original procedural approximations, not licensed manufacturer CAD models or photorealistic scanned assets. Driver is an original illustrated/game-style character, not a real person.
- The game is a prototype, not a finished commercial-grade racing simulator. Audio, lap timing, AI opponents, garage/upgrades, save data, and rigorous device testing remain to be built.

## Build the APK
### Android Studio
1. Install Android Studio with Android SDK Platform 35 and JDK 17.
2. Open this folder as an existing Gradle project.
3. Sync Gradle, then select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. The debug APK is generated at `app/build/outputs/apk/debug/app-debug.apk`.

### Build in GitHub Actions (no local Android SDK required)
1. Create a GitHub repository and upload the contents of this folder.
2. Push to the `main` branch, or go to **Actions > Build Android APK > Run workflow**.
3. When the workflow finishes, open its run and download the `StreetRacer3D-debug-apk` artifact.
4. Extract the artifact and install `app-debug.apk` on Android. You may need to allow installation from your browser/file manager.

## Play in a browser
Open `app/src/main/assets/index.html` in a modern browser with internet access. The Three.js module requires CDN access.
