# UKM Student Hub

**One-line:** UKM Student Hub is a student-first mobile prototype that connects UKM students with a campus marketplace, peer finder, chat, course record and profile management — built as a focused alternative to social media for UKM campus life.

---
## 🎬 Demo
[Watch demo video on YouTube](https://youtu.be/rKbOmRUdYAo)  
[![UKM Student Hub Demo](https://img.youtube.com/vi/rKbOmRUdYAo/0.jpg)](https://youtu.be/rKbOmRUdYAo)
- If reviewers want to try it, I can upload an APK to GitHub Releases (prefers not to publish on Play Store without official support).

---
## Status (honest)
- **Type:** Prototype / solo project by Raslene Klai  
- **State:** Core app features implemented and working locally; **not deployed** due to lack of institutional integration/support.  
- **What’s finished:** sign in/out/registration, password reset, posting/updating/deleting marketplace items, in-app chat, peer finder, course record, profile management (personal info fields).  
- **What’s missing / blocked:** automatic matric/faculty integration with UKM systems (no access/support from faculty) — remaining features are WIP or polishing only.

---

## My role
- **Solo developer** — full stack mobile dev for this prototype (UI, client logic, Firebase integration, basic backend rules).
- I designed, implemented and tested the app alone using Android Studio + Kotlin and Firebase services.

---

## Tech stack
- **Client:** Android (Kotlin), Android Studio  
- **Backend / services:** Firebase (Auth, Firestore, Storage, Security Rules)  
- **Storage / DB:** Firestore for app data; Storage for images  
- **Build / release:** Android Studio (APK artifact)  
- **Notes:** `google-services.json` is required locally (do not commit to GitHub).

---

## Features — implemented (what actually works)
- **Authentication:** Email registration, login, sign out, password reset (Firebase Auth).  
- **Marketplace:** Create item (title, description, price, category, image), edit item, delete item, list/browse items.  
- **Chat:** Basic in-app chat between users (Firestore-backed).  
- **Peer Finder:** Search / find other students by declared fields (name, faculty, year, course).  
- **Course / Profile-recording:** Add/view course records and personal profile fields (name, contact, year, semester, faculty, country, birthday).  
- **Client-side validation & image upload** (simple compression and upload to Firebase Storage).

---

## Features — partial / WIP / blocked
- **Automatic matric number & faculty DB integration** — intended to auto-validate users against UKM records; blocked due to lack of access/support.  
- **Play Store / public release** — not published (no institutional approval/support).  
- **Analytics / metrics collection** — minimal; not instrumented for user analytics.  
- **Polish / UX improvements** — some screens need UI polish and error handling improvements.

---

## How to run (developer)
**Requirements**
- Android Studio (Arctic Fox or later recommended)
- JDK 11+ (Android Studio handles this)
- Firebase project (you must add `google-services.json`)

**Steps**
1. Clone the repo.
2. Create a Firebase project and enable Auth + Firestore + Storage.
3. Download `google-services.json` from your Firebase project and place it in `app/` (do **not** commit this file).
4. Open the project in Android Studio and let it sync Gradle.
5. Run on an emulator or a physical device.

---

## Architecture (short)
- **Client-only prototype** with Firestore as the primary data layer.
- Simple collections: `users`, `items`, `chats`, `courses`.
- Security rules enforce basic ownership (only owners can edit/delete their items).

---

## Hard technical problem I solved
- **Realtime chat + basic offline resilience:** implemented a Firestore-based chat schema that supports message write/reads and basic ordering. Handled image upload in messages by first uploading to Storage then attaching the URL to the message object.

---

## What I learned
- Production-level Firebase setup and security rules.  
- Shipping a small Android app end-to-end (auth, storage, read/write flows).  
- Building an MVP solo under limited institutional support.

## Contact
Raslene Klai — klairaslen@gmail.com  
GitHub: https://github.com/raslenkl


