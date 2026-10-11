# FakhriTok

Flutter Android short-video app starter with:
- Full-screen vertical video feed
- Demo network videos
- Local video picker and playback
- Local likes, saved videos, follows, comments, and username preferences
- Discover search (demo accounts)
- Arabic RTL interface
- Share action

## Important scope
This workspace is a functional local prototype, not a full public TikTok-scale service. User uploads remain on the device; likes, comments, saved items, and follows are local. Authentication, real cross-user feeds, cloud uploads, DMs, push notifications, moderation, recommendation infrastructure, and a production backend require configuration and deployment.

## Requirements
- Flutter stable SDK compatible with Dart >=3.3
- Android SDK / build environment
- Internet for demo network video

## Run
```bash
flutter pub get
flutter run
```

## Build APK
```bash
flutter build apk --release
```
Expected output:
`build/app/outputs/flutter-apk/app-release.apk`

## Android permissions
`image_picker` uses Android's system media picker. For older Android versions or custom storage flows, check plugin documentation and Android configuration.

## Firebase integration
Firebase dependencies are included but not initialized in this starter. To enable real multi-user accounts and cloud uploads:
1. Create a Firebase project.
2. Configure Android app package `com.fakhri.football` (change package ID to `com.fakhri.fakhritok` if desired and keep it consistent).
3. Run FlutterFire CLI configuration to generate `firebase_options.dart`.
4. Initialize Firebase in `main.dart` using `DefaultFirebaseOptions.currentPlatform`.
5. Implement authentication, Firestore repositories, Storage uploads, security rules, moderation, and notifications.
6. Never publish permissive Firestore/Storage rules or service account keys.

## Demo content
The demo video URLs are public Flutter documentation sample media and are not football clips. Replace them only with media you have permission to use.
