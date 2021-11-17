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

## Homebrew (Mac)

Use [Homebrew](https://brew.sh) to install the latest version:

```
brew tap mantil-io/mantil
brew install mantil
```

## Download (Linux, Windows and Mac)

Below are the available downloads for the latest version of Mantil (0.1.20). Please download the proper package for your operating system and architecture.

Mantil is distributed as a single binary. Install Mantil by extracting it and moving it to a directory included in your system’s PATH .

