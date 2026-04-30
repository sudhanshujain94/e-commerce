# AGENTS.md

## Cursor Cloud specific instructions

### Project Overview

MyShop is a Flutter e-commerce mobile/web application using Provider for state management. All data is in-memory (no backend/database). Target platforms: Android, iOS, Web.

### Environment

- **Flutter SDK**: 2.10.5 installed at `/opt/flutter/bin` (Dart 2.16.2)
- **PATH**: `/opt/flutter/bin` is added to `~/.bashrc`
- **Chrome**: Available at `/opt/google/chrome` for web testing
- **SDK constraint**: `>=2.7.0 <3.0.0` (Dart 2.x required; do NOT upgrade to Flutter 3.x/Dart 3.x)

### Common Commands

| Task | Command |
|------|---------|
| Install deps | `flutter pub get` |
| Lint/analyze | `flutter analyze` |
| Run tests | `flutter test` |
| Run web (dev) | `flutter run -d web-server --web-port=8080 --web-hostname=0.0.0.0` |
| Build web | `flutter build web` |

### Known Issues / Gotchas

- `flutter analyze` reports ~13 info-level deprecation warnings (e.g. `accentColor`, `showSnackBar`). These are expected for this older codebase and do not indicate errors.
- The existing `test/widget_test.dart` is boilerplate from the Flutter template (counter app test) and does **not** match the actual MyShop app. It will fail when run. This is a pre-existing issue, not a regression.
- The Android embedding v1 deprecation warning appears on every Flutter command. It can be safely ignored for web/development purposes.
- Font assets (`assets/fonts/FugazOne-Regular.ttf`, `assets/fonts/Niconne-Regular.ttf`) are required and already present in the repo.
