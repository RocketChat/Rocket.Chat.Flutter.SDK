# Contributing to Rocket.Chat Flutter SDK

We appreciate your interest in contributing to the Rocket.Chat Flutter SDK! Your help and expertise are essential to the continued development and improvement of this project.

This document provides guidelines and instructions to make the contribution process as smooth as possible.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Setting Up the Development Environment](#setting-up-the-development-environemt)
- [Project Structure](#project-structure)
- [Bug Reports](#bug-reports)
- [Feature Requests](#feature-requests)
- [Pull Requests](#pull-requests)
- [Coding Guidelines](#coding-guidelines)
- [Testing](#testing)
- [Community](#community)

## Code of Conduct

By participating in this project, you agree to abide by the [Rocket.Chat Code of Conduct](https://github.com/RocketChat/Rocket.Chat/blob/develop/CODE_OF_CONDUCT.md). Please read and follow it to ensure a respectful and inclusive environment for all contributors.

## Getting Started

1. Fork the repository on GitHub.
2. Clone the forked repository to your local machine.
3. Follow the instructions below to set up the development environment.
4. Identify an issue or feature you want to work on or create a new issue to discuss your ideas.
5. Before starting the implementation, discuss your approach in the issue comments to ensure that your work aligns with the project's direction and goals.

## Setting Up the Development Environment

To set up the development environment for the Rocket.Chat Flutter SDK, follow these steps:

1. Clone the repository:

   ```sh
   git clone https://github.com/your-username/Rocket_Chat_FlutterSDK.git
   ```

2. Navigate to the project directory:

   ```sh
   cd rocket_chat_api
   ```
   or
   ```sh
   cd rocket_chat_embeddedchat_component
   ```

3. Install the required dependencies:

   ```sh
   flutter pub get
   ```

### Local Setup

Congratulations. 🎉.  You've successfully cloned our repository, and you are ready to make your first contribution. Before you can start making code changes, there are a few things to configure. 

**Melos Setup**

RCFlutterSDK uses `Melos` to manage our mono-repository. For those unfamiliar, Melos is used to  split up large code bases into separate independently versioned packages. To install Melos, developers can run the following command:

```bash
pub global activate melos 
```

Once activated, users can now "bootstrap" their local clone by running the following:

```bash
melos bootstrap
```

Bootstrap will automatically fetch and link dependencies for all packages in the repository. It is the Melos equivalent of running `flutter pub get`.

Bonus Tip: You can define and run custom scripts using Melos, We use custom scripts for all sorts of actions like testing, lints, and more. 

To run a script, use `melos run <script name>`.

Happy coding!

## Project Structure

- `.github`: GitHub files including issue templates, pull request templates, and GitHub Action scripts.

- `packages/`: contains all the packages for Rocket Chat.
  - `rocket_chat_api/`: contains the core package for Rocket Chat Flutter.
    - `lib/`: contains the source code for the package.
    - `test/`: contains unit, widget and integration tests for the package.
    - `pubspec.yaml`: contains the package dependencies and other metadata.
    -  `sample_app`: contains the example Flutter application for the rocket_chat_api.

  - `rocket_chat_embeddedchat_component/`: contains the Flutter UI package for Rocket Chat.
    - `lib/`: contains the source code for the package.
    - `test/`: contains unit, widget and integration tests for the package.
    - `pubspec.yaml`: contains the package dependencies and other metadata.
    -  `sample_app`: contains the example Flutter application for the rocket_chat_embeddedchat_component.
- `.gitignore`: Listing of files and file extensions ignored for this project.
- `README`: Project overview and usage guide.
- `LICENSE`: Legal.
- `melos.yaml`: Configuration file used to control [Melos](https://pub.dev/packages/melos), our mono-repo management tool of choice.


## Bug Reports

When reporting a bug, please include the following information:

- A clear and concise description of the issue.
- Steps to reproduce the problem.
- Any relevant logs or error messages.
- Information about your environment, such as the Flutter and Dart versions, OS, and device (if applicable).
- Possible solutions or workarounds, if you have any.

Please create an issue using the "Bug report" template on GitHub.

## Feature Requests

When requesting a new feature, please include the following information:

- A clear and concise description of the feature.
- An explanation of why the feature is useful and how it aligns with the project's goals.
- Any relevant examples or use cases.
- Possible implementation approaches or considerations, if you have any.

Please create an issue using the "Feature request" template on GitHub.

## Pull Requests

Before submitting a pull request, please make sure that your changes adhere to the following guidelines:

- The code follows the project's coding guidelines and best practices.
- The code has been tested, and all tests pass.
- The code is well-documented, and any new features or changes are explained in the issue and PR comments.
- The PR is linked to a relevant issue, and the issue is referenced in the PR description.
- The PR title and description clearly describe the changes and their purpose.

## Coding Guidelines

- Follow the [Effective Dart](https://dart.dev/guides/language/effective-dart) guidelines.
- Adhere to the project's code style and linting rules.
- Write clean, maintainable, and modular code.
- Keep functions and classes focused on a single responsibility.
- Comment your code to explain complex or unusual logic.
- Use meaningful names for variables, functions, and classes.

## Testing

- Write unit, integration, and widget tests for your code.
- Make sure all tests pass before submitting a pull request.
- Update or add new tests if you make changes to existing code or implement new features.
- Follow the project's testing best practices and conventions.

## Community

We value the contribution of each member of our community and encourage open and respectful communication. If you have any questions or need assistance, feel free to reach out in the project's communication channels, such as GitHub issues or the Rocket.Chat community.

Thank you for your interest in contributing to the Rocket.Chat Flutter SDK! Together, we can make this project better and help shape the future of Rocket.Chat and its integrations.
