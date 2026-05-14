---
title: ADB Commands for Battery Optimization on Android
source: https://technastic.com/adb-battery-optimization-commands/
author:
  - "[[Rakesh Shukla]]"
published: 2024-09-17
created: 2026-05-14
description: Extend the battery life of your Android phone with ADB commands. Learn how to optimize your phone's battery for longer-lasting performance.
tags:
  - adb
---
adbSmartphones have become extensions of ourselves. We spend hours juggling apps, checking notifications, making and receiving calls, surfing the web, playing games, and watching OTTs. With this level of engagement with our phones, the battery life can often feel like a ticking clock. You can [tweak your Android phone settings for longer battery life](https://technastic.com/samsung-battery-saving-tips-one-ui/). However, if you want to achieve pro-level battery optimization, we’ve compiled a list of ADB commands that allow users to fine-tune advanced settings for longer battery performance.

Recently, we published a detailed listicle of [ADB commands to improve performance](https://technastic.com/adb-commands-improve-performance-android/) and speed up Android phones. This guide will introduce you to essential ADB commands specifically designed for battery optimization.

You must [set up Android SDK Platform Tools](https://technastic.com/android-sdk-platform-tools-download/) on your computer to run ADB commands. If you don’t have a PC, you can [use aShell to execute commands on your Android device](https://technastic.com/run-adb-commands-android-without-pc/).

Table of Content

## ADB Commands to Optimize Battery

If your phone is older than 2 years, [check the status and health of the battery](https://technastic.com/check-battery-health-charge-level-cycle-capacity-adb/). Battery performance usually degrades over time. Now, let’s check out the battery optimization commands. With each command executed thoughtfully, you’ll notice positive changes in how long your device lasts on a single charge.

### 1\. Enable Battery Saver Mode

It’s easy to enable battery saver mode on Android through ADB. You only need to enter the command prompt or terminal command mentioned below.

```
adb shell settings put global low_power 1
```

This will turn on the battery-saver mode which limits background processes, reduces screen brightness, and restricts certain features to reduce the overall resource consumption of your device.

Here are two ADB commands to extend battery life without sacrificing device performance.

```
adb shell settings put global automatic_power_save_mode 1
```

```
adb shell settings put global dynamic_power_savings_enabled 1
```

### 2\. Disable UI Animation and Transition Effects

Animations and transition effects may look visually appealing, but they also drain your device’s battery. To disable animations through ADB, execute the following commands.

Window Animation Scale is a visual effect when opening or closing an app on your Android device. Disabling this animation can make a noticeable difference in your device’s speed.

```
adb shell settings put global window_animation_scale 0.0
```

Transition Animation Scale controls the animation when switching between apps on your device.

```
adb shell settings put global transition_animation_scale 0.0
```

Animator Duration Scale governs how long an animation plays on your screen before transitioning to another state.

```
adb shell settings put global animator_duration_scale 0.0
```

You can also lower UI animation scales or completely disable them from the [Developer Options](https://technastic.com/developer-options-android/) in Android settings.

### 3\. Restrict Background Apps and Processes

[Apps and processes running in the background](https://technastic.com/check-background-apps-and-processes-via-adb/) consume battery juice even when you are not actively using them. The following command lets you check and analyze which apps consume a significant chunk of your phone’s battery.

```
adb shell dumpsys batterystats
```

Similarly, you can also check the battery usage stats for a specific app.

```
adb shell dumpsys batterystats --charged <app-package-name>
```

Several system apps on Android phones have permission to bypass battery optimizations. Use the following command to print the list of whitelisted apps.

```
adb shell dumpsys deviceidle
```

[![adb shell dumpsys deviceidle command](https://technastic.com/wp-content/uploads/2024/03/white-list-apps-android-adb.png)](https://technastic.com/wp-content/uploads/2024/03/white-list-apps-android-adb.png)

Once you have the whitelisted apps, note down the [app package names](https://technastic.com/app-package-name-android/) of the app you want to move to the battery optimization list. Then use the following command.

```
adb shell dumpsys deviceidle sys-whitelist -<package-name>
```

[![enable or disable device idle apps in whitelist using adb](https://technastic.com/wp-content/uploads/2024/03/remove-restore-app-battery-whitelist-adb.png)](https://technastic.com/wp-content/uploads/2024/03/remove-restore-app-battery-whitelist-adb.png)

You can also use the following commands to kill or stop a battery-hogging app or process using ADB.

```
adb shell am force-stop <package-name>
```

```
adb shell am kill <package-name>
```

You can restrict background data usage through ADB by entering this command: adb shell pm restrict-background <package-name>. Replace <package-name> with the app name you want to restrict from using background data.

### 4\. Uninstall Unused System Apps

Bloatware refers to pre-installed apps that you may not use but still run in the background and drain your battery. Through ADB, you can uninstall, freeze, or disable bloatware using the commands.

Uninstall the apps you want to remove.

```
pm uninstall --user 0 <package-name>
```

[![uninstall android app using adb command](https://technastic.com/wp-content/uploads/2024/02/uninstall-android-app-adb-command.png)](https://technastic.com/wp-content/uploads/2024/02/uninstall-android-app-adb-command.png)

Freeze an app running in the background.

```
adb shell cmd appops set <package-name> RUN_IN_BACKGROUND ignore
```

Disable a system app.

```
adb shell pm disable-user --user 0 <package-name>
```

### 5\. Disable Performance Mode

Fixed-performance mode clocks the CPU and GPU with an upper and lower bound. However, faster performance comes at the cost of faster battery drain. You can turn off performance mode on your device to enjoy better battery life.

```
adb shell cmd power set-fixed-performance-mode-enabled false
```

Overclocking boosts clock speed, allowing apps to run faster and enhancing gaming experiences. However, it may cause overheating and drain the battery quickly.

### 6\. Decrease Screen Refresh Rate and Window Blur Effect

ADB also lets you adjust the screen refresh rate and window blur animation, which can improve the battery life on Android devices.

```
adb shell settings put secure user_refresh_rate 90
```

```
adb shell settings put system peak_refresh_rate 90
```

```
adb shell settings put system min_refresh_rate 90
```

```
adb shell settings put global disable_window_blurs 0
```

### 7\. Adjust Screen Brightness

Brightness settings play a crucial role in battery consumption. Reducing the screen brightness can extend battery life throughout the day. The following ADB command will enable Auto-brightness.

```
adb shell settings put system screen_auto_brightness_adj 1.0
```

### 8\. Lower Screen Resolution and Density

Most Android phones support up to three screen resolutions. Using the highest supported resolution may produce sharp visuals, but it drains the battery faster. For example, the Samsung Galaxy S4 Ultra offers HD+ (720 x 1560 px), FHD+ (1080 x 2340 px), and QHD+ (1440 x 3120 px) resolution. You can switch to FHD+ for good picture quality while enjoying great battery life.

You can use the commands below to change the screen resolution and density via ADB.

```
adb shell wm size 1080x2340
```

```
adb shell wm density 390
```

Having executed the commands, reboot your device.

```
adb reboot
```

### 9\. Disable Motion and Gestures

Android devices come with sensors like gyroscope, proximity, and ambient light. These sensors facilitate features like double tap to wake or sleep, ambient light, doze mode, etc., but consume power even when idle. Turning off those sensors reduces power drain effectively.

```
adb shell settings put system master_motion 0
```

```
adb shell settings put system motion_engine 0
```

```
adb shell settings put system air_motion_engine 0
```

```
adb shell settings put system air_motion_wake_up 0
```

```
adb shell settings put global ambient_enabled 0
```

```
adb shell settings put global ambient_touch_to_wake 0
```

```
adb shell settings put secure aware_enabled 0
```

```
adb shell settings put secure doze_enabled 0
```

```
adb shell settings put secure double_tap_to_sleep 0
```

```
adb shell settings put secure double_tap_to_wake 0
```

```
adb shell settings put secure wake_gesture_enabled 0
```

### 10\. Disable Nearby Devices and Network Scanning

Connectivity features like Wi-Fi, Bluetooth, and networks are at the core of the smartphone experience. Smartphones constantly search for available devices and networks to connect to. You can disable the scanning feature and enable Wi-Fi power-saving mode to stop the battery from draining.

```
adb shell settings put system nearby_scanning_permission_allowed 0
```

```
adb shell settings put system nearby_scanning_enabled 0
```

```
adb shell settings put global ble_scan_always_enabled 0
```

```
adb shell settings put global wifi_power_save 1
```

### 11\. Power Management Commands

If you’re into smartphone gaming, you might want to throttle the CPU and GPU for a better experience. However, keeping the CPU clock at a moderate level can save the battery without making the device slow. Besides, you can turn on adaptive battery management and app restrictions to limit app activity on your phone.

```
adb shell settings put global sem_enhanced_cpu_responsiveness 0
```

```
adb shell settings put global enhanced_processing 0
```

```
adb shell settings put global app_standby_enabled 1
```

```
adb shell settings put global adaptive_battery_management_enabled 1
```

```
adb shell settings put global app_restriction_enabled true
```

### 12\. Force Sleep Mode

The Sleep Mode feature on Android stops most background activities when the device is not in use to prevent battery drain. Forcing Sleep Mode via ADB will get you some extra battery juice.

```
adb shell dumpsys deviceidle force-idle
```

```
adb shell dumpsys deviceidle enable
```

```
adb shell settings put system intelligent_sleep_mode 1
```

```
adb shell settings put secure adaptive_sleep 1
```

This will activate the Sleep Mode, which will remain active until you disable it.

### 13\. Disable Lift to Wake Screen and AOD

The Always-on display feature displays time and notifications, but consumes battery to work. Similarly, many users use the lift-to-wake feature for faster access to the fingerprint sensor and time. Disabling these features will give you a longer battery backup. Here are the ADB commands to do that.

```
adb shell settings put secure doze_quick_pickup_gesture 0
```

```
adb shell settings put system lift_to_wake 0
```

### 14\. Force Battery Optimization

If you have enabled battery optimizations on your Android phone but feel that they aren’t working for some or all apps, you can force the optimizations with an ADB command.

```
adb shell cmd package bg-dexopt-job
```

Please remember that the battery optimization service might take around 30 minutes to 2 hours to finish. When complete, don’t forget to reboot your device. Also, you’ll need to rerun the command if you receive a new OTA update after forcing the battery optimizations.