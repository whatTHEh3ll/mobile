---
title: "Things to Do After Installing Termux: A Comprehensive Guide for Beginners"
source: https://dev.to/terminaltools/things-to-do-after-installing-termux-a-comprehensive-guide-for-beginners-3f9c
author:
  - "[[Stephano Kambeta]]"
published: 2025-04-20
created: 2026-05-21
description: Termux is a powerful terminal emulator and Linux environment for Android that opens the door to a... Tagged with termux, termuxforbeginners, termuxtutorials, installtermux.
tags:
  - Android
  - clippings
---
Termux is a powerful terminal emulator and Linux environment for Android that opens the door to a world of possibilities. Whether you're a beginner or a seasoned tech enthusiast, setting up Termux properly is the first step to unlocking its potential. In this guide, we’ll walk you through the essential things to do after installing Termux, ensuring a smooth start to your Linux-on-Android journey.

[![Things to Do After Installing Termux: A Comprehensive Guide for Beginners](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Frjvzpurvhb9ndad0m49x.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhMhUJLbsGrRdvRPOGUWRFwIAnJzfgGXaB2toclq9alzFvQ2_EOmrJr6Ow8WlAlnW3jBNVia7pIuWpG__SCUkxAzE2njzGLcq8cJnuaXjf5gGVpKgrkA5-zFBx56I6v0njOsOc0ewvSeifTfp7teZX-6VrnEulpdg7yTOF1l-0feuG8v9tn54agv5ftLFho/s1280/Dark%20Blue%20White%20Brush%20Stroke%20Business%20Ideas%20YouTube%20Thumbnail%20%2842%29-min.png)

## 1\. Update and Upgrade Termux

The first step after installing [Termux](https://terminaltools.blogspot.com/p/termux-tutorial-comprehensive-guide-to.html) is to update and upgrade the packages. This ensures you’re running the latest and most secure versions of the tools available. Run the following command:

```
pkg update && pkg upgrade
```

This will fetch the latest updates and apply them to your Termux installation.

## 2\. Set Up Storage Access

By default, Termux doesn’t have access to your device storage. Grant it permission to access files on your device by running:

```
termux-setup-storage
```

This creates a folder `storage` in your Termux home directory and allows you to access your device files seamlessly.

## 3\. Install Basic Packages

Termux doesn’t come preloaded with many tools. Here are some basic packages to install right away:

```
pkg install python git curl wget nano vim
```
- **Python**: For scripting and development.
- **Git**: To manage repositories.
- **Curl/Wget**: To download files.
- **Nano/Vim**: Text editors for scripting and configuration.

## 4\. Customize Termux Appearance

Why stick to the default look when you can make Termux your own? You can customize the color scheme and fonts using the Termux styling tools. Install them with:

```
pkg install termux-tools
```

Then edit the files `~/.termux/colors.properties` for colors and `~/.termux/font.ttf` for custom fonts.

## 5\. Install Advanced Shells

While Termux comes with Bash as the default shell, you might prefer other shells like Zsh for its advanced features and better customization. Install Zsh with:

```
pkg install zsh
chsh -s zsh
```

Consider pairing Zsh with a plugin manager like Oh My Zsh for enhanced functionality.

## 6\. Install Networking Tools

Networking tools are vital, especially if you’re into [cybersecurity](https://terminaltools.blogspot.com/p/comprehensive-guide-to-cybersecurity.html) or network troubleshooting. Start with:

- **Net-tools** (for `ifconfig` and similar commands):
```
pkg install net-tools
```
- **SSH** (to connect to remote servers):
```
pkg install openssh
```

## 7\. Install Programming Languages

Termux supports various programming languages, making it a perfect coding environment on the go. Install the following as needed:

- **Python**:
```
pkg install python
```
- **Node.js**:
```
pkg install nodejs
```
- **Ruby**:
```
pkg install ruby
```

## 8\. Set Up a Package Manager

Installing and managing tools becomes easier with package managers:

- **Pip** for Python:
```
pkg install python-pip
```
- **npm** for Node.js:
```
pkg install nodejs-lts
```

## 9\. Install Cybersecurity Tools

For those interested in [ethical hacking](https://terminaltools.blogspot.com/p/ethical-hacking-understanding-roles.html) or cybersecurity, Termux can be your portable lab. Start with:

- **[Metasploit Framework](https://terminaltools.blogspot.com/2023/11/metasploit-framework.html)**:
```
pkg install unstable-repo
pkg install metasploit
```
- **[Nmap](https://terminaltools.blogspot.com/2023/11/how-to-install-and-use-nmap-in-termux.html)**:
```
pkg install nmap
```

These tools are essential for penetration testing and network scanning.

## 10\. Clone Git Repositories

Git is one of the most powerful tools you can use on Termux. Install Git and clone repositories to work on your projects:

```
pkg install git
git clone <repository_url>
```

You can now collaborate on projects or download scripts and tools shared by others.

## 11\. Install Termux API

[Termux API](https://wiki.termux.com/wiki/Termux:API) provides access to device features like sensors, SMS, and the camera. To install it:

```
pkg install termux-api
```

Ensure you also install the Termux API app from the Play Store for full functionality.

## 12\. Set Up SSH Server

Turn your Termux into an SSH server to access it remotely. Install the OpenSSH package and start the SSH daemon:

```
pkg install openssh
sshd
```

Now you can connect to your Termux environment from another device.

## 13\. Install Tools for Specific Tasks

Depending on your use case, install additional tools:

- **Hacking tools**: Metasploit, [Nikto](https://terminaltools.blogspot.com/2023/11/nikto.html), [Hydra](https://terminaltools.blogspot.com/2023/11/menu-termux-termux-install-hydra-in.html), etc.
- **Development tools**: GCC, Python libraries, etc.
- **Data analysis**: Jupyter Notebook, Pandas.

For example, if you’re into ethical hacking, Termux provides a lightweight platform for experimenting with penetration testing tools.

## 14\. Join the Termux Community

To make the most out of Termux, consider joining communities and forums where users share tips, tricks, and tutorials. The Termux GitHub page and Reddit community are excellent starting points.

If you find any part of this guide confusing or need further assistance, don't hesitate to reach out! Leave a message in the comments section or contact us directly. We're here to help you make the most of your Termux experience!

**Your feedback is invaluable.** Let us know how we can improve or what topics you'd like to see covered next on **TerminalTools**.

## Final Thoughts

Termux is a versatile tool that can transform your Android device into a powerful Linux environment. By following the steps above, you’ll have a robust setup ready for coding, ethical hacking, networking, or anything else you want to explore.

For more advanced guides and tutorials, be sure to check out our **[TerminalTools blog](https://terminaltools.blogspot.com/)**, where we cover cybersecurity, ethical hacking, and Termux tips in detail!

DEV Community

[![Google AI Education track image](https://media2.dev.to/dynamic/image/width=775%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fu09y9fffqrb2one15j3g.png)](https://dev.to/deved/build-apps-with-google-ai-studio?bb=238781)

## Build Apps with Google AI Studio 🧱

This track will guide you through Google AI Studio's new "Build apps with Gemini" feature, where you can turn a simple text prompt into a fully functional, deployed web application in minutes.
