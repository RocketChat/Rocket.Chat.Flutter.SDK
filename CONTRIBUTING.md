# Contributing to Rocket.Chat Flutter SDK

We appreciate your interest in contributing to the Rocket.Chat Flutter SDK! Your help and expertise are essential to the continued development and improvement of this project.

This document provides guidelines and instructions to make the contribution process as smooth as possible.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Setting Up the Development Environment](#setting-up-the-development-environment)
- [Building the Project](#building-the-project)
- [GitHub Actions CI](#github-actions-ci)
- [Project Structure](#project-structure)
- [Bug Reports](#bug-reports)
- [Feature Requests](#feature-requests)
- [Pull Requests](#pull-requests)
- [Coding Guidelines](#coding-guidelines)
- [Testing](#testing)
- [Troubleshooting](#troubleshooting)
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

**Local Setup**

Clone the repository:

   ```sh
   git clone https://github.com/your-username/Rocket_Chat_FlutterSDK.git
   ```

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

You're all set, Happy coding!

## Building the Project

When building a package, you will not receive a standalone output file like an APK or an app bundle, as the package is meant to be used as a dependency in other Flutter projects. **Ensure that the package is built without any errors and can be easily imported and used in other projects** using following command:

1. Install the required dependencies:

   ```bash
   melos bootstrap
   ```

2. Run test with melos, hit:

   ```bash
   melos run test
   ```

3. Analyze code with melos, hit:

   ```bash
   melos run analyze
   ```

4. Compile and dry-run publish with Melos, hit:

   ```bash
   melos run publish
   ```

### Build Artifacts

For the sample apps included in each package, you can build them as you would with any other Flutter application, and you'll get an output file (e.g., APK for Android) after the build process is completed.

To build a sample package: 

1. Navigate to the app's root directory

   ```sh
   cd rocket_chat_api/sample_app
   ```
   or
   ```sh
   cd rocket_chat_embeddedchat_component/sample_app
   ```
2. Get all dependencies

   ```bash
   flutter pub get
   ```

3. Run:
   ```bash
   flutter build <platform>
   ```

Replace `<platform>` with the platform you are targeting (e.g., `apk`, `ios`, `web`).
After building, the artifacts for each sample apps will be located in the following directories:

- `rocket_chat_embeddedchat_component`: `packages/rocket_chat_embeddedchat_component/sample_app/build/outputs`
- `rocket_chat_api`: `packages/rocket_chat_api/sample_app/build/outputs`

### Error Logs

If the build process encounters any errors, check the terminal or debug console in your development environment (e.g., VSCode) for error messages and stack traces.

## GitHub Actions CI

The project is integrated with GitHub Actions CI, which automatically builds and tests the packages on every push and pull request. The CI configuration can be found in `.github/workflows/ci.yml`.

### CI Logs

If the CI process fails, logs can be accessed from the "Actions" tab in the GitHub repository. Click on the specific run, and then select the failed job to view the logs.

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

## Troubleshooting

If you encounter any issues during the build process or while using the package, follow these steps to troubleshoot:

1. **Check the build logs**: Make sure to carefully examine the build logs in the terminal or your IDE's debug console for any error messages or warnings.
2. **Verify dependencies**: Double-check your `pubspec.yaml` file to ensure that all dependencies are listed and their versions are compatible.
3. **Flutter doctor**: Run `flutter doctor` to identify any potential issues with your Flutter installation or development environment.
4. **Clean and rebuild**: Sometimes, issues can be resolved by simply cleaning your project's build cache and rebuilding. Run `flutter clean` followed by build instruction to perform a clean rebuild of your project.
5. **Search for known issues**: Check the package's GitHub repository for any reported issues or ongoing discussions related to your problem.
6. **Ask for help**: If you're still having trouble, don't hesitate to reach out to the Rocket.Chat community or create a new issue on the GitHub repository.

For more specific guidance on troubleshooting, please provide detailed information about the issue you're facing, including error messages, logs, and any steps you've already taken to resolve the problem.

## Community

We value the contribution of each member of our community and encourage open and respectful communication. If you have any questions or need assistance, feel free to reach out in the project's communication channels, such as GitHub issues or the Rocket.Chat community.

Thank you for your interest in contributing to the Rocket.Chat Flutter SDK! Together, we can make this project better and help shape the future of Rocket.Chat and its integrations.
