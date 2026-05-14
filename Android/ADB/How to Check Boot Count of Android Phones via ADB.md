---
title: "How to Check Boot Count of Android Phones via ADB"
source: "https://technastic.com/check-boot-count-android-phone-adb/"
author:
  - "[[Rakesh Shukla]]"
published: 2024-09-21
created: 2026-05-14
description: "The \"Boot_Count\" string records the number a device has been booted. Here's the ADB command to check the boot count of Android phones."
tags:
  - "clippings"
---
I’m unsure how many Android users ever want to know how many times their device has booted. However, if you are a curious tech enthusiast, you might be interested in learning little but important things about your device. With the help of ADB, you can not only [speed up your Android phone](https://technastic.com/adb-commands-improve-performance-android/) and [improve its battery life](https://technastic.com/adb-battery-optimization-commands/) but also get various technical information about it. In this tutorial, we’ll 2 ADB commands that help you show the boot count of Android phones and tablets.

ADB is a versatile and powerful command-line tool for Android that allows users to perform basic and advanced tasks. It can help users tweak system settings, diagnose the device, manage permissions, simulate hardware buttons, make calls and send messages, etc. using commands. Having set up ADB on your Windows, Mac, or Linux, you’ll have a range of [ADB commands](https://technastic.com/adb-commands-list-adb-cheat-sheet/) to try.

The “Boot\_Count” or “Phenotype\_boot\_count” string was introduced to Android with the Noughat SDK. So, if you have a device running Android 7, 8, 9, 10, 11, 12, 13, 14, or above, you can see its boot count via ADB. Please note that the boot count stat is saved in the settings of the device. It means that the counter is reset when a factory reset is performed. That’s to say, the commands mentioned in this article will show the number of times a device was booted since the last factory reset.

## Steps to Check Boot Count via ADB

To find the boot count of your Android device using ADB, first, ensure you have ADB installed on your computer. Follow the steps below.

1. Download and install the [latest Android SDK Platform tools](https://technastic.com/android-sdk-platform-tools-download/).
2. Enable the USB Debugging settings in [Developer Options](https://technastic.com/developer-options-android/).
3. Connect your phone to your computer via a USB cable.
4. Open the ‘ **platform-tools** ‘ folder and launch a command or terminal window with its path. You can do that either by entering “ **powershell** ” in the folder’s address bar or right-clicking inside the folder window and selecting the **Open in Terminal** option. [![open command prompt with folder path in windows 11](https://technastic.com/wp-content/uploads/2022/12/open-command-prompt-windows-10.png)](https://technastic.com/wp-content/uploads/2022/12/open-command-prompt-windows-10.png)
5. When the command window is launched, execute the following command.
	```
	adb shell settings get global boot_count
	or
	adb shell settings get global Phenotype_boot_count
	```
6. You’ll see the boot count of your Android device in the output.[![adb shell get global boot count android](https://technastic.com/wp-content/uploads/2024/09/adb-get-global-boot-count-android.png)](https://technastic.com/wp-content/uploads/2024/09/adb-get-global-boot-count-android.png)
7. There is yet another command that displays the boot count of Android devices.
	```
	adb shell settings list global
	```
8. Check the numerical value next to **Phenotype\_boot\_count** to find how many times your Android device has been booted.[![adb shell settings list global command](https://technastic.com/wp-content/uploads/2024/09/adb-shell-settings-list-global.png)](https://technastic.com/wp-content/uploads/2024/09/adb-shell-settings-list-global.png)

You can also check the boot count of your Android via [ADB without a computer or root using the aShell](https://technastic.com/webadb-adb-commands-web-browser/) on your device. Just set up [Shizuku](https://technastic.com/shizuku-rootless-apps-mods-android/) on your phone or tablet, and install the [aShell app](https://play.google.com/store/apps/details?id=in.sunilpaulmathew.ashell) to run ADB commands.

[![adb command to check boot count ashell app](https://technastic.com/wp-content/uploads/2024/09/adb-command-to-check-boot-count-ashell-app.jpg)](https://technastic.com/wp-content/uploads/2024/09/adb-command-to-check-boot-count-ashell-app.jpg)

That’s all! Try the 3 ADB commands and share the boot count of your Android phone.