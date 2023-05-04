# Rocket.Chat Flutter SDK

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
[![melos](https://img.shields.io/badge/maintained%20with-melos-f700ff.svg?style=flat-rounded)](https://github.com/invertase/melos)

This repository contains the `Rocket.Chat Flutter SDK`, which includes the `rocket_chat_embeddedchat_component` and `rocket_chat_api` packages. These packages make it easier for developers to integrate and interact with Rocket.Chat in their Flutter applications.

## Table of Contents

- [Packages](#packages)
- [Usage](#usage)
- [Structure](#structure)
- [Contributing](#contributing)
- [License](#license)


## Packages 
We provide a variety of packages depending on the level of customization you want to achieve.

### [`rocket_chat_embeddedchat_component`](https://github.com/RocketChat/Rocket.Chat.Flutter.SDK/tree/main/packages/rocket_chat_embeddedchat_component)
A Flutter package that provides a complete embedded chat UI component for Rocket.Chat.

### [`rocket_chat_api`](https://github.com/RocketChat/Rocket.Chat.Flutter.SDK/tree/main/packages/rocket_chat_api)
A Flutter package that provides a comprehensive wrapper for the Rocket.Chat REST API.

### Sample Apps
Every package folder includes a fully functional sample app with setup instructions.

## Usage

To use the packages in your Flutter project, follow these steps:

1. Add the desired package to your `pubspec.yaml` file:

```yaml
dependencies:
  rocket_chat_embeddedchat_component: ^VERSION
  // or
  rocket_chat_api: ^VERSION
```

2. Import the package in your Dart code:

```dart
import 'package:rocket_chat_embeddedchat_component/rocket_chat_embeddedchat_component.dart';
// or
import 'package:rocket_chat_api/rocket_chat_api.dart';
```

3. Follow the documentation and sample apps to learn how to use the packages.

## Structure
Rocket.Chat Flutter SDK is a monorepo built using [Melos](https://docs.page/invertase/melos). Individual packages can be found in the `packages` directory while configuration and top-level commands can be found in `melos.yaml`. 

To get started, run `bootstrap` after cloning the project. 

```shell
melos bootstrap
```

## Contributing

We welcome contributions to the Rocket.Chat Flutter SDK! Before contributing, please read the [CONTRIBUTING.md](CONTRIBUTING.md) file for guidelines on how to contribute and set up the development environment.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
