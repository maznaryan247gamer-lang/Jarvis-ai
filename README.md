# JARVIS AI — Android Foundation v1.0

A phone-first Android app foundation with a Tony Stark-inspired blue HUD interface.

## Current features
- Native Android app using Kotlin and Jetpack Compose
- Home dashboard with a custom JARVIS-style orb
- Chat interface (local demo responses only)
- System diagnostics screen
- GitHub Actions cloud build for a debug APK

## Not connected yet
Gemma, Gemini, Groq, speech recognition, wake word, screen understanding, phone automation and multi-agent workflows are future stages. The current chat does not call an AI service.

## Build from your phone using GitHub
1. Download and extract this ZIP on your Android phone.
2. Open https://github.com in Chrome and sign in or create an account.
3. Create a new repository named `JARVIS-AI`. Choose **Public** or **Private**; either works for this workflow.
4. In the repository, choose **Add file → Upload files**.
5. Upload the *contents* of this project folder, preserving the folder structure. Make sure `.github/workflows/build.yml` is included. If the GitHub mobile page hides dot-folders, use Chrome's **Desktop site** option.
6. Commit the uploaded files to the `main` branch.
7. Open the repository's **Actions** tab. Select **Build JARVIS AI APK**.
8. If prompted, enable GitHub Actions for the repository.
9. Wait for the workflow to finish with a green check mark.
10. Open the completed workflow run, scroll to **Artifacts**, and download `JARVIS-AI-debug-APK`.
11. Extract the downloaded artifact ZIP. Inside it is `app-debug.apk`.
12. Tap the APK to install it. Android may ask you to allow installation from that browser or file manager. Only allow the installer you deliberately used, then turn that permission off again afterwards if you prefer.

## Build configuration
- Application ID: `com.jarvis.ai`
- Minimum Android: API 26 (Android 8.0)
- Compile / target SDK: 35
- Java: 17
- Android Gradle Plugin: 8.9.2
- Gradle: 8.11.1
- Kotlin: 2.0.21

## Important
The workflow creates a **debug APK** for testing. It is not a Play Store release. A later release build should use a securely stored signing key and GitHub Actions secrets. Never put API keys or signing passwords in source files.
