# Mantil

Mantil is a cloud development toolset for Go and AWS Lambda.

Cloud-native development demands a new approach to building, launching and observing cloud apps. Mantil is a 
modern Go toolset for creating and managing AWS Lambda projects.

In this early version, Mantil addresses fundamental issues often encountered while building and launching the apps:
* setting up a new AWS Lambda project from scratch or an existing template
* setting up a local development environment and tieing everything with AWS
* deploying the app on every change
* code testing via standard go tests or by invoking a specific function
* getting logs instantly
* supporting multiple development stages and parallel lines of deployment

Please, go and try it! Let us know your thoughts.

# Installation

## Homebrew (Mac and Linux)

Use [Homebrew](https://brew.sh) to install the latest version:

```
brew tap mantil-io/mantil
brew install mantil
```

## Direct Download (Linux, Windows and Mac)

Below are the available downloads for the latest version of Mantil (0.1.20). Please download the right package for your operating system and architecture.

Mantil is distributed as a single binary. Install Mantil by extracting it and moving it to a directory included in your system's PATH .

| OS      | Architecture | Download link                                                                                                                |
| --------| ------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| Darwin  | arm64        | [mantil_Darwin_arm64.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Darwin_arm64.tar.gz)     |
| Darwin  | x86_64       | [mantil_Darwin_x86_64.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Darwin_x86_64.tar.gz)   |
| Linux   | x86_64       | [mantil_Linux_x86_64.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Linux_x86_64.tar.gz)     |
| Linux   | i386         | [mantil_Linux_i386.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Linux_i386.tar.gz)         |
| Linux   | arm64        | [mantil_Linux_arm64.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Linux_arm64.tar.gz)       |
| Linux   | arm          | [mantil_Linux_arm.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Linux_arm.tar.gz)           |
| Windows | x86_64       | [mantil_Windows_x86_64.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Windows_x86_64.tar.gz) |
| Windows | i386         | [mantil_Windows_i386.tar.gz](https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Windows_i386.tar.gz)     |


### An example for Linux x86_64

```
wget https://s3.eu-central-1.amazonaws.com/releases.mantil.io/latest/mantil_Linux_x86_64.tar.gz
tar xvfz mantil_Linux_x86_64.tar.gz
mv mantil /usr/local/bin
```

# Documentation

We suggest to check out "Getting started" and familiarize yourself with "General Concepts."

The documentation is divided into several sections:
* [Getting Started](getting_started.md)
* [General Concepts](project_structure.md)
* [Mantil CLI Commands](commands/README.md)
* [Project Templates](templates/excuses.md)
* [Troubleshooting and support](troubleshooting.md)

# License

This documentation is licensed under Creative Commons (CC BY-SA 4.0).

