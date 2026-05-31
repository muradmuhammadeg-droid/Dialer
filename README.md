# Dialer 📞

A modern, feature-rich Android Dialer application built with Jetpack Compose. This project demonstrates advanced Android development practices, including custom In-Call services, biometric-ready authentication, and interactive UI components.

## ✨ Features

- **Custom Dialer UI**: A clean, intuitive numeric keypad for making calls.
- **Contact Management**: Integrated contact list with search and detailed contact views.
- **Advanced In-Call Screen**: 
    - Real-time call state management (Incoming, Outgoing, Active, Ended).
    - Mute, Speaker, and Keypad controls.
    - **Animated Emojis**: Send interactive Lottie-based emojis during active calls.
- **Dual Authentication**:
    - **Sign in with Google**: Uses the latest Android Credential Manager API.
    - **Sign in with GitHub**: Full OAuth2 implementation with profile fetching.
- **Modern Tech Stack**: 100% Kotlin and Jetpack Compose (Material 3).

## 🛠 Technologies Used

- **Language**: Kotlin
- **UI Framework**: Jetpack Compose (Material 3)
- **Image Loading**: Coil
- **Animations**: Lottie for Android
- **Camera**: CameraX (for future video call integration)
- **Identity**: Android Credential Manager & Google ID library
- **Networking**: HttpURLConnection & Coroutines

## 🚀 Getting Started

### Prerequisites

- Android Studio Ladybug or newer.
- Android SDK 36 (target).
- A Google Cloud Project for Sign-in with Google.
- A GitHub OAuth App for Sign-in with GitHub.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/muradmuhammadeg-droid/Dialer
   ```
2. Open the project in Android Studio.
3. Sync Project with Gradle Files.

### Configuration

#### Google Sign-In
Replace the `serverClientId` in `MainActivity.kt` with your Web Client ID from the [Google Cloud Console](https://console.cloud.google.com/):
```kotlin
val googleIdOption = remember {
    GetGoogleIdOption.Builder()
        .setServerClientId("YOUR_CLIENT_ID.apps.googleusercontent.com")
        .build()
}
```

#### GitHub Sign-In
Replace the placeholders in `MainActivity.kt` with your credentials from [GitHub Developer Settings](https://github.com/settings/developers):
```kotlin
val githubClientId = "YOUR_GITHUB_CLIENT_ID"
val githubClientSecret = "YOUR_GITHUB_CLIENT_SECRET"
```
Ensure your **Authorization callback URL** is set to `dialer://github-auth`.

## 📱 Permissions

The app requires the following permissions to function as a dialer:
- `CALL_PHONE`: To initiate calls.
- `READ_CONTACTS`: To display your contact list.
- `READ_PHONE_STATE`: To monitor call status.
- `CAMERA`: For video call features.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

Copyright (C) 2026 Murad Muhammad
Licensed under the Apache License, Version 2.0.
