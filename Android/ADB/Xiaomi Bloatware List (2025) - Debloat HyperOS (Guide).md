______________________________________________________________________

title: "Xiaomi Bloatware List (2025) - Debloat HyperOS (Guide)"
source: "https://technastic.com/xiaomi-bloatware-list-miui/"
author:

- "\[[Rakesh Shukla]\]"
  published: 2025-06-06
  created: 2026-05-14
  description: "Find the list of safe-to-remove Xiaomi and MIUI bloatware. Learn how to uninstall system apps on MIUI 14 &13 via Xiaomi ADB/fastboot tools."
  tags:
- "clippings"

______________________________________________________________________

Xiaomi is notorious for shipping its smartphones with numerous useless apps, often referred to as bloatware. Since such apps are installed as system apps, one can’t uninstall them from the app settings. It’s easy to remove bloatware on Xiaomi, Redmi, Mi, and POCO devices running HyperOS and MIUI via ADB without root.

Recently, I shared a [list of secret codes for Xiaomi Redmi devices](https://technastic.com/xiaomi-redmi-secret-codes-list/) and the steps to uninstall them without root. Today, we’ll see how to uninstall the pre-installed apps on Xiaomi smartphones using ADB and bloatware removal tools.

Table of Content

## Xiaomi Bloatware List (HyperOS)

Here are the [app package names](https://technastic.com/app-package-name-android/) of safe-to-remove Xiaomi bloatware so you can uninstall or disable them without worrying about any adverse effects on your smartphone.

**Warning:** Please note that if you uninstall essential apps like the default launcher, gallery, camera, file manager, etc., you must install a 3rd-party alternative to such apps before you remove them. Also, if you are unsure about the outcome of uninstalling a system app, try disabling it first.

### Google Bloatware

```
com.android.bips | Default Printing Service
```

```
com.android.bookmarkprovider | Bookmark Provider
```

```
com.android.cellbroadcastreceiver
```

```
com.android.cellbroadcastreceiver.overlay.common
```

```
com.android.egg z| Android Easter Egg
```

```
com.android.emergency | SOS Calling
```

```
com.android.printspooler | Printing service
```

```
com.android.statementservice | Checks APK files
```

```
com.android.stk | SIM Tool-kit
```

```
com.android.wallpaper.livepicker | Live wallpaper
```

```
com.android.chrome | Chrome
```

```
com.google.android.apps.tachyon | Google Meet
```

```
com.google.android.apps.subscriptions.red | Google One
```

```
com.google.android.as.oss | Google private Compute Service
```

```
com.google.android.apps.youtube.music | Youtube Music
```

```
com.google.android.apps.docs | Google Docs
```

```
com.google.android.apps.photos | Google Photos
```

```
com.google.android.apps.wellbeing | Digital Wellbeing
```

```
com.google.android.feedback | Feedback app
```

```
com.google.android.inputmethod.latin | Gboard
```

```
com.google.android.marvin.talkback | Talkback feature
```

```
com.google.android.printservice.recommendation | Mobile Printing
```

```
com.google.android.videos | Google TV
```

```
com.google.ar.lens | AR Lens
```

### Xiaomi Bloatware

```
com.miui.cloudbackup | Xiaomi Cloud
```

```
com.xiaomi.micloud.sdk | Xiaomi Cloud
```

```
com.miui.micloudsync | Xiaomi Cloud
```

```
com.miui.cloudservice | Xiaomi Cloud
```

```
com.xiaomi.account | Xiaomi Account
```

```
com.miui.player | Mi Music
```

```
com.mi.global.shop | Mi Store
```

```
com.miui.yellowpage | Xiaomi Yellow pages
```

```
com.miui.miservice | Services & Feedback
```

```
com.xiaomi.aicr | Xiaomi AI engine
```

```
com.miui.accessibility | Mi Ditto
```

```
cn.wps.xiaomi.abroad.lite | Xiaomi WPS reader
```

```
com.mi.globalminusscreen | Xiaomi App Vault
```

```
com.android.thememanager | Xiaomi Theme manager
```

```
com.tencent.soter.soterserver | Tencent Wallet
```

```
com.miui.global.packageinstaller | Add based App Installer
```

```
com.android.providers.downloads.ui | Add based App Installer
```

```
com.mi.globalbrowser | Mi Browser
```

```
com.mi.health | Mi Health
```

```
com.mi.webkit.core | Mi Webkit
```

```
com.mipay.wallet.id | Mi Wallet
```

```
com.micredit.in | Mi Wallet (India)
```

```
com.miui.analytics | Telemetry (spyware)
```

```
com.miui.android.fashiongallery | Xiaomi Wallpaper Carousel
```

```
com.miui.bugreport | Bug reporting app
```

```
com.miui.cleanmaster | System Cleaner
```

```
com.miui.compass | MIUI Compass
```

```
com.miui.hybrid | Quick Apps (data mining app)
```

```
com.miui.hybrid.accessory | Quick Apps (data mining app)
```

```
com.miui.mishare.connectivity | Mi Share
```

```
com.miui.msa.global | MSA or MIUI Ad Services
```

```
com.miui.notes | Notes
```

```
com.miui.screenrecorder | Screen Recorder
```

```
com.miui.system | MIUI System Launcher
```

```
com.miui.systemui.carriers.overlay | Carrier name chaging service
```

```
com.miui.touchassistant | Quick Ball feature
```

```
com.miui.userguide | User Guide app
```

```
com.miui.videoplayer | MIUI Video player
```

```
com.miui.weather2 | Weather app
```

```
com.sohu.inputmethod.sogou.xiaomi
```

```
com.xiaomi.calendar | Mi Calendar
```

```
com.xiaomi.glgm | Game Center
```

```
com.xiaomi.joyose | Junk and safe to remove
```

```
com.xiaomi.midrop | Mi Drop
```

```
com.xiaomi.mipicks | GetApps (Xiaomi app store)
```

```
com.xiaomi.mircs | Message
```

```
com.xiaomi.payment | Mi Pay/Mi Coin
```

```
com.xiaomi.scanner | Scanner app
```

### Amazon, Netflix, Opera & Facebook Bloatware

```
com.amazon.appmanager | Amazon spyware
```

```
cn.wps.xiaomi.abroad.lite
```

```
com.netflix.partner.activation | Netflix
```

```
com.netflix.mediaclient | Netflix
```

```
com.opera.app.news | Opera
```

```
com.opera.branding | Opera
```

```
com.opera.branding.news | Opera News
```

```
com.opera.mini.native | Opera Mini
```

```
com.opera.preinstall | Opera
```

```
com.tencent.soter.soterserver | Chinese Payment service
```

```
com.facebook.appmanager | Facebook spyware
```

```
com.facebook.services | Facebook
```

```
com.facebook.system | Facebook
```

You can download the full list of safe-to-remove bloatware on HyperOS with `pm uninstall` command from [Google Drive](https://drive.google.com/file/d/1OSw05IqGrIJSEi4xcEMiV56xw4t428H3/view).

## ADB Command to List System Apps

You can use ADB shell commands to get the list of all installed apps regardless of the Xiaomi or Redmi phone model and OS version. By executing the following command, you can print the list of all system apps on your device.\
`adb shell`\
`pm list packages -s`

![xiaomi miui safe to remove bloatware](https://technastic.com/wp-content/uploads/2020/07/xiaomi-miui-system-apps-adb.png)

Xiaomi bloatware list

## Removing Bloatware on Xiaomi

You can uninstall bloatware on Xiaomi and Redmi devices running HyperOS using ADB commands.

To use ADB, you must download and set up the [latest SDK Platform Tools](https://technastic.com/android-sdk-platform-tools-download/) on your computer. You can also [use ADB commands on your Xiaomi phone](https://technastic.com/adb-fastboot-android/) without root if you don’t have a laptop or PC.

1. Extract the downloaded ‘ **platform-tools-latest-windows.zip** ‘ and open the folder.
1. Launch the Command Prompt via the Windows context menu by pressing the **Shift key + Right-click button** on the mouse.
1. Now type the following command in the CMD window and allow USB debugging to authorize ADB when prompted.
   ```
   adb devices
   ```
   [![ALLOW USB DEBUGGING ON XIAOMI]
