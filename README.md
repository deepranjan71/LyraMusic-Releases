# Lyra Music — Production Release Distribution Hub

Welcome to the official public distribution repository for **Lyra Music**, a high-performance, ad-free Android audio streaming application built on Jetpack Compose, ExoPlayer, and Material 3 design principles.
---

## Technical Specifications (v4.0.0)

| Specification | Details |
| :--- | :--- |
| **Version Name** | `v4.0.0` |
| **Version Code** | `400` |
| **Package Identifier** | `com.deep.musicplayer` |
| **Target Architecture** | ARM64-v8a / x86_64 |
| **Minimum SDK** | Android 8.0 (API 26) / Target Android 15 (API 35) |
| **Binary Optimization** | R8 / ProGuard Minified (5.8 MB) |
| **Signing Certificate** | V1 & V2 SHA-256 Verified Release Key |

---

## Release Notes — Version 4.0.0

### Executive Summary
Version 4.0.0 introduces direct In-App Software Updates & Package Installation, instant 0ms cold startup via persistent disk caching, a 120 FPS high-performance image caching pipeline, a smooth pull-to-refresh & header refresh action, playable Listening Recap, dynamic Light Mode color extraction, fluid spring player physics, and a modern straight-line progress bar.

---

### Key Architectural & Feature Enhancements

#### 1. In-App Direct Software Update & Installer
- **Direct Download & Auto-Install**: Stream APK updates directly inside the app with real-time percentage progress indicators, then auto-trigger package installation without opening external browser links.
- **Material 3 Update Interface**: Clean full-page update experience displaying current version, build number, check timestamps, formatted release notes, and action buttons.

#### 2. Instant Cold Startup & Disk Persistence (`HomeCache`)
- **0 ms Delay**: Restores the complete home feed (shelves, speed dial, trending tracks, and genre chips) directly from local disk storage on app launch for instant rendering.

#### 3. 120 FPS Smooth Image Caching Pipeline
- **Lag-Free Scrolling**: Custom in-memory (25% RAM) and disk caches in Coil ensure zero thumbnail flickering and smooth horizontal scrolling.

#### 4. Home Page Refresh & Smooth Pull-to-Refresh
- **Spinning Refresh Action**: Dedicated refresh button in the top header row next to Settings, and smooth pull-to-refresh gesture support.

#### 5. Playable Listening Recap & Scoped Genre Content
- **1-Tap Playable Recap**: Tap any top track from your weekly or monthly Listening Recap to start playing it instantly.
- **Focused Genre Feeds**: Speed Dial and Popular Artists are conditionally scoped exclusively to the "All" genre tab to keep genre channels clean.

#### 6. Refined Player UI & Fluid Spring Physics
- **Modern Progress Bar**: Replaced squiggly line with a clean, modern straight-line progress bar.
- **Fluid Spring Sheet Motion**: Re-tuned player sheet physics to a soft 260f stiffness spring with smooth color morphing.
- **Minimalist Header Controls**: Removed circular ring highlights around Cast and collapse buttons.

---

## Installation Guide

1. Download **[Lyra-v4.0.0-release.apk](https://github.com/deepranjan71/LyraMusic-Releases/releases/download/v4.0.0/Lyra-v4.0.0-release.apk)** *(5.8 MB)*.
2. Open the downloaded `.apk` file on your Android device.
3. Grant permission for **"Install from unknown sources"** if prompted by your package installer.
4. Complete installation and launch the application.

---

## Security & Verification

All release binaries published in this repository are compiled directly from source and cryptographically signed with the official release key (`lyra-release-key.jks`).

---

## Legal Disclaimer

*Lyra Music is an open-source, non-commercial media application designed strictly for personal and educational use. Lyra Music does not host, store, or distribute copyrighted audio files. All media streams, metadata, and trademarks belong to their respective copyright holders and public content providers.*
