<div align="center">

<img width="625" height="399" alt="Gemini_Generated_Image_ri752vri752vri755-removebg-preview" src="https://github.com/user-attachments/assets/abd58387-1663-41f9-9bb5-1b1019036ad2" />

# 📱 NSBM ATTEND

### Smart QR Attendance for NSBM Green University

[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/)
[![Built With](https://img.shields.io/badge/Built%20With-Ionic%20React-3880FF?style=for-the-badge&logo=ionic&logoColor=white)](https://ionicframework.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Capacitor](https://img.shields.io/badge/Capacitor-8.0-119EFF?style=for-the-badge&logo=capacitor&logoColor=white)](https://capacitorjs.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**NSBM ATTEND** is a mobile application that simplifies lecture attendance marking at NSBM Green University. Scan the QR code, and the app does the rest — auto-login, attendance marking, and lecture detail extraction, all in a single tap.

[Download APK](#-download) • [Features](#-features) • [How It Works](#-how-it-works) • [Tech Stack](#-tech-stack)

</div>

---

<div align="center">

## 📸 Screenshots

| Home Dashboard | QR Scanner | Settings |
|:-:|:-:|:-:|
| <img src="img_source/home_dashboard.png" width="220"> | <img src="img_source/qr_sanner.png" width="220"> | <img src="img_source/settings.png" width="220"> |

| Onboarding | Welcome | Credits |
|:-:|:-:|:-:|
| <img src="img_source/onboarding.png" width="220"> | <img src="img_source/welome_img1.png" width="220"> | <img src="img_source/credits.png" width="220"> |

| Welcome |
|:-:|
| <img src="img_source/welcome_img2.png" width="220"> |

</div>

---

## ✨ Features

### 🔍 Smart QR Scanning
- Real-time camera QR scanning powered by **Google ML Kit**
- Flashlight toggle for low-light environments
- Pinch-to-zoom functionality for distant QR codes
- Instant scan feedback with haptic response

### 🔐 One-Tap Auto Login
- Save your NSBM credentials securely on your device
- Auto-fills username & password on the university portal
- Seamless login → attendance marking flow — no manual typing needed

### 📋 Lecture Detail Extraction
- Automatically extracts lecture information after attendance is marked
- Displays **Module Name**, **Date**, and **Time** in Recent Activity
- Replaces raw URLs with readable lecture cards

### 🛡️ University Domain Lock
- Only accepts QR codes from the official `nsbm.ac.lk` domain
- Blocks non-university and malicious QR codes with a warning alert
- Protects against phishing and unauthorized URL redirection

### 🌓 Dark & Light Mode
- Beautiful theme toggle with smooth transitions
- Respects system-level dark mode preference on first launch
- Persistent theme preference across sessions

### 👤 User Profiles
- Customizable display name and profile photo
- Camera or gallery photo selection
- Personalized greeting on the home dashboard

### 📊 Attendance Tracking
- Running count of total successful QR attendance scans
- Recent Activity feed with the last 5 scans
- Swipe-to-delete individual scan records
- Clear all history option

### 🚀 First-Time User Onboarding
- Guided setup wizard for new users
- Step-by-step credential and profile configuration
- Skip option for returning users

---

## 🔄 How It Works

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│   📷 Scan QR Code                                       │
│       │                                                 │
│       ▼                                                 │
│   🔒 Domain Check (nsbm.ac.lk?)                         │
│       │                                                 │
│       ├── ❌ Non-NSBM → Alert & Block                    │
│       │                                                 │
│       └── ✅ Valid → Open University Portal               │
│               │                                         │
│               ▼                                         │
│           🔑 Auto-fill Credentials                       │
│               │                                         │
│               ▼                                         │
│           ✅ Attendance Marked                            │
│               │                                         │
│               ▼                                         │
│           📋 Extract Lecture Details                      │
│           (Module, Date, Time)                          │
│               │                                         │
│               ▼                                         │
│           💾 Save to Recent Activity                     │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

<div align="center">

| Category | Technology | Purpose |
|:--------:|:----------:|:-------:|
| **Framework** | ![Ionic](https://img.shields.io/badge/Ionic_React-3880FF?style=flat-square&logo=ionic&logoColor=white) | Cross-platform UI framework |
| **Frontend** | ![React](https://img.shields.io/badge/React_19-61DAFB?style=flat-square&logo=react&logoColor=black) | Component-based UI library |
| **Language** | ![TypeScript](https://img.shields.io/badge/TypeScript_5.9-3178C6?style=flat-square&logo=typescript&logoColor=white) | Type-safe JavaScript |
| **Build Tool** | ![Vite](https://img.shields.io/badge/Vite_5-646CFF?style=flat-square&logo=vite&logoColor=white) | Fast build & HMR |
| **Native Runtime** | ![Capacitor](https://img.shields.io/badge/Capacitor_8-119EFF?style=flat-square&logo=capacitor&logoColor=white) | Native bridge & plugins |
| **QR Scanner** | ![ML Kit](https://img.shields.io/badge/Google_ML_Kit-4285F4?style=flat-square&logo=google&logoColor=white) | Barcode detection |
| **Browser** | ![Cordova](https://img.shields.io/badge/InAppBrowser-E8E8E8?style=flat-square&logo=apache-cordova&logoColor=black) | In-app web views |
| **Storage** | ![Capacitor](https://img.shields.io/badge/Preferences_API-119EFF?style=flat-square&logo=capacitor&logoColor=white) | Local data persistence |
| **Platform** | ![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white) | Target platform |

</div>

### Architecture Overview

```
┌──────────────────────────────────────────────────────┐
│                    NSBM ATTEND                       │
├──────────────────────────────────────────────────────┤
│                                                      │
│  ┌─────────────┐  ┌─────────────┐  ┌──────────────┐ │
│  │   Home      │  │  Settings   │  │  Components  │ │
│  │  Dashboard  │  │   Page      │  │  (Modals)    │ │
│  │  + Scanner  │  │  + Profile  │  │  + Onboard   │ │
│  │  + History  │  │  + Creds    │  │  + Credits   │ │
│  │  + Theme    │  │  + Password │  │  + Splash    │ │
│  └──────┬──────┘  └──────┬──────┘  └──────┬───────┘ │
│         │                │                │          │
│  ┌──────┴────────────────┴────────────────┴───────┐  │
│  │              Storage Service                   │  │
│  │   Credentials │ Profile │ Theme │ Scan History │  │
│  └────────────────────────┬───────────────────────┘  │
│                           │                          │
├───────────────────────────┼──────────────────────────┤
│                    Native Layer                      │
│  ┌──────────┐ ┌──────────┐ ┌────────┐ ┌──────────┐  │
│  │ ML Kit   │ │ InApp    │ │Camera  │ │Preferences│ │
│  │ Scanner  │ │ Browser  │ │Plugin  │ │  API     │  │
│  └──────────┘ └──────────┘ └────────┘ └──────────┘  │
└──────────────────────────────────────────────────────┘
```

---

## 🔒 Security

| Security Aspect | Details |
|----------------|---------|
| **Credential Storage** | Stored locally on-device via Android SharedPreferences (per-app sandbox) |
| **No Cloud Storage** | Credentials never leave the device — no server-side storage |
| **APK Safety** | Credentials are NOT bundled in APK — each device has isolated storage |
| **Domain Validation** | Only `nsbm.ac.lk` URLs are processed — all other domains are blocked |
| **Session Handling** | University portal manages sessions via server-side PHP cookies |

---

## 📥 Download

<!-- Add your APK download link here -->
> **Latest Release**: Check the [Releases](https://github.com/RadinReanula/NSBM-Attend/releases) section for the latest signed APK.

### Installation

1. Download the `.apk` file from [Releases](https://github.com/RadinReanula/NSBM-Attend/releases)
2. Enable **Install from Unknown Sources** on your Android device
3. Open the downloaded file and tap **Install**
4. Launch **NSBM ATTEND** and follow the onboarding setup

### Requirements

- Android 7.0 (API 24) or higher
- Camera access for QR scanning
- Active internet connection for university portal access

---

## 📁 Project Structure

```
NSBM ATTEND
├── src/
│   ├── components/
│   │   ├── CreditsModal         # App credits & team info
│   │   ├── OnboardingModal      # First-time user setup wizard
│   │   └── SplashOverlay        # Branded splash screen
│   ├── pages/
│   │   ├── Home                 # Dashboard, scanner, & history
│   │   └── Settings             # Profile & credentials management
│   ├── services/
│   │   └── storage.ts           # Local storage operations
│   ├── theme/                   # Ionic CSS variables
│   └── App.tsx                  # Root component & routing
├── android/                     # Native Android project
└── capacitor.config.ts          # Capacitor configuration
```

---

## 👨‍💻 Developer

<div align="center">

**Radin Reanula**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/radinreanula/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RadinReanula)

</div>

### Beta Testers & QA

- **Poojana Fernando** — [LinkedIn](https://www.linkedin.com/in/poojana-fernando/)
- **Chamindu Rathnayake** — [LinkedIn](https://www.linkedin.com/in/chamidu-rathnayake-0b89702b8/)
- **Vinuka Jayavihan** — [LinkedIn](https://www.linkedin.com/in/vinuka-jayavijan-b8b49833a/)

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Made with ❤️ for NSBM Green University**

*⚠️ This repository contains the showcase documentation only. Source code is private.*

</div>
