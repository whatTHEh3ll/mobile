---
title: Instructions for connecting Termux's android-tools adb to the current device via Wireless debugging and fixing phantom process killing
source: https://gist.github.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d
author:
published:
created: 2026-05-21
description: Instructions for connecting Termux's android-tools adb to the current device via Wireless debugging and fixing phantom process killing - 1-termux-adb.md
tags:
  - Android
  - guide
---
Instructions for connecting Termux's android-tools adb to the current device via Wireless debugging and fixing phantom process killing

[Raw](https://gist.github.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/7b6f82169d228e50385215562d678b08f58429ce/1-termux-adb.md)

[**1-termux-adb.md**](#file-1-termux-adb-md)

> Install android-tools if you haven't already:

```
pkg update ; pkg upgrade
pkg install android-tools
```
```
adb pair 127.0.0.1:port
```

> Where port is taken from the menu shown after clicking from `Developer options > Wireless debugging > Pair device with pairing code`. Use splitscreen to show the `Wireless debugging` setting below the Termux app when pairing.

[![](https://gist.githubusercontent.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/dd358e3fc8241f7eac7da00c5bb18f49bc74d876/pair.png)](https://gist.githubusercontent.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/dd358e3fc8241f7eac7da00c5bb18f49bc74d876/pair.png)

> After pairing successfully, run the following commands to either connect or disconnect:

```
adb connect 127.0.0.1:port

adb disconnect
```

> Where port is shown in the `Wireless debugging` menu as `IP address & Port`.

[![](https://gist.githubusercontent.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/dd358e3fc8241f7eac7da00c5bb18f49bc74d876/connect-disconnect.png)](https://gist.githubusercontent.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/dd358e3fc8241f7eac7da00c5bb18f49bc74d876/connect-disconnect.png)

> After you're done with adb, make sure to close the daemon:

```
adb kill-server
```

#### Notice: Disabling phantom process killing might cause battery drainage issues according to this comment, disable it at your own risk. From my experience, I never experienced this issue but that might be because I'm on MIUI so it might be more problematic if your phone OEM doesn't have an aggresive battery saver feature like Samsung or Xiaomi does.

> After Termux has connected via `Wireless debugging`, run the command below to fix phantom process killing. (Android 12L and above)

```
adb shell "settings put global settings_enable_monitor_phantom_procs false"
```

[Raw](https://gist.github.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/7b6f82169d228e50385215562d678b08f58429ce/connect-disconnect.png)

[**connect-disconnect.png**](#file-connect-disconnect-png)

![connect-disconnect.png](https://gist.github.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/7b6f82169d228e50385215562d678b08f58429ce/connect-disconnect.png)

[Raw](https://gist.github.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/7b6f82169d228e50385215562d678b08f58429ce/pair.png)

[**pair.png**](#file-pair-png)

![pair.png](https://gist.github.com/kairusds/1d4e32d3cf0d6ca44dc126c1a383a48d/raw/7b6f82169d228e50385215562d678b08f58429ce/pair.png)

```
adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"

adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"

adb shell settings put global settings_enable_monitor_phantom_procs false

adb shell cmd deviceidle whitelist +com.termux

 adb shell cmd appops set com.termux RUN_IN_BACKGROUND allow

 adb shell cmd appops set com.termux RUN_ANY_IN_BACKGROUND allow

 adb shell cmd appops set com.termux SYSTEM_EXEMPT_FROM_ACTIVITY_BG_START_RESTRICTION allow

 adb shell cmd appops set com.termux SYSTEM_EXEMPT_FROM_HIBERNATION allow

 adb shell cmd appops set com.termux SYSTEM_EXEMPT_FROM_POWER_RESTRICTIONS allow

 adb shell cmd appops set com.termux SYSTEM_EXEMPT_FROM_SUSPENSION allow

 adb shell cmd appops set com.termux WAKE_LOCK allow
```
