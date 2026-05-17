______________________________________________________________________

title: ADB Commands to Improve Performance on Android
source: https://technastic.com/adb-commands-improve-performance-android/
author:

- "\[[Rakesh Shukla]\]"
  published: 2024-09-08
  created: 2026-05-14
  description: Improve the performance of your Android device with these ADB commands. With ADB you can enjoy a faster, smoother experience.
  tags:
- adb

______________________________________________________________________

Android is a user-friendly OS. However, it is also notorious for sluggish performance and faster battery drain that mar the experience, especially on low and mid-range devices. The good thing is you can tweak your device settings for better performance. If you are comfortable with command-line tools, the ADB commands listed in this article may help you improve the performance of your Android device.

Most Android users who use ADB are familiar with a basic set of commands. However, ADB can perform more advanced tasks like clearing cache, uninstalling bloatware, adjusting system animations, limiting background processes, changing screen refresh rate and resolution, speeding up app launch times, reducing lag, optimizing battery life, etc.

Table of Content

## ADB Commands to Improve Performance

This article will list all ADB commands to tweak advanced settings and enjoy faster load times, smoother multitasking, better battery life, and improved performance. If you don’t know how to set up and use ADB to execute commands, refer to the following tutorials.

- [**Download and Set Up Android SDK Platform Tools**](https://technastic.com/android-sdk-platform-tools-download/)
- [**Run ADB Commands on Android without Root or PC**](https://technastic.com/run-adb-commands-android-without-pc/)

### 1. Adjusting Animation Settings via ADB

Animation settings can significantly impact the responsiveness of your Android device. Standard animation duration may slow down perceived performance. Adjusting these settings makes your phone feel faster and reduces battery consumption.

To adjust animation speeds, navigate through Developer Options on your device. Look for Window Animation Scale, Transition Animation Scale, and Animator Duration Scale. Lowering these values to 0.5x, 0.25x, or turning them off entirely will boost the speed of your device.

[![ANDROID UI ANIMATION SETTINGS DEVELOPER OPTIONS]
#### 1. Window Animation Scale

Window Animation Scale is a visual effect when opening or closing an app on your Android device. Disabling this animation can make a noticeable difference in your device’s speed. The following command will disable the animation completely.

```
adb shell settings put global window_animation_scale 0.0
```

#### 2. Transition Animation Scale

Transition Animation Scale controls the animation when switching between apps on your device. Reducing this will result in a faster transition between apps.

```
adb shell settings put global transition_animation_scale 0.0
```

#### 3. Animator Duration Scale

Animator Duration Scale governs how long an animation plays on your screen before transitioning to another state.

```
adb shell settings put global animator_duration_scale 0.0
```

### 2. Speed up App Launch Time

Optimizing the startup process via ADB can speed up app launches. Try the following commands to speed up your device’s app launch time.

```
adb shell settings put system rakuten_denwa 0
```

```
adb shell settings put system send_security_reports 0
```

```
adb shell settings put secure send_action_app_error 0
```

```
adb shell settings put global activity_starts_logging_enabled 0
```

### 3. Disable Game Optimizing Service (Samsung)

When enabled, the Game Optimizing Service stops Samsung devices from aggressively throttling the CPU and GPU while playing games. While it results in higher frame rates in graphic-intensive games, it also slows down the device’s performance. Thankfully, you can disable GOS on Samsung phones using ADB commands.

```
adb shell settings put secure gamesdk_version 0
```

```
adb shell settings put secure game_home_enable 0
```

```
adb shell settings put secure game_bixby_block 1
```

```
adb shell settings put secure game_auto_temperature_control 0
```

```
adb shell pm clear --user 0 com.samsung.android.game.gos
```

### 4. Clearing App Cache and Data

Regularly [clearing app cache and data](https://technastic.com/clear-cache-android-adb-fastboot-recovery-settings/) ensures your device stays responsive and runs faster. This not only frees up storage space but also helps apps run smoother. The following ADB command takes the desired free space parameter in K/M/G (kilo/mega/gigabytes) and trims caches according to the defined space. So, if you add an insane size in MB or GB, ADB will clear caches until that size is reached. Since the size is never reached, all caches are cleared.

```
adb shell pm trim-caches 128G
```

[![ADB SHELL PM TRIM CACHES COMMAND]
If you want to clear the cache and data for all apps installed on your phone, you should use the following command.

```
adb shell cmd package list packages|cut -d":" -f2|while read package ;do pm clear $package;done
```

You can also clear the system cache on Android devices via [Recovery Mode](https://technastic.com/samsung-recovery-mode/).

### 5. Kill Background Apps and Processes

Background apps and processes significantly impact the performance of Android devices as they stealthily consume system resources and drain the battery. ADB can help you [check the apps running in the background](https://technastic.com/check-background-apps-and-processes-via-adb/) and kill them using commands. Fewer processes mean less strain on your processor and RAM.

Executing `adb shell ps` will give you a list of all running apps and processes with their PIDs. Similarly, you can sort top processes by their memory and CPU consumption

**Memory usage**: `adb shell top -s 6`

**CPU usage**: `adb shell top -s 9`

Once you have the PID, use the following command to kill a process by PID.

```
adb shell kill <PID>
```

[![ADB COMMAND TO GET TOP ACTIVITY AND KILL THE PROCESS]
### 6. Adjust the Refresh Rate, Window Blur, and Transparency

Adjusting screen refresh rate, window blur animation, and transparency can significantly impact your Android device’s performance. You can enhance the performance of your device with the following ADB commands.

```
adb shell settings put system peak_refresh_rate 120.0
```

```
adb shell settings put system min_refresh_rate 120.0
```

```
adb shell settings put global disable_window_blurs 1
```

```
adb shell settings put global accessibility_reduce_transparency 1
```

### 7. Uninstall, Disable, and Freeze Bloatware

Android apps come preloaded with several unwanted apps that clutter the home and app screens, take up storage, and drain resources. [Uninstalling bloatware on your Android device](https://technastic.com/freeze-uninstall-system-apps-android/) will free up RAM and reduce background processes to improve performance. Tools like [ADB AppControl](https://technastic.com/adb-app-control-extended-android/) and [Universal Android debloater](https://technastic.com/universal-android-debloater-best-bloatware-remover/) can help you remove system apps safely but you can also do that using ADB commands.

Execute this command to uninstall the apps you want to uninstall.

```
pm uninstall --user 0 <package-name>
```

[![UNINSTALL ANDROID APP USING ADB COMMAND]
The following command will freeze an app running in the background.

```
adb shell cmd appops set <package-name> RUN_IN_BACKGROUND ignore
```

To disable a system app, use the following command.

```
adb shell pm disable-user --user 0 <package-name>
```

### 8. Enable Fixed Performance Mode

Fixed-performance mode clocks the CPU and GPU with an upper and lower bound. Enabling the feature disables thermal throttling without root and improves the performance on Android devices.

```
adb shell cmd power set-fixed-performance-mode-enabled true
```

Overclocking boosts clock speed, allowing apps to run faster and enhancing gaming experiences. However, it may cause overheating and drain the battery quickly.

### 9. Disable RAM Plus

Disabling RAM Plus not only improves the performance but also saves battery.

```
adb shell settings put global zram_enabled 0
```

```
adb shell settings put global ram_expand_size_list 0
```

### 10. Improve Audio Quality

Modern smartphones provide great audio quality, which can be further enhanced with the help of equalizer apps. However, you can also enjoy a [better audio experience on Android phones](https://technastic.com/set-up-equalizer-apps-on-android/) by enabling K2HD and Tube Amp effects via ADB.

```
adb shell settings put system k2hd_effect 1
```

```
adb shell settings put system tube_amp_effect 1
```

### 11. Improve Touchscreen Latency and Response Time

A longer touch-and-hold delay means you need to keep your finger on the screen longer before it registers as an input. You can adjust the long-press delay timeout for faster touch response on Android phones and tablets. Try the following commands.

```
adb shell settings put secure long_press_timeout 250
```

```
adb shell settings put secure multi_press_timeout 250
```

```
adb shell settings put secure tap_duration_threshold 0.0
```

```
adb shell settings put secure touch_blocking_period 0.0
```

### 12. Optimize System Performance

Finally, here are some ADB commands to unleash the full potential of the CPU and GPU

```
adb shell setprop debug.force-opengl 1
```

```
adb shell setprop debug.hwc.force_gpu_vsync
```

```
adb shell settings put global ram_expand_size 0 default
```

```
adb shell settings put system multicore_packet_scheduler 1
```

If you want your phone’s processor to spike to the peak speed without sacrificing the optimized mode, try the following ADB command.

```
adb shell settings put global sem_enhanced_cpu_responsiveness 1
```

### 13. Enable/Disable Private DNS

Keeping the private DNS feature enabled or disabled on your phone is a matter of personal preference. While the standard DNS isn’t encrypted, private DNS queries are encrypted. It enhances privacy and security while using a network.

You can use the following ADB commands to enable or disable private DNS on your phone.

```
adb shell settings put global private_dns_mode off
```

Similarly, you can enable private DNS with the hostname.

```
adb shell settings put global private_dns_specifier dns.adguard.com
```

### 14. Improve Network Performance

Android devices keep scanning for devices and networks in the background by default. Using the following command will reduce stress on your phone’s system resources and battery and thus speed up its performance.

```
adb shell settings put global wifi_power_save 0
```

```
adb shell settings put global enable_cellular_on_boot 1
```

```
adb shell settings put global mobile_data_always_on 0
```

```
adb shell settings put global tether_offload_disabled 0
```

```
adb shell settings put global ble_scan_always_enabled 0
```

```
adb shell settings put global network_scoring_ui_enabled 0
```

```
adb shell settings put global network_recommendations_enabled 0
```

### 15. Power Management Tweaks

Finally, here are some [ADB commands to optimize battery](https://technastic.com/adb-battery-optimization-commands/) on Android devices.

```
adb shell settings put system intelligent_sleep_mode 0
```

```
adb shell settings put secure adaptive_sleep 0
```

```
adb shell settings put global app_restriction_enabled true
```

```
adb shell settings put global automatic_power_save_mode 0
```

```
adb shell settings put global sem_enhanced_cpu_responsiveness 0
```

```
adb shell settings put global adaptive_battery_management_enabled 0
```

These ADB performance commands will help you optimize and improve the performance of your Android device. These ADB tweaks will make your device run faster and smoother, and enhance your overall user experience. Please note that after tweaking your phone for faster performance, you may experience battery drain.

**Read Next: [12 Tips to Boost Gaming Performance on Android](https://technastic.com/boost-gaming-performance-on-android/)**
