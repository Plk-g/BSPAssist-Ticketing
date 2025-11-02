```markdown
# BSPAssist — Ticket Raising & Management App 🎫

A Flutter-based mobile app for submitting, tracking, and managing service tickets.  
Built with clean architecture principles, offline support, and accessible UI design.

---

## ✨ Features
- 🧑‍💼 **User Roles:** Employee, Admin, and Support Agent views  
- 📨 **Ticket Lifecycle:** Create, assign, update, and close tickets in real time  
- 📶 **Offline-first:** Local cache with sync-on-reconnect functionality  
- 🔔 **Notifications:** Real-time status updates and reminders  
- 🎨 **Accessibility & Theming:** Dark mode, scalable text, and high-contrast colors  

---

## 🧱 Tech Stack
| Layer | Tools |
|-------|-------|
| Framework | Flutter (Dart 3.x) |
| Database | Firebase / REST API |
| Local Storage | Hive / Sqflite |
| State Mgmt | Riverpod / Provider |
| CI/CD | GitHub Actions |
| Version Control | Git & GitHub |

---

## 🗂️ Project Structure
```

lib/
core/               # constants, errors, routing, theming
data/               # models, data sources, repository impls
features/
auth/
tickets/
domain/
presentation/
application/
app.dart

````

---

## 🧪 Testing & CI
Run static analysis and tests locally:
```bash
flutter analyze
flutter test
````

GitHub Actions build & test automatically on each commit.

---

## 🧭 Roadmap

* [ ] Add analytics dashboard for Admins
* [ ] SLA timers and escalations
* [ ] Ticket comments & in-app chat
* [ ] Multi-language support (EN + HI)

---

## 📸 Screenshots (coming soon)

| Login                            | Create Ticket                      | Dashboard                                |
| -------------------------------- | ---------------------------------- | ---------------------------------------- |
| ![login](docs/screens/login.png) | ![create](docs/screens/create.png) | ![dashboard](docs/screens/dashboard.png) |

---

## 🧠 Learnings

* Implemented feature-based architecture for scalability
* Explored state management and offline-first design
* Strengthened clean code and documentation practices

---

## 👩‍💻 Author

**Palak Gupta**
MS CS @ NYU Tandon | Building accessible & intelligent tech
[LinkedIn](https://www.linkedin.com/in/palakg008) • [GitHub](https://github.com/Plk-g)

---

## 📜 License

MIT License — feel free to use and modify.
