______________________________________________________________________

title: "3 Ways to Run ADB Commands on Android without PC or Root"
source: "https://technastic.com/run-adb-commands-android-without-pc/"
author:

- "\[[Rakesh Shukla]\]"
  published: 2025-05-18
  created: 2026-05-14
  description: "Using a Shizuku app aShell and terminal app Termux, we can use ADB and Shell commands on Android devices without root or a computer."
  tags:
- "adb"

______________________________________________________________________

Do you need to use an ADB command on your Android phone or tablet to perform a task, but don’t have access to a computer? Earlier, it was impossible to run commands on an Android device itself without superuser permissions. Thankfully, Terminal emulator apps like aShell (Shizuku) and Termux allow you to use ADB natively. This tutorial will explore different methods to run ADB on Android devices without root, including Termux, aShell, and WebADB.

Let’s check out different methods to harness the power of ADB on Android devices without a PC.

Table of Content

## 1. Using Shizuku-supported aShell App

Shizuku acquires system APIs and permissions through wireless debugging and passes them to supported apps. Unlike other apps that require root privileges to modify Android devices, Shizuku leverages certain [Android permissions](https://technastic.com/all-special-dangerous-android-permissions/). You can use the [Shizuku-supported apps](https://technastic.com/best-shizuku-apps-mods-android/) to do amazing things without rooting your device. Besides modifying, tweaking, and customizing your Android phone, Shizuku also makes it possible to use ADB on Android devices without root.

1. Download and install [Shizuku](https://play.google.com/store/apps/details?id=moe.shizuku.privileged.api&hl=en&gl=US) on your Android device.
1. [Enable the Developer options](https://technastic.com/developer-options-android/) on your device.
1. Open Shizuku and tap the **Pairing** button under the ‘Start via Wireless debugging’ section.[![pairing option in shizuku](https://technastic.com/wp-content/uploads/2024/04/pairing-option-in-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/04/pairing-option-in-shizuku.jpg)
1. Shizuku will request notification permission. To grant it, tap **Notification options** and allow notifications for Shizuku.[![allow notifications permission to shizuku](https://technastic.com/wp-content/uploads/2024/04/allow-notifications-permission-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/04/allow-notifications-permission-shizuku.jpg)
1. Having allowed notifications, tap the back button on the navigation bar and select **Developer options**.[![developer options in shizuku](https://technastic.com/wp-content/uploads/2024/04/developer-options-shizuku-android.jpg)](https://technastic.com/wp-content/uploads/2024/04/developer-options-shizuku-android.jpg)
1. Go to the **Debugging** section, tap **Wireless Debugging,** and enable the feature. Next, select the **Pair device with pairing code** option.[![pair shizuku with pairing code via wireless debugging](https://technastic.com/wp-content/uploads/2020/11/pair-shizuku-via-wireless-debugging.jpg)](https://technastic.com/wp-content/uploads/2020/11/pair-shizuku-via-wireless-debugging.jpg)
1. A pop-up with a pairing code will appear, and you’ll receive a notification from Shizuku requesting to enter the 6-digit code.[![enter wireless debugging pairing code for shuzuku](https://technastic.com/wp-content/uploads/2024/04/enter-wireless-debugging-pairing-code-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/04/enter-wireless-debugging-pairing-code-shizuku.jpg)
1. Type the Wi-Fi pairing code and tap the **Send** option.
1. In Shizuku, tap the **Start** button. The app will run a script and start the Shizuku service in the background.
1. Exit Shizuku and install **aShell** from the [Play Store](https://play.google.com/store/apps/details?id=in.sunilpaulmathew.ashell&hl=en&gl=US) (paid) or [F-Droid](https://f-droid.org/en/packages/in.sunilpaulmathew.ashell/) (free).
1. Launch aShell and grant it access to Shizuku.[![allow ashell to access shizuku](https://technastic.com/wp-content/uploads/2024/01/allow-shell-access-shizuku.jpg)](https://technastic.com/wp-content/uploads/2024/01/allow-shell-access-shizuku.jpg)
1. That’s it! You can now use the aShell command box to execute ADB and Shell commands on your device without root. For instance, to [check the health of your phone’s battery](https://technastic.com/check-battery-health-charge-level-cycle-capacity-adb/), type “ `dumpsys battery` ” and press the **Send** or **Enter** button.[![](https://technastic.com/wp-content/uploads/2020/11/using-adb-command-in-ashell.jpg)](https://technastic.com/wp-content/uploads/2020/11/using-adb-command-in-ashell.jpg)

## 2. Setting up ADB in Termux (Root)

It’s possible to install ADB and Fastboot on Android by cloning any of the 3 Gits listed below using a terminal emulator like Termux.

1. [ADB Fastboot Termux](https://github.com/freetheorange905/adb-fastboot-termux)
1. [Termux ADB](https://github.com/MasterDevX/Termux-ADB)
1. [Termux ADB Fastboot](https://github.com/rendiix/termux-adb-fastboot)

Now let’s see how you can install ADB and Fastboot on an Android phone or tablet.

1. Download and install [Termux](https://play.google.com/store/apps/details?id=com.termux) from the Play Store.
1. After installing the app, you need to grant Termux **Storage** permission. To do so, go to **Settings > Apps > Termux** and select **Permissions**. Then tap **Storag** e and select **Allow**.[![termux storage permission android](https://technastic.com/wp-content/uploads/2020/12/termux-storage-permissions.jpg)](https://technastic.com/wp-content/uploads/2020/12/termux-storage-permissions.jpg)
1. Now open Termux, type the following and tap the **Enter** key on the keyboard.
   ```
   pkg update
   ```
1. Now, execute the following command to upgrade Termux packages.
   ```
   pkg upgrade
   ```
1. Since ADB Fastboot Termux is a Python-based script, we must install Python on the Android device. Issue the following command in Termux.
   ```
   pkg install python
   ```
   [![INSTALL PYTHON ON ANDROID VIA TERMUX]
