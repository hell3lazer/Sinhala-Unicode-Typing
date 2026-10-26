# Sinhala Unicode Typing

An open-source, privacy-first Android keyboard tailored specifically for seamless **Sinhala Unicode typing**. Designed with a modern Material Day/Night interface, customizable themes, and intuitive Sinhala character layouts.

---

## Features

- **Intuitive Sinhala Unicode Input**:
  - Full support for Sinhala consonants, vowels, and diacritics (පිල්ලම්).
  - Dedicated Sinhala keyboard layout optimized for natural typing speed and touch accuracy.
  - Quick-switch English keyboard for bilingual communication.
  - Number row and dedicated symbol keyboards.
- **Modern Material Design UI**:
  - Clean Material Day/Night styling with adaptive theme support.
  - Elevated cards, streamlined navigation, and rounded action buttons.
  - Real-time interactive test typing field on the home screen.
- **Custom Keyboard Themes**:
  - Multiple clean dark and light themes (Dark Blue, Dark, Dark Teal, Dark Muted, Light).
  - Modern pill-shaped action/enter keys.
  - Per-app tinting and customizable key height.
- **Privacy First**:
  - **Zero internet access required** — does not send keystrokes anywhere.
  - Built-in Incognito mode to prevent recording typing history.
  - Open source and transparent.
- **Productivity & Ergonomics**:
  - Physical keyboard support.
  - Gesture typing and glide input.
  - Customizable tactile feedback (vibration and sound).
  - Emoji support with fast categorization.

---

## Getting Started & Installation

You can build and install Sinhala Unicode Typing directly using Android Studio or the Gradle command line.

### Prerequisites

- **Java Development Kit (JDK)**: OpenJDK 21
- **Android SDK**: API Level 35
- **Gradle**: Wrapper provided (`./gradlew`)

### Building from Source

To compile a debug APK:
```bash
./gradlew :ime:app:assembleDebug
```
The output APK will be located at:
`ime/app/build/outputs/apk/debug/app-debug.apk`

To compile a release APK:
```bash
./gradlew :ime:app:assembleRelease
```
The output APK will be located at:
`ime/app/build/outputs/apk/release/app-release.apk`

### Installing on Device

With your Android device connected via ADB (USB or Wireless Debugging):
```bash
adb install -r ime/app/build/outputs/apk/release/app-release.apk
```

---

## Development & Code Quality

- **Code Formatting**: Code formatting is enforced using Spotless:
  ```bash
  ./gradlew spotlessApply
  ```
- **Unit Tests**:
  ```bash
  ./gradlew :ime:base-rx:testDebugUnitTest
  ```

---

## Contributing

Contributions, bug reports, and suggestions are welcome! Please check [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines and project structure.

All participants are expected to adhere to the [Code of Conduct](CODE_OF_CONDUCT.md).

---

## Acknowledgments & Upstream

Sinhala Unicode Typing is forked and developed from the open-source [AnySoftKeyboard](https://github.com/AnySoftKeyboard/AnySoftKeyboard) project created by [Menny Even-Danan](https://github.com/menny) and contributors. We gratefully acknowledge their foundational work.

---

## License

```text
Copyright 2026 Sinhala Unicode Typing Contributors
Copyright 2009-2024 Menny Even-Danan and AnySoftKeyboard Contributors

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
