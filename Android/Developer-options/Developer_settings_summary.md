---
Developer settings: Summary of Developer settings
tags:
  - Android
  - guide
source: https://youtu.be/JkV78G4UXDM?si=Gz2mfxk_Uyu5C1z-
---

Here's a summary of the video "Every Android Setting in the Developer Options Explained!"

## Developer Options Explained

The Android Developer Options menu is a hidden treasure trove of advanced settings and features not typically accessible to regular users. It offers powerful customization and debugging tools for developers and advanced users to enhance their smartphone experience, troubleshoot issues, and unlock new functionalities.

## How to Enable Developer Options (2:07)

To enable Developer Options:
1.  Go to System Settings.
2.  Scroll down and tap on "About Phone."
3.  Find "Build Number" and tap it seven times.
4.  Confirm your passcode if prompted.
5.  A toast message will confirm, "You're now a developer!"
6.  Navigate back to System settings, and "Developer Options" will appear.

*(Note: The exact location and available toggles may vary based on Android version and device manufacturer. This video uses a Google Pixel 5 running Android 12 Beta 4 for demonstration.)*

## General Settings (First Section of Settings) (2:52)

*   **Memory**: Provides statistics on phone memory usage over various periods (3, 6, 12, or 24 hours) and shows which apps consume the most memory. Useful for identifying memory-leaching apps.
*   **Running Services**: Shows apps and services actively running in the background, allowing users to terminate services consuming too much memory in real-time.
*   **Bug Report**: Captures system logs and activity to help developers diagnose app or system interface issues. Can be configured to appear in the power menu for easy access.
*   **Verbose Vendored Logging**: Adds device-specific vendor information (e.g., Samsung, OnePlus, Google) to bug reports, assisting developers further.
*   **Bug Report Handler**: Allows choosing a specific app to handle bug reports (e.g., Android Beta Feedback app for reporting directly to Google).
*   **Desktop Backup Password**: Encrypts full desktop backups created using ADB commands.
*   **Stay Awake**: Keeps the phone screen on indefinitely while charging until manually locked.
*   **Enable Bluetooth HCI Snoop Log**: Creates a log of Bluetooth usage over time, primarily for developers.
*   **OEM Unlocking**: A critical setting that allows unlocking the bootloader via an ADB command, opening possibilities for rooting, installing custom ROMs, and Magisk modules for advanced modifications.
*   **WebView Implementation**: Allows users to choose a different WebView app for in-app browsers. Default Android System WebView is generally sufficient.
*   **Advanced Reboot**: (For rooted devices) Adds options to quickly reboot into recovery or bootloader from the power menu.
*   **Automatic System Updates**: Automatically applies available software updates upon phone restart.
*   **DSU Loader**: (For developers) Allows installing the latest Generic System Image (GSI) from Google without ADB/Fastboot commands for app testing on stock Android.
*   **System UI Demo Mode**: Cleans up the status bar by removing notification icons, setting the time to a consistent value, and displaying 100% battery, useful for screen recordings or presentations.
*   **Quick Settings Developer Tiles**: Adds quick toggles for developer options in the quick settings panel. Useful toggles include:
    *   **Sensors Off**: Disables almost all phone sensors (cameras, GPS, microphone) for privacy.
    *   **Wireless Debugging**: Allows connecting the phone to a command prompt wirelessly for ADB commands, enabling app installations, reboots, etc., without a cable (requires both devices on the same Wi-Fi network).
*   **Revoke USB Debugging Authorizations**: Revokes all previously granted USB debugging access to computers, requiring re-authorization for security.
*   **Disable ADB Authorization Timeout**: Prevents ADB authorizations from automatically revoking after seven days of inactivity.

## Debugging (10:03)

*   **Select Mock Location App**: Allows spoofing your current location using a fake GPS app.
*   **Forceful GNSS Measurements**: For developers, continuously tracks satellites for accurate position calculation in apps.
*   **Enable View Attribute Inspection**: Helps developers debug app UI elements.
*   **Select Debug App / Wait for Debugger**: Tools for app developers to debug their applications without complex ADB commands.
*   **Verify Apps Over USB**: Google scans apps installed via USB through ADB for malicious content. Disabling this is only recommended if you trust the app's source.
*   **Verify Bytecode of Debuggable Apps**: Android's runtime verifies the bytecode of installed apps for security.
*   **Logger Buffer Sizes**: Adjusts the buffer size for audio recording. (Generally not recommended for average users).
*   **Feature Flags**: Experimental features (like Chrome flags) for enabling/disabling new Android OS functionalities being tested by Google.
*   **GPU Debug Layers**: For game developers to debug graphics rendering.
*   **Graphics Driver Preferences**: Allows selecting a specific graphics driver per app/game to potentially improve gaming performance (e.g., using "System graphics driver" if a phone lacks a dedicated gaming mode).
*   **App Compatibility Changes**: (Android 11+) Simplifies toggling new platform behavior changes for app developers, saving time from typing ADB commands.

## Networking (14:30)

*   **Wireless Display Certification**: Useful for devices supporting MirrorCast displays.
*   **Wi-Fi Verbose Logging**: Provides detailed logs of Wi-Fi connections and signal strength.
*   **Wi-Fi Scan Throttling**: Saves battery and improves network performance by limiting how often apps can scan for Wi-Fi. (Foreground apps: 4 scans/2 mins; background apps: 1 scan/30 mins). Keep this on.
*   **Wi-Fi Non-Persistent MAC Randomization**: Changes the device's MAC address each time it connects to a Wi-Fi network for privacy reasons. (Recommended to enable).
*   **Mobile Data Always Active**: Keeps the mobile data connection active even when on Wi-Fi for faster network switching. This is a significant battery drain. (Recommended to turn off unless you rely on MMS in the US, as turning it off might prevent MMS send/receive on Wi-Fi).
*   **Tethering Hardware Acceleration**: On supported devices/networks, uses hardware instead of software for tethering, saving battery. (Enable if your device supports it, though compatibility may vary).
*   **Show Bluetooth Devices Without Names**: Displays Bluetooth devices with only MAC addresses, which are usually hidden. Useful for finding elusive devices.
*   **Disable Absolute Volume**: Separates the volume control between the phone and the Bluetooth device, useful for overly loud speakers or finer volume adjustments.
*   **Enable Gabeldorsche**: Enables Google's new Bluetooth stack for improved security and reliability. (Currently experimental, leave off unless instructed).
*   **Bluetooth Debugging Options (A2DP Hardware Offload, AVRCP Version, MAP Version)**: These are last-resort options for troubleshooting widespread Bluetooth issues, usually only occurring with alpha/beta software or newly released phones. Reboot after each change.
*   **Bluetooth Audio Codec**: Allows selecting a higher quality audio profile for Bluetooth devices (e.g., AAC for good quality, Qualcomm aptX HD for even better, LDAC for highest quality). SBC is the lowest quality.
*   **Sampling Rate, Audio Bits, Channel Mode**: (If supported by headphones) Allows further customization of audio quality for Bluetooth.

## Input (19:30)

*   **Show Taps**: Displays a visual indicator on the screen where you tap, useful for screen recordings.
*   **Pointer Location**: Draws a tracer line showing precise swipe paths, mainly for developers.

## Drawing (19:47)

*   **Show Surface Updates**: Flashes parts of the screen rapidly to show developers which parts of their app are actively rendering.
*   **Show Layout Bounds**: Clearly marks borders, clip bounds, margins, etc., for app developers to validate UI positioning and alignment.
*   **Force RTL Layout Direction**: Flips the entire screen layout from right-to-left. (Could be a fun prank).
*   **Window Animation Scale, Transition Animation Scale, Animator Duration Scale**: These three are popular settings to speed up or slow down UI animations. Setting them to 0.5x or 0x can make the phone feel faster.
*   **Simulate Secondary Displays**: Enables a second virtual screen with chosen resolution, for developers to test app appearance on different screen sizes.
*   **Smallest Width (DP)**: Changes the density-independent pixels (dp) of the display, making everything on the screen smaller or larger.
*   **Display Cutout**: Adjusts how the system handles screen notches or hole punches, helping developers ensure app compatibility.

## Hardware Accelerated Rendering (21:18)

*   **Show View Updates**: Flashes parts of the screen red when the GPU operates an object, helping game developers optimize.
*   **Show Hardware Layers Updates**: Flashes green when updates are made to hardware layers, indicating areas that could be optimized.
*   **Debug GPU Overdraw**: Color-codes areas of the screen that are drawn over multiple times, helping developers reduce unnecessary rendering layers for better performance.
*   **Override Force Dark**: Forces most apps without native dark mode to have one. (One of the top three favorite toggles).
*   **Force 4x MSAA**: For gamers, improves graphics and visual experience but consumes significant performance and battery. (Not recommended for competitive gaming where performance is key).
*   **Disable Hardware Overlays**: Forces apps to constantly check for collisions and clipping without hardware assistance, costing more CPU power. (Leave off).
*   **Simulate Color Space**: Allows developers to see how their apps look to colorblind users or to turn the screen black and white.

## Media (22:59)

*   **Disable USB Audio Routing**: Disables automatic audio routing to USB audio peripherals.
*   **Configure Transcoding**: Configures options for when sound or video gets transcoded.

## Monitoring (23:16)

*   **Strict Mode Enabled**: Flashes the screen when apps take longer than usual to perform operations, indicating potential battery drain or performance issues.
*   **Profile HWUI Rendering**: Displays a real-time graph of GPU activity, showing how the GPU performs during app animations and operations.

## Apps (23:42)

*   **Don't Keep Activities**: Force closes every app you leave. Good for privacy, but terrible for battery life and performance as the CPU constantly re-opens apps from scratch. (Highly suggested to leave off).
*   **Background Process Limit**: Allows choosing how many apps or processes can run in the background. (Default is usually best, setting it too low can hinder multitasking).
*   **Background Check**: Helps identify misbehaving apps that prevent the phone from going into deep sleep, allowing you to stop them.
*   **Always Show Crash Dialogue**: Brings back the crash window dialogue for frozen apps, allowing you to choose between closing or waiting, instead of automatically crashing the app.
*   **Show Background ANRs**: For apps crashing in the background, displays a dialogue.
*   **Suspend Execution for Cached Apps**: Freezes cached apps so they don't consume CPU cycles, reducing power consumption. (Recommended to enable).
*   **Notification Channel Warnings**: For developers to ensure proper notification display.
*   **Reset Notification Importance**: Resets the prioritization of notifications.
*   **Standby Apps**: Allows categorizing apps into five groups (Active, Working Set, Frequent, Rare, Restricted) to control their background activity and resource usage. The OS generally manages this automatically based on usage, but manual modification is possible.
    *   **Active**: No restrictions (e.g., messaging, phone apps).
    *   **Working Set**: Medium restrictions, apps function as usual (e.g., Google Maps, Chrome).
    *   **Frequent**: Stronger restrictions but still able to run (e.g., some games).
    *   **Rare**: Strict rules, limited background activity, no internet access in background.
    *   **Restricted**: Cannot run or do anything in the background.
*   **Force Allow Apps on External**: Forces apps to be storable on an SD card, saving internal memory space.
*   **Enable Freeform Windows**: Allows apps to become floating windows on Android. (Difficult to resize, cannot open multiple freeform apps simultaneously, mostly a cool but impractical feature).
*   **Force Desktop Mode**: Enables a desktop-like experience on an external monitor when connected via a USB-C to HDMI cable. (Requires phones that support DisplayPort Alt Mode, not all phones support this).
*   **Shortcut Manager Rate Limiting**: (For developers) Resets the rate limit for background apps to call shortcut APIs.

## Autofill (28:05)

*   **Login Level (Verbose/Debug)**: Classifies entries in a log file by urgency for autofill service. Verbose provides more detailed information.
*   **Maximum Request/Visible Dataset**: Allows developers to set maximum requests for autofill services and visible datasets.
*   **Reset Values**: Resets autofill values to default.
*   **Shared Data**: Assumed to be data allowed to be shared with private/public servers, but details are unclear.

## Final Thoughts (28:55)

The video concludes by emphasizing that it provides a comprehensive explanation of every Developer Option setting, which is unique. The presenter encourages viewers to like the video and subscribe if they found it helpful and discovered new settings.
