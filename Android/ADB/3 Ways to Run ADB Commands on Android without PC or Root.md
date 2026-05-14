---
title: "3 Ways to Run ADB Commands on Android without PC or Root"
source: "https://technastic.com/run-adb-commands-android-without-pc/"
author:
  - "[[Rakesh Shukla]]"
published: 2025-05-18
created: 2026-05-14
description: "Using a Shizuku app aShell and terminal app Termux, we can use ADB and Shell commands on Android devices without root or a computer."
tags:
  - "adb"
---
Do you need to use an ADB command on your Android phone or tablet to perform a task, but don’t have access to a computer? Earlier, it was impossible to run commands on an Android device itself without superuser permissions. Thankfully, Terminal emulator apps like aShell (Shizuku) and Termux allow you to use ADB natively. This tutorial will explore different methods to run ADB on Android devices without root, including Termux, aShell, and WebADB.

Let’s check out different methods to harness the power of ADB on Android devices without a PC.

Table of Content

## 1\. Using Shizuku-supported aShell App

Shizuku acquires system APIs and permissions through wireless debugging and passes them to supported apps. Unlike other apps that require root privileges to modify Android devices, Shizuku leverages certain [Android permissions](https://technastic.com/all-special-dangerous-android-permissions/). You can use the [Shizuku-supported apps](https://technastic.com/best-shizuku-apps-mods-android/) to do amazing things without rooting your device. Besides modifying, tweaking, and customizing your Android phone, Shizuku also makes it possible to use ADB on Android devices without root.

1. Download and install [Shizuku](https://play.google.com/store/apps/details?id=moe.shizuku.privileged.api&hl=en&gl=US) on your Android device.
2. [Enable the Developer options](https://technastic.com/developer-options-android/) on your device.
3. Open Shizuku and tap the **Pairing** button under the ‘Start via Wireless debugging’ section.[![pairing option in shizuku](https://technastic.com/wp-content/uploads/2024/04/pairing-option-in-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/04/pairing-option-in-shizuku.jpg)
4. Shizuku will request notification permission. To grant it, tap **Notification options** and allow notifications for Shizuku.[![allow notifications permission to shizuku](https://technastic.com/wp-content/uploads/2024/04/allow-notifications-permission-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/04/allow-notifications-permission-shizuku.jpg)
5. Having allowed notifications, tap the back button on the navigation bar and select **Developer options**.[![developer options in shizuku](https://technastic.com/wp-content/uploads/2024/04/developer-options-shizuku-android.jpg)](https://technastic.com/wp-content/uploads/2024/04/developer-options-shizuku-android.jpg)
6. Go to the **Debugging** section, tap **Wireless Debugging,** and enable the feature. Next, select the **Pair device with pairing code** option.[![pair shizuku with pairing code via wireless debugging](https://technastic.com/wp-content/uploads/2020/11/pair-shizuku-via-wireless-debugging.jpg)](https://technastic.com/wp-content/uploads/2020/11/pair-shizuku-via-wireless-debugging.jpg)
7. A pop-up with a pairing code will appear, and you’ll receive a notification from Shizuku requesting to enter the 6-digit code.[![enter wireless debugging pairing code for shuzuku](https://technastic.com/wp-content/uploads/2024/04/enter-wireless-debugging-pairing-code-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/04/enter-wireless-debugging-pairing-code-shizuku.jpg)
8. Type the Wi-Fi pairing code and tap the **Send** option.
9. In Shizuku, tap the **Start** button. The app will run a script and start the Shizuku service in the background.
10. Exit Shizuku and install **aShell** from the [Play Store](https://play.google.com/store/apps/details?id=in.sunilpaulmathew.ashell&hl=en&gl=US) (paid) or [F-Droid](https://f-droid.org/en/packages/in.sunilpaulmathew.ashell/) (free).
11. Launch aShell and grant it access to Shizuku.[![allow ashell to access shizuku](https://technastic.com/wp-content/uploads/2024/01/allow-shell-access-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/01/allow-shell-access-shizuku.jpg)
12. That’s it! You can now use the aShell command box to execute ADB and Shell commands on your device without root. For instance, to [check the health of your phone’s battery](https://technastic.com/check-battery-health-charge-level-cycle-capacity-adb/), type “ `dumpsys battery` ” and press the **Send** or **Enter** button.[![](https://technastic.com/wp-content/uploads/2020/11/using-adb-command-in-ashell.jpg)](https://technastic.com/wp-content/uploads/2020/11/using-adb-command-in-ashell.jpg)

## 2\. Setting up ADB in Termux (Root)

It’s possible to install ADB and Fastboot on Android by cloning any of the 3 Gits listed below using a terminal emulator like Termux.

1. [ADB Fastboot Termux](https://github.com/freetheorange905/adb-fastboot-termux)
2. [Termux ADB](https://github.com/MasterDevX/Termux-ADB)
3. [Termux ADB Fastboot](https://github.com/rendiix/termux-adb-fastboot)

Now let’s see how you can install ADB and Fastboot on an Android phone or tablet.

1. Download and install [Termux](https://play.google.com/store/apps/details?id=com.termux) from the Play Store.
2. After installing the app, you need to grant Termux **Storage** permission. To do so, go to **Settings > Apps > Termux** and select **Permissions**. Then tap **Storag** e and select **Allow**.[![termux storage permission android](https://technastic.com/wp-content/uploads/2020/12/termux-storage-permissions.jpg)](https://technastic.com/wp-content/uploads/2020/12/termux-storage-permissions.jpg)
3. Now open Termux, type the following and tap the **Enter** key on the keyboard.
	```
	pkg update
	```
4. Now, execute the following command to upgrade Termux packages.
	```
	pkg upgrade
	```
5. Since ADB Fastboot Termux is a Python-based script, we must install Python on the Android device. Issue the following command in Termux.
	```
	pkg install python
	```
	[![install python on android via termux](https://technastic.com/wp-content/uploads/2020/12/termux-install-python.jpg)](https://technastic.com/wp-content/uploads/2020/12/termux-install-python.jpg)
6. While installing Python on your Android device, you might be prompted to authorize the installation by typing ‘ **Y** ‘ (for Yes).
7. Since we have to clone Git from GitHub, you’ll need to install another package called Git using this command.
	```
	pkg install git
	```
	[![install git and android via termux](https://technastic.com/wp-content/uploads/2020/12/termux-install-git.jpg)](https://technastic.com/wp-content/uploads/2020/12/termux-install-git.jpg)
8. It’s time to clone the ADB Fastboot Termux Git using Termux.
	```
	git clone https://github.com/freetheorange905/adb-fastboot-termux.git
	```
	[![adb fastboot git clone termux android](https://technastic.com/wp-content/uploads/2020/12/adb-fastboot-termux-git.jpg)](https://technastic.com/wp-content/uploads/2020/12/adb-fastboot-termux-git.jpg)
9. Now that the ADB and Fastboot Git have been cloned to your Android device, we need to change the path directory using `cd` as shown below (see the screenshot above).
	```
	cd adb-fastboot-termux
	```
10. Finally, execute the following command in Termux.
	```
	python af.py
	```
11. As soon as you tap the Enter key, a new screen will appear and you will be prompted to type **1** to install ADB and Fastboot on your Android device, and **2** to uninstall them. Type **1** and tap the Enter key.[![adb fastboot installed in termux android](https://technastic.com/wp-content/uploads/2020/12/adb-fastboot-installed-android.jpg)](https://technastic.com/wp-content/uploads/2020/12/adb-fastboot-installed-android.jpg)
12. When ADB and Fastboot are installed, you’ll get a message saying, “ **Tools were successfully installed!**“

You can also install the ADB and Fastboot tools on your Android with a single command that includes all the above commands in one line.

```
pkg update && pkg upgrade && pkg install python && pkg install git && git clone https://github.com/freetheorange905/adb-fastboot-termux.git && cd adb-fastboot-termux && python af.py
```

Having set up ADB and Fastboot on your device via Termux, use the following command to verify if you have done everything as expected.

```
adb
or
adb help
```

As you can see below, you’ll get information such as the Android Debug Bridge version and other ADB options on your phone’s screen.

[![adb command in termux for android](https://technastic.com/wp-content/uploads/2020/12/adb-command-termux.jpg)](https://technastic.com/wp-content/uploads/2020/12/adb-command-termux.jpg)

Please note that if you run the `adb devices` command, you won’t get any device ID under the list of devices attached because your Android device will now act like an ADB/Fastboot host.

[![adb devices command on android device via termux](https://technastic.com/wp-content/uploads/2020/12/adb-devices-command-termux.jpg)](https://technastic.com/wp-content/uploads/2020/12/adb-devices-command-termux.jpg)

Please note that to use ADB, your host Android device needs to be rooted, as it can be done using a Magisk module called **ADB & Fastboot for Android NDK**.

## 3\. Using ADB Commands via Web ADB

Recently, a developer named Yume Chan launched a website that lets us use [ADB on Android via Chrome](https://technastic.com/webadb-adb-commands-web-browser/), Opera, and Microsoft Edge browsers. It means we no longer need a rooted Android device to use ADB. WebADB makes use of the WebUSB API found in all Chromium-based desktop and mobile browsers.

WebADB lets you send ADB commands from one Android device to another, mirror the screen, and control the other device, install APKs, browse the files on the other device, capture screenshots, etc.

**Prerequisites**

- Two Android devices (phone or tablet).
- A USB OTG or a USB Type-C to a USB Type-C cable.[![USB OTG and USB Type-C to Type-C cable](https://technastic.com/wp-content/uploads/2020/12/usb-otg-usb-ctype-cable.jpg)](https://technastic.com/wp-content/uploads/2020/12/usb-otg-usb-ctype-cable.jpg)
- Enable USB debugging on the Android device you want to send ADB commands.

Let’s see how to use Web ADB to run ADB commands on Android devices without root. You can use one of two Android devices as a host to perform ADB commands on the other device.

1. Open the [Web ADB website](https://app.webadb.com/#/) on the Android device you want to use as a host.
2. Tap the **3-dot icon** in the Chrome browser and enable the **Desktop site** option.[![enable desktop site option in chrome for android](https://technastic.com/wp-content/uploads/2020/12/desktop-site-chrome-android.jpg)](https://technastic.com/wp-content/uploads/2020/12/desktop-site-chrome-android.jpg)
3. Insert the USB OTG or the USB Type-C cable into the device you want to use as a host. Now, plug the other end of the USB cable into the client Android device you want to send the command to.
4. Tap the **Add Device** option on the WebADB website. Select your device in the pop-up window and tap the **Connect** button.[![select android device in web adb](https://technastic.com/wp-content/uploads/2020/11/connect-adb-device.jpg)](https://technastic.com/wp-content/uploads/2020/11/connect-adb-device.jpg)
5. Tap **OK** when the browser asks to grant access to your connected device.[![grant usb adb connection on chrome for android](https://technastic.com/wp-content/uploads/2020/11/adb-access-to-chrome.jpg)](https://technastic.com/wp-content/uploads/2020/11/adb-access-to-chrome.jpg)
6. At this point, you will receive a notification on your second device asking you to **Allow USB debugging**. Tap on **Allow**.[![allow usb debugging on computer](https://technastic.com/wp-content/uploads/2020/07/allow-usb-debugging-on-pc.jpg)](https://technastic.com/wp-content/uploads/2020/07/allow-usb-debugging-on-pc.jpg)
7. You’ll see your device’s codename in the WebADB command box. It means that both devices have been appropriately connected for ADB operations.[![android devices connected via adb](https://technastic.com/wp-content/uploads/2020/11/adb-connected.jpg)](https://technastic.com/wp-content/uploads/2020/11/adb-connected.jpg)
8. You’re all set to use ADB commands to control the connected Android device. Don’t forget to omit “adb” and “adb shell” while executing commands on a computer. For example, if you want to reboot the connected Android phone or tablet into the bootloader mode, you should use `reboot bootloader` and tap Enter on the keyboard.[![adb reboot bootloader comand](https://technastic.com/wp-content/uploads/2020/11/adb-reboot-bootloader.jpg)](https://technastic.com/wp-content/uploads/2020/11/adb-reboot-bootloader.jpg)

You can execute any other ADB command on your Android device without a laptop or PC, without rooting your device.