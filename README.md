<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/daytonaio/daytona/raw/main/assets/images/Daytona-logotype-white.png">
    <img alt="Daytona logo" src="https://github.com/daytonaio/daytona/raw/main/assets/images/Daytona-logotype-black.png" width="40%">
  </picture>
</div>

<div align="center">

[![Documentation](https://img.shields.io/github/v/release/daytonaio/docs?label=Docs&color=23cc71)](https://www.daytona.io/docs)
[![License](https://img.shields.io/badge/License-Apache--2.0-blue)](#license)
[![Go Report Card](https://goreportcard.com/badge/github.com/daytonaio/daytona)](https://goreportcard.com/report/github.com/daytonaio/daytona)
[![Issues - daytona](https://img.shields.io/github/issues/daytonaio/daytona)](https://github.com/daytonaio/daytona/issues)
![GitHub Release](https://img.shields.io/github/v/release/daytonaio/daytona)
</div>

<h1 align="center"> Open Source Development Environment Manager</h1>

<div align="center">
  Set up a development environment on any infrastructure with a single command
</div>

<div align="center">
  <img src="https://github.com/daytonaio/daytona/raw/main/assets/images/daytona_demo.gif" width="75%">
</div>

<p align="center">
    <a href="https://www.daytona.io/docs"> Documentation </a>·
    <a href="https://github.com/daytonaio/daytona/issues/new?assignees=&labels=bug&projects=&template=bug_report.md&title=%F0%9F%90%9B+Bug+Report%3A+"> Report Bug </a>·
    <a href="https://github.com/daytonaio/daytona/issues/new?assignees=&labels=enhancement&projects=&template=feature_request.md&title=%F0%9F%9A%80+Feature%3A+"> Request Feature </a>·
    <a href="https://go.daytona.io/slack"> Join Our Slack </a>·
    <a href="https://x.com/daytonaio"> X </a>
</p>

## Features

- **Quick Setup**: Activate a fully configured development environment with a single command.
- **Runs everywhere**: Spin up your development environment on any machine; local, remote, cloud-based, physical server or a VM & on any architecture; x86 or ARM.
- **Various Providers Support**: Choose popular providers like AWS, GCP, Azure, DigitalOcean & [more](https://github.com/orgs/daytonaio/repositories?q=daytona-provider) or use Docker on bare metal.
- **IDE Support** : Seamlessly supports [VS Code](https://github.com/microsoft/vscode), [JetBrains](https://www.jetbrains.com/remote-development/gateway/) products and more, ready to use without configuration. Also includes a built-in Web IDE for convenience.
- **Git Provider Integration**: GitHub, GitLab, Bitbucket and [other](https://www.daytona.io/docs/configuration/git-providers/#add-a-git-provider) Git providers can be connected allowing you to start working on a specific branch or PR and to push changes immediately. 
- **Configuration File Support**: Support for [dev container](https://containers.dev/) and an upcoming expansion to DevFile, Nix & Flox.
- **Prebuilds System**: Drastically improve environment build times by prebuilding them based on Git Providers' hook events.
- **Reverse Proxy Integration**: Enable collaboration and streamline feedback loops by leveraging our reverse proxy. Access preview ports and the Web IDE seamlessly, even behind firewalls. 
- **Extensibility**: Coming soon: extend functionality by developing plugins - linked to all major workspace lifecycle events. (Contributions welcome here!). 
- **Security**: Automatically creates a VPN connection between the client machine and the development environment, ensuring a fully secure connection.
- **Works on my Machine**: Never experience it again.

## Quick Start

To see detailed/manual steps click [here](https://www.daytona.io/docs/installation/installation/#installation).

### Mac / Linux

```bash
curl -sfL get.daytona.io | sudo bash && daytona server -y && daytona
```

### Windows

```pwsh
powershell -Command "irm https://get.daytona.io/windows | iex"
```

### Create your first dev environment by opening a new terminal, and running:

```bash
daytona create
```

**Start coding.**

## Getting Started

### Requirements

Before starting the installation script, if you are going to develop locally, ensure [Docker](https://www.docker.com/products/docker-desktop/) is installed and running.

### Initializing Daytona

To initialize Daytona, follow these steps:

**1. Start the Daytona Server:**
Use this command to initiate the Daytona Server in daemon mode: 

```bash
daytona server
```

**2. Add Your Git Provider of Choice:**
Daytona supports GitHub, GitLab, Bitbucket and [more](https://www.daytona.io/docs/configuration/git-providers/#add-a-git-provider) Git Providers. Use this command to set them up:

```bash
daytona git-providers add
```

**3. Add Your Provider Target:**
This step is for choosing where to deploy Development Environments. By default, Daytona includes a Docker provider to spin up environments on your local machine. For remote development environments, use the command and follow the prompts:

```bash
daytona target create
```

**4. Choose Your Default IDE:**
The default IDE for Daytona is the local VS Code installation. To switch to the Web IDE or any other IDE, use:

```bash
daytona ide
```

Now that you have installed and initialized Daytona, you can proceed to setting up your development environments and start coding instantly.

### Creating Dev Environments

Creating development environments with Daytona is a straightforward process, accomplished with just one command:

```bash
daytona create
```

You can add the `--no-ide` flag if you don't wish to open the IDE immediately after creating the environment.

Upon executing this command, you will be prompted with two questions:

1. Choose the provider to decide where to create a dev environment.
2. Select or type the Git repository you wish to use to create a dev environment.

After making your selections, press enter, and Daytona will handle the rest. All that remains for you to do is to execute the following command to open your default IDE:

```bash
daytona code
```

This command opens your development environment in your preferred IDE, allowing you to start coding instantly.

### Stopping the Daytona Server:

```bash
daytona server stop
```

### Restarting the Daytona Server:

```bash
daytona server restart
```

## How to Extend Daytona

Daytona offers flexibility for extension through the creation of plugins and providers.

### Providers

Daytona is designed to be infrastructure-agnostic, capable of creating and managing development environments across various platforms. Providers are the components that encapsulate the logic for provisioning compute resources on a specific target platform. They allow for the configuration of different targets within a single provider, enabling, for instance, multiple AWS profiles within an AWS provider.

How does it work? When executing the `daytona create` command, Daytona communicates the environment details to the selected provider, which then provisions the necessary compute resources. Once provisioned, Daytona sets up the environment on these resources, allowing the user to interact with the environment seamlessly.

Providers are independent projects that adhere to the Daytona Provider interface. They can be developed in nearly any major programming language. More details coming soon.

### Plugins

Plugins enhance Daytona's core functionalities by adding new CLI commands, API methods, or services within the development environments. They offer configurable settings to tailor the plugin's behavior to the user's needs.

Similar to providers, plugins are independent projects that conform to the Daytona Plugin interface and can be developed in a wide range of programming languages. More details coming soon.

## Contributing

Daytona is Open Source under the [Apache License 2.0](LICENSE), and is the [copyright of its contributors](NOTICE). If you would like to contribute to the software, read the Developer Certificate of Origin Version 1.1 (https://developercertificate.org/). Afterwards, navigate to the [contributing guide](CONTRIBUTING.md) to get started.