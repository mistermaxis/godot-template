# Godot Project Template

This is a template for a Godot project that includes basic project code along with GitHub Action workflows to automate deployment and builds for various platforms, including Linux, Windows, macOS, and Android. It also manages releases based on branch names for pull requests.

## Features :star:

- Basic project setup code for Godot.
- GitHub Actions to deploy to GitHub Pages.
- Build workflows for multiple platforms
- Automatic releases based on source and target branch names in pull requests.

## Getting Started :rocket:

To get started with this template, follow these instructions:

### Prerequisites

- [Godot Engine](https://godotengine.org/download) installed on your machine.
- Git installed to clone the repository.
- An active GitHub account.

### Using this repository as a template

- In the repository main page, look for the **Use this template** button

- It will send you to the **New Repository** page, where you can create a new repository using this template

### Adding to Your Godot Project

- Open Godot Engine

- Select **Import Project**

- Navigate to and select the folder where you cloned this repository

- Click **Import**

## GitHub Actions :gear:

### This project utilizes GitHub Actions for automation

- The workflows are located in the ```.github/workflows``` directory

### Workflow for Building Projects

- The workflow files build the project for the following platforms:

  - **Linux**
  - **Windows**
  - **macOS**
  - **Android**

### Deployment to GitHub Pages

- The game is automatically deployed to **GitHub Pages** whenever a push is made to the `gh-pages` branch.

### Creating Releases

- Releases are automatically created based on your branch naming conventions in pull requests - see [BRANCH_SCHEME](BRANCH_SCHEME.md) for more information

## License :bookmark_tabs:

- This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details

## Contributing :handshake:

- Contributions are welcome! Please submit an [issue](https://github.com/mistermaxis/godot-template/issues) or [pull request](https://github.com/mistermaxis/godot-template/pulls) for any enhancements or fixes

## Acknowledgements :heart:

- [Godot Engine](https://godotengine.org/) for creating an amazing game engine.

- [GitHub Actions](https://github.com/features/actions) for allowing automation of workflows.