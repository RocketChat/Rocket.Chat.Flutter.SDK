# Rocket.Chat API

This package provides a comprehensive wrapper for the Rocket.Chat REST API, making it easy to interact with the Rocket.Chat platform in your Flutter applications.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Compiling the Package](#compiling-the-package)
- [Example App](#example-app)
- [Contributing](#contributing)

## Features

- Comprehensive wrapper for the Rocket.Chat REST API
- Support for all major features of the Rocket.Chat platform
- Asynchronous, non-blocking API calls

## Installation

Add the `rocket_chat_api` package to your `pubspec.yaml` file:

```yaml
dependencies:
  rocket_chat_api: ^VERSION
```

## Usage

Import the package in your Dart code:

```dart
import 'package:rocket_chat_api/rocket_chat_api.dart';
```

Follow the package documentation(once released) for detailed usage instructions and examples.

## Compiling the Package

To compile the package: 

1. Navigate to the `rocket_chat_api` directory 

```bash
cd packages/rocket_chat_api
```

2. Get all the dependencies:

```bash
flutter pub get
```

3. Run tests:

```bash
flutter test
```

4. Analyze code:

```bash
flutter analyze
```

5. Compile rocket_chat_api: 

```bash
flutter pub publish --dry-run
```

Above commands will compile the package, and any errors will be displayed in the terminal or IDE's debug console.

Note: Since this is a package, there won't be a separate artifact generated after building the package. The package is built alongside your main Flutter application. **Make sure package compile without any error.**

## Example App

A example app demonstrating the usage of the `rocket_chat_api` package can be found in the `example` directory. To run the example app:

navigate to the `example` directory 

```bash
cd packages/rocket_chat_api/example
```

and execute the following commands:

```bash
flutter clean
flutter pub get
flutter run
```

To build the example app, hit:
```bash
flutter build <platform>
```

Replace `<platform>` with the platform you are targeting (e.g., `apk`, `ios`, `web`).
After building, the artifacts for the example app will be located in the `packages/rocket_chat_api/sample_app/build/outputs` directory.

## Contributing

We welcome contributions to the Rocket.Chat Flutter SDK at every level! Before contributing, please read the [CONTRIBUTING.md](CONTRIBUTING.md) file for guidelines on how to contribute and set up the development environment.
