# Lyra Music — Production Release Distribution Hub

Welcome to the official public distribution repository for **Lyra Music**, a high-performance, ad-free Android audio streaming application built on Jetpack Compose, ExoPlayer, and Material 3 design principles.


## Technical Specifications (v3.8.0)

| Specification | Details |
| :--- | :--- |
| **Version Name** | `v3.8.0` |
| **Version Code** | `380` |
| **Package Identifier** | `com.deep.musicplayer` |
| **Target Architecture** | ARM64-v8a / x86_64 |
| **Minimum SDK** | Android 8.0 (API 26) / Target Android 15 (API 35) |
| **Binary Optimization** | R8 / ProGuard Minified (12.9 MB) |
| **Signing Certificate** | V1 & V2 SHA-256 Verified Release Key |

---

## Release Notes — Version 3.8.0

### Executive Summary
Version 3.8.0 introduces core improvements across gesture responsiveness, display efficiency, application security, and personalized recommendation layout engines. The application package size has been reduced by 80% via R8 bytecode optimization while implementing hardware-backed security protocols.

---

### Core System & Architectural Enhancements

#### 1. Real-Time Gesture Tracking Pipeline
- **Zero-Latency Queue Gesture Engine**: Replaced standard modal sheet containers with a 120 FPS GPU-composited overlay (`graphicsLayer`). Provides 1:1 finger tracking with sub-millisecond response time and partial-drag state locking.
- **Full-Screen Dismissal Mechanics**: Normalized drag-down dismissal mechanics across the full display height (`coerceIn(0f, screenHeightPx)`), preventing layout snapping and premature close thresholds.

#### 2. Display & Power Optimization
- **Pure AMOLED Dark Mode**: Integrated true `#000000` pitch-black OLED background theme option in Settings to reduce power consumption on AMOLED displays.
- **Off-Thread Bitmap Pipeline**: Standardized thumbnail processing to 500x500px resolution with off-main-thread decoding via Coil worker pools, eliminating main-thread layout recalculations.

#### 3. Personalization & Content Delivery
- **Personalized 3-Row Home Feed**: Replaced generic trending lists with three personalized feeds:
  1. *Suggested Songs*: High-resolution 1:1 square artwork cards.
  2. *Listening-Based Playlists*: Tailored playlists based on historical listening preferences.
  3. *Recommended Related Artists*: Circular artist profiles derived from top played artists.
- **Strict Regional Filtering**: Applied language and regional regex constraints across genre filters (e.g., *USA Pop* excludes non-English/non-Western streams; *Bollywood* excludes Western hits).
- **3x3 Speed Dial Grid**: Rebuilt Speed Dial into a 3-column x 3-row grid featuring an integrated, non-floating *Lucky Play* randomization tile.

#### 4. Security & Hardening Protocols
- **R8 Bytecode Minification**: Enabled R8 code obfuscation and resource shrinking to protect intellectual property and minimize APK footprint.
- **Network & Backup Hardening**: Disabled plain-text HTTP traffic (`usesCleartextTraffic="false"`) and ADB backup extraction (`allowBackup="false"`).
- **Runtime Integrity Audit**: Integrated `SecurityManager` runtime checks for attached debuggers, root binaries (`su`), and release certificate SHA-256 signature verification.

#### 5. User Interface & Audio FX
- **Multi-Page Settings Navigation**: Restructured Settings into a multi-page hub with sub-page routing and animated `FastOutSlowInEasing` transitions.
- **5-Band Equalizer & Virtualizer**: Integrated 5-band frequency controls (-15 dB to +15 dB), acoustic presets, Bass Boost, 3D Surround, and AutoEq profile loading.
- **In-App Auto-Update System**: Automated background release check querying the official GitHub distribution endpoint with direct 1-tap APK update prompts.

---

## Installation Guide

1. Download **[Lyra-v3.8.0-release.apk](https://github.com/deepranjan71/LyraMusic-Releases/releases/download/v3.8.0/Lyra-v3.8.0-release.apk)** *(12.9 MB)*.
2. Open the downloaded `.apk` file on your Android device.
3. Grant permission for **"Install from unknown sources"** if prompted by your package installer.
4. Complete installation and launch the application.

---

## Security & Verification

All release binaries published in this repository are compiled directly from source and cryptographically signed with the official release key (`lyra-release-key.jks`).

---

## Legal Disclaimer

*Lyra Music is an open-source, non-commercial media application designed strictly for personal and educational use. Lyra Music does not host, store, or distribute copyrighted audio files. All media streams, metadata, and trademarks belong to their respective copyright holders and public content providers.*
