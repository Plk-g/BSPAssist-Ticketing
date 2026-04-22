# BSPAssist — Mobile Ticketing App

A Flutter mobile app for submitting and tracking service/support tickets, backed by Firebase Authentication. Built as a fullstack mobile project with role-based navigation, session persistence, and offline-aware state handling.

---

## Features

- **Role-based views** — separate dashboards for Users, Admins, and Support Agents
- **Firebase Auth** — email/password login and registration with real-time session management
- **Session persistence** — login state stored via `SharedPreferences` so users don't re-authenticate on relaunch
- **Ticket lifecycle** — create, track, and close tickets with expandable list UI
- **Splash screen + routing** — app checks auth state on launch and routes accordingly
- **Profile screen** — editable user profile accessible from the nav drawer

---

## Tech Stack

| Layer | Tools |
|---|---|
| Framework | Flutter / Dart 3.x |
| Auth & Backend | Firebase Authentication, Firebase Core |
| Local Persistence | SharedPreferences |
| Testing | flutter_test, Mockito |
| Linting | flutter_lints |

---

## Project Structure

```
lib/
├── components/        # Reusable widgets (drawer, list tile, text box, ticket card)
├── pages/
│   ├── Dashboard/     # Admin, User, and main dashboard views
│   ├── profile/       # Profile screen
│   ├── login_page.dart
│   ├── register.dart
│   └── splash_screen.dart
├── firebase_options.dart
└── main.dart          # Entry point — auth check + route initialization
```

---

## Getting Started

**Prerequisites:** Flutter SDK ≥ 3.0.6, a Firebase project with Authentication enabled.

```bash
# Clone the repo
git clone https://github.com/Plk-g/BSPAssist-Ticketing.git
cd BSPAssist-Ticketing

# Install dependencies
flutter pub get

# Run on a connected device or emulator
flutter run
```

> **Note:** You'll need your own `google-services.json` (Android) and `GoogleService-Info.plist` (iOS) from your Firebase project. The files in this repo are placeholders.

---

## Running Tests

```bash
flutter analyze   # Static analysis
flutter test      # Unit + widget tests
```

---

## Roadmap

- [ ] Firestore integration for real-time ticket updates
- [ ] Push notifications for ticket status changes
- [ ] Admin analytics dashboard
- [ ] SLA timers and escalation rules
- [ ] Multi-language support (EN + HI)

---

## Author

**Palak Gupta**  
[GitHub](https://github.com/Plk-g)

---

## License

MIT License — see [LICENSE](LICENSE) for details.
