# Contributing to Sinhala Unicode Typing

Thank you for your interest in contributing to **Sinhala Unicode Typing**! Whether reporting an issue, proposing an improvement, or contributing code, your help is appreciated.

---

## Code of Conduct

All contributors and participants are expected to adhere to our [Code of Conduct](CODE_OF_CONDUCT.md). Please treat fellow contributors with respect and kindness.

---

## Development Environment Setup

To build and develop Sinhala Unicode Typing, ensure you have:

- **Java Development Kit (JDK)**: OpenJDK 21 installed.
- **Android SDK**: API Level 35 (with Build Tools).
- **Git**: Installed and configured.
- **Android Studio**: Android Studio Ladybug or later recommended.

Make sure your `local.properties` file points to your Android SDK installation:
```properties
sdk.dir=/path/to/android/sdk
```

---

## Project Structure

- `ime/`: Core keyboard application modules.
  - `ime/app/`: The primary application module (`com.sinhala.unicode.typing`).
  - `ime/pixel/`: Material theme styles, palettes, day/night resources, and custom UI views.
  - `ime/base/` & `ime/base-rx/`: Base keyboard logic, reactive event pipelines, and core state handling.
  - `ime/dictionaries/`: Dictionary loaders and word suggestion logic.
  - `ime/gesturetyping/`: Glide and gesture typing algorithms.
- `addons/`: Add-on modules including the dedicated Sinhala language pack under `addons/languages/sinhala/`.

---

## Building the Project

Always use the Gradle wrapper:

- **Build Debug APK**:
  ```bash
  ./gradlew :ime:app:assembleDebug
  ```
- **Build Release APK**:
  ```bash
  ./gradlew :ime:app:assembleRelease
  ```
  *(Note: Do not run `./gradlew build` directly, as it triggers non-Android lifecycle tasks. Use `assembleDebug` or `assembleRelease` instead).*

---

## Code Style & Formatting

We use [Spotless](https://github.com/diffplug/spotless) to maintain clean and consistent formatting across all Java, Kotlin, and XML resources.

Before submitting code, always run the auto-formatter:
```bash
./gradlew spotlessApply
```

---

## Running Tests

To run unit tests across modules:
```bash
./gradlew :ime:base-rx:testDebugUnitTest
```

When running tests in the `:ime:app` module, use a specific test filter:
```bash
./gradlew :ime:app:testDebugUnitTest --tests "com.anysoftkeyboard.keyboards.views.preview.KeyPreviewsManagerTest"
```

---

## License

Sinhala Unicode Typing is distributed under the [Apache License, Version 2.0](LICENSE). By contributing to this repository, you agree that your contributions are licensed under the same Apache 2.0 terms.
