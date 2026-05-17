______________________________________________________________________

title: "Run ADB Commands in Web Browser with WebADB"
source: "https://technastic.com/webadb-adb-commands-web-browser/"
author:

- "\[[Rakesh Shukla]\]"
  published: 2020-11-16
  created: 2026-05-14
  description: "WebADB lets you execute ADB and Shell commands in a web browser like Chrome without root installing ADB drivers on your computer."
  tags:
- "clippings"

______________________________________________________________________

You can run ADB commands in Chromium-based web browsers without setting up Android SDK Platform tools on your computer. WebADB is a handy online tool that brings the powerful features of ADB to desktop and mobile browsers. This web browser-based tool supports all ADB and ADB Shell commands. Moreover, it allows you to control your Android phone or tablet from another device via ADB in Chrome and other supported browsers.

WebADB takes advantage of the WebUSB API found in all Chromium-based web browsers, including the ones listed below.

- Google Chrome
- Microsoft Edge
- Opera
- Vivaldi
- Brave
- Blisk
- Colibri
- Yandex Browser
- Cent Browser
- UC Browser

WebUSB API lets web pages access and communicate with devices connected via USB. The developer, Yume Chan, recommends the latest version of Google Chrome or Microsoft Edge for the best compatibility.

Table of Content

## Features of WebADB

WebADB can be used to execute ADB commands from a compatible desktop or mobile web browser. Besides, you can browse the files stored on your Android device, capture the screen, and install APK files from a web browser’s interface. You can also [mirror your phone’s screen using Scrcpy](https://technastic.com/mirror-android-device-pc/) via WebADB. Below is a complete list of its features.

- Device information
- Run ADB shell commands
- Manage files
- Install APK files
- [Enable ADB over Wi-Fi to run ADB](https://technastic.com/set-up-adb-over-wifi-android/) commands wirelessly.
- Capture screenshots and record screens.
- Mirror and control the device via USB with SCRCPY (screen copy).
- Power off and reboot Android devices to Bootloader, Fastboot, Recovery, Qualcomm EDL, and Download (Samsung) modes.
- Supports mobile browsers.

The whole concept of WebADB looks pretty neat, but it has its dark sides too. Many of us might not be comfortable granting ADB access to a web app. It’s like handing over the key to our house to a stranger. If someone hacks the WebADB website, they can do anything from uploading all our data to installing malware stealthily. Such a thing might turn out to be a nightmare for anyone.

## Using ADB in a Web Browser

Having discussed the features of WebADB, let’s see how to use it to execute ADB Shell commands via web browsers that support the WebUSB API.

1. First, [enable USB debugging](https://technastic.com/developer-options-android/) from the **Developer Options** on your Android device.
1. Open the [WebADB web app](https://app.webadb.com/#/) in a Chromium-based web browser.
1. If you are a Windows user, open [Chrome’s flags page](https://technastic.com/best-google-chrome-flags/) and enable the **New USB Backend**.
   ```
   chrome://flags/#enable-webusb-device-detection
   ```
   [![ENABLE NEW USB BACKENED CHROME]
