---
title: "Run ADB Commands in Web Browser with WebADB"
source: "https://technastic.com/webadb-adb-commands-web-browser/"
author:
  - "[[Rakesh Shukla]]"
published: 2020-11-16
created: 2026-05-14
description: "WebADB lets you execute ADB and Shell commands in a web browser like Chrome without root installing ADB drivers on your computer."
tags:
  - "clippings"
---
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
2. Open the [WebADB web app](https://app.webadb.com/#/) in a Chromium-based web browser.
3. If you are a Windows user, open [Chrome’s flags page](https://technastic.com/best-google-chrome-flags/) and enable the **New USB Backend**.
	```
	chrome://flags/#enable-webusb-device-detection
	```
	[![enable new usb backened chrome](https://technastic.com/wp-content/uploads/2020/12/enable-new-usb-backened-chrome.jpg)](https://technastic.com/wp-content/uploads/2020/12/enable-new-usb-backened-chrome.jpg)
4. Connect your phone or tablet to the computer via a USB cable and select **File Transfer mode** when prompted. Make sure no other Android device is connected to your PC, as WebADB can communicate with only one device at a time. If multiple devices are connected, you’ll get the “ **Unable to claim interface** ” error.
5. Click the **Add Device** button, select your device, and click the **Connect** button.[![add android device in web adb](https://technastic.com/wp-content/uploads/2020/12/add-android-device-web-adb.png)](https://technastic.com/wp-content/uploads/2020/12/add-android-device-web-adb.png)
6. Your Android device will be connected to WebADB. You are now ready to enjoy all the features it offers.
7. Please note that you’ll need to **Allow USB debugging** on your device when prompted.[![allow usb debugging on vivo phones](https://technastic.com/wp-content/uploads/2020/08/allow-usb-debugging-vivo.jpg)](https://technastic.com/wp-content/uploads/2020/08/allow-usb-debugging-vivo.jpg)
8. If you want to run a Shell command, click on **Interactive Shell**. You don’t need to execute `adb shell` first to start the daemon, as WebADB activates that by default. For instance, to get the list of all system apps installed on your Android device, type `pm list packages -s` in the command box and press the **Enter** key. Similarly, you are supposed to omit the “adb” part while using ADB commands. For instance, to [boot an Android device into recovery mode](https://technastic.com/samsung-recovery-mode/), use `reboot recovery`. [![adb command in chrome browser](https://technastic.com/wp-content/uploads/2020/12/webadb-shell-command.png)](https://technastic.com/wp-content/uploads/2020/12/webadb-shell-command.png)
9. To mirror your Android device’s screen in a web browser window, click **Scrcpy**. Just click the **Start** button to start mirroring and control your device from the computer.

## Using WebADB on a Mobile Browser

WebADB also lets you send ADB commands from one Android device to another phone or tablet. That means you don’t need a laptop or desktop computer or even root privileges for that.

1. Open **WebADB** in your phone’s web browser.
2. Since the command box on the WebADB website is not properly visible in a mobile browser window, you should enable the **Desktop site** option from the browser menu.[![enable desktop site option in chrome for android](https://technastic.com/wp-content/uploads/2020/12/desktop-site-chrome-android.jpg)](https://technastic.com/wp-content/uploads/2020/12/desktop-site-chrome-android.jpg)
3. Make sure to enable **USB debugging** on the other Android phone or tablet.
4. You will need a **USB OTG** or **USB C-Type to C-Type cable**.  
	[![USB OTG and USB Type-C to Type-C cable](https://technastic.com/wp-content/uploads/2020/12/usb-otg-usb-ctype-cable.jpg)](https://technastic.com/wp-content/uploads/2020/12/usb-otg-usb-ctype-cable.jpg)
5. Plug the USB cable into the phone you’ll use as a host. Then plug the other end of the USB-C cable into the device you want to send the commands to. In my case, I am using the Galaxy Note 10 as a host so I can control my Redmi K20 Pro.
6. When you connect the first device (host) to the second one, it’ll prompt you to select the USB connection mode. You must select the **File Transfer** mode shown below.[![android file transfer mode](https://technastic.com/wp-content/uploads/2020/12/android-file-transfer-mode.jpg)](https://technastic.com/wp-content/uploads/2020/12/android-file-transfer-mode.jpg)
7. Also, you’re supposed to enable **USB debugging** on the second device and authorize debugging when prompted.
8. Now, click the **Interactive Shell** option on WebADB, and you can send any ADB command via the mobile web browser to any Android phone or tablet without root and using a computer.

All the features of WebADB work flawlessly on Chrome for Android. I tested the screen mirroring feature called Scrcpy, and it worked as expected.

[![android screen mirroring via scrcpy](https://technastic.com/wp-content/uploads/2020/12/adb-command-android.jpg)](https://technastic.com/wp-content/uploads/2020/12/adb-command-android.jpg)

You can use WebADB on computers and Android devices. The feature I like most is its compatibility with mobile browsers like Chrome, Microsoft Edge, Opera, etc. It fills a much-needed void by allowing us to control a phone or tablet from another Android device without root.

Source: [GitHub](https://github.com/yume-chan/ya-webadb)