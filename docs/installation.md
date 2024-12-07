---
sidebar_position: 1
---


# Installing Golang

This guide will walk you through all of the steps necessary to install Go on your computer and to get you to go programming!

## Prerequisites

Before you begin, make sure that you are:

- Running one of the big three operating systems (Linux, macOS, or Windows).

- Are connected to the internet.

## 1. Downloading Go

### Windows & Linux

1. Visit the Go download page: [https://golang.org/dl/](https://golang.org/dl/)
2. Download the appropriate installation file for your operating system.

### macOS

1. Make sure you have brew installed on your computer.
2. Type the following command:
   ```bash
   brew install go
   ```

## 2. Installing Go

### Windows

1. Run the .msi installer that was downloaded off of the Go download page.
2. Follow the prompts in the installer to complete the setup. Make sure you close and reopen your terminal or vscode in order to load Go into the path.

### Linux

- Don't have a linux OS to reproduce. Check instructions on official Go website.

### macOS

- Already installed from brew, installed when downloading.

## 3. Verify Installation

After installation, open a new terminal and type the command below to make sure that the installation went smooth:

```bash
go version
```

It should print out the Go version that you installed from the downloads page, e.g.:

```bash
go version go1.23.4 darwin/arm64
```

## 4. Success!

You successfully installed Go onto your computer! Go to the next tutorial to see Go in action.
