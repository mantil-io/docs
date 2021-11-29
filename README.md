# Mantil

[Mantil](https://www.mantil.com) is a cloud development toolset for Go and AWS Lambda.

Cloud-native development demands a new approach to building, launching and
observing cloud apps. Mantil is a modern Go toolset for creating and managing
AWS Lambda projects.

In this early version, Mantil addresses fundamental issues often encountered
while building and launching the apps:
* setting up a new AWS Lambda project from scratch or an existing template
* setting up a local development environment and tieing everything with AWS
* deploying the app on every change
* code testing via standard go tests or by invoking a specific function
* getting logs instantly
* supporting multiple development stages and parallel lines of deployment

Please, go and try it! [Let us know](mailto:support@mantil.com?subject=Mantil%20feedback) your thoughts.

# Installation

## Homebrew (Mac and Linux)

Use [Homebrew](https://brew.sh) to install the latest version:

```
brew tap mantil-io/mantil
brew install mantil
```

## Direct Download (Linux, Windows and Mac)

Below are the available downloads for the latest version of Mantil. Please
download the right package for your operating system and architecture.

Mantil is distributed as a single binary. Install Mantil by extracting it and
moving it to a directory included in your system's PATH.

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

# Activation

Mantil is in closed early beta. After installing Mantil CLI you will need to [answer a few short questions](https://xai8bc1fisj.typeform.com/to/QU5wd7lQ#source=GitHub_RM) to get full access. This is important for us to better understand your use case and it will help us further improve Mantil. 

Once the survey is filled you will receive an activation code in the provided email. Use it in the terminal to finalize your Mantil activation:
```
mantil activate <activation-code>
```
And that's it. Now when Mantil is activated you can start building your AWS Lambda-based Go backends quicker than ever!


# Documentation

We suggest to check out "Getting started" and familiarize yourself with "General
Concepts."

The documentation is divided into several sections:
* [Getting Started](getting_started.md)
* [General Concepts](concepts.md)
* [Using a Mantil API](api.md)
* [API Configuration](api_configuration.md)
* [Mantil CLI Commands](commands/README.md)
* [Troubleshooting and support](troubleshooting.md)

Start exploring by creating Mantil project from one of the templates:
* [ping](https://github.com/mantil-io/template-ping) - default template for new Mantil projects
* [excuses](https://github.com/mantil-io/template-excuses) - UI and environment variables showcase
* [chat](https://github.com/mantil-io/template-chat) - demonstrates WebSocket Mantil API interface

# License

This documentation is licensed under Creative Commons (CC BY-SA 4.0).
