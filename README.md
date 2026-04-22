# BSPAssist 🎫

> **Mobile-first service ticketing — built for teams that don't sit at desks.**

A Flutter app for filing, triaging, and tracking support tickets from your phone. Role-based access control, Firebase-backed auth, and session persistence that survives app restarts — so users are never re-authenticating mid-shift.

---

## Why BSPAssist? 🤔

Most ticketing tools are web-only and assume a desk. BSPAssist is designed for mobile-first environments where tickets need to be raised, assigned, and resolved on the go — with the app smart enough to stay authenticated between sessions and route each user to exactly the right view based on their role.

---

## How the Auth Flow Works 🔐

The auth check is the backbone of the app. On cold start, the app reads a persisted token from `SharedPreferences` *before* Firebase initializes — skipping the login screen entirely for returning users. Sign-out clears the token and hard-redirects; the route table never exposes the dashboard to an unauthenticated state.

```
main() → checkIfLoggedIn()
           ├── token found  → /dashboard
           └── no token     → / (SplashScreen → Login)
```

Role-based views are handled through isolated dashboard components — `DashboardPage`, `UserDashboard`, and `AdminDashboard` — keeping privilege-specific logic cleanly separated rather than conditionally crammed into one bloated screen.

---

## Tech Stack 🛠️

| Layer | Choice | Why |
|---|---|---|
| 📱 Framework | Flutter / Dart 3.x | Single codebase for Android + iOS |
| 🔑 Auth | Firebase Authentication | Managed identity, email/password, extensible to OAuth |
| 💾 Persistence | SharedPreferences | Lightweight session token storage — no DB overhead for auth state |
| 🧪 Testing | flutter_test + Mockito | Widget tests + mock-based unit testing |

---

## Project Structure 📁

```
lib/
├── components/        # Drawer, list tiles, ticket card, reusable inputs
├── pages/
│   ├── Dashboard/     # Role-split views: User, Admin, main dashboard
│   ├── profile/       # Editable user profile
│   ├── login_page.dart
│   ├── register.dart
│   └── splash_screen.dart
├── firebase_options.dart
└── main.dart          # Auth check → route resolution on cold start
```

---

## Getting Started 🚀

Requires Flutter ≥ 3.0.6 and a Firebase project with Authentication enabled.

```bash
git clone https://github.com/Plk-g/BSPAssist-Ticketing.git
cd BSPAssist-Ticketing
flutter pub get
flutter run
```

> 🔧 Drop your own `google-services.json` (Android) and `GoogleService-Info.plist` (iOS) into the appropriate directories — the ones in this repo are project-specific and won't work out of the box.

---

## Testing ✅

```bash
flutter analyze   # Static analysis
flutter test      # Widget + unit tests
```

---

## What's Next 🗺️

- [ ] 🔄 Firestore integration for live ticket sync across devices
- [ ] 🔔 Push notifications on ticket status transitions
- [ ] ⏱️ SLA timers with escalation rules
- [ ] 📊 Admin analytics dashboard
- [ ] 🌐 Multi-language support (EN + HI)

---

## Author ✍️

**Palak** · MS CS @ NYU Tandon  
[GitHub](https://github.com/Plk-g)

---

*MIT License*
