# Adb

## Extensive list of ADB commands

https://www.adb-shell.com/

## Different resource for ADB commands

[https://adbshell.com/](https://adbshell.com/)

## Start Adb server

```bash
adb start-server
```

## Kill the Adb server

```bash
adb kill-server
```

## List connected devices

```bash
adb devices
```

## Disconnect a device

```bash
adb disconnect <device-id>

```

## List apps (packages)

```bash
adb shell pm list packages
```

## Hardware stats

```bash
adb shell getprop |egrep "model|version.sdk|manufacturer|hardware|platform|revision|serialno|product.name|brand" 2> /dev/null
```

## Uninstall bloatware

[https://technastic.com/app-package-name-android/](https://technastic.com/app-package-name-android/)

### Google Chrome

```bash
adb shell pm uninstall --user 0 com.android.chrome

adb shell pm clear com.android.chrome 

adb shell pm hide --user 0 com.android.chrome 

adb shell pm disable-user --user 0 com.android.chrome
```

### Gmail

```bash
adb shell pm uninstall --user 0 com.google.android.gm

adb shell pm clear com.google.android.gm

adb shell pm disable-user --user 0 com.google.android.gm

adb shell pm hide --user 0 com.google.android.gm
```

### One Weather

```bash
adb shell pm uninstall --user 0 com.handmark.expressweather

adb shell pm clear com.handmark.expressweather


```

### Facebook

```bash
adb shell pm uninstall --user 0 com.facebook.katana

adb shell pm clear com.facebook.katana
```

### Linkedin

```bash
adb shell pm uninstall --user 0 com.linkedin.android

adb shell pm clear com.linkedin.android

```

### Spotify

```bash
adb shell pm uninstall --user 0 com.spotify.music

adb shell pm clear com.spotify.music

```

### Myhub

```bash
adb shell pm uninstall --user 0 com.tracfone.generic.mysites

adb shell pm clear com.tracfone.generic.mysites

adb shell pm disable-user --user 0 com.tracfone.generic.mysites
```

### Google Drive

```bash
adb shell pm uninstall --user 0 com.google.android.apps.docs

adb shell pm clear com.google.android.apps.docs

```

### Gmail

```bash
adb shell pm uninstall --user 0 com.google.android.gm

adb shell pm clear com.google.android.gm

```

### Google TV

```bash
adb shell pm uninstall --user 0 com.google.android.videos

adb shell pm clear com.google.android.videos

```

### Google Assistant

```bash
adb shell pm uninstall --user 0 com.google.android.apps.googleassistant

adb shell pm clear com.google.android.apps.googleassistant

adb shell pm hide --user 0 com.google.android.apps.googleassistant
```

## Google one

```bash
adb shell pm uninstall --user 0 com.google.android.apps.subscriptions.red

adb shell pm clear  com.google.android.apps.subscriptions.red

```

### Google Meet

```bash
adb shell pm uninstall --user 0 com.google.android.apps.tachyon

adb shell pm clear com.google.android.apps.tachyon

```

### Google Maps

```bash
adb shell pm uninstall --user 0 com.google.android.apps.maps

adb shell pm clear com.google.android.apps.maps
```

### Google Photos

```bash
adb shell pm uninstall --user 0 com.google.android.apps.photos

adb shell pm clear com.google.android.apps.photos

adb shell pm disable-user --user 0 com.google.apps.photos

adb shell pm hide --user 0 com.google.android.apps.photos
```

### Google Searchbox

```bash
adb shell pm uninstall --user 0 com.google.android.googlequicksearchbox
```

### Google Home

```bash
adb shell pm uninstall --user 0 com.google.android.apps.chromecast.app

adb shell pm clear com.google.android.apps.chromecast.app
```

### Google Wallet

```bash
adb shell pm uninstall --user 0 com.google.android.apps.walletnfcrel

adb shell pm clear com.google.android.apps.walletnfcrel
```

### TikTok

```bash
adb shell pm uninstall --user 0 com.zhiliaoapp.musically

adb shell pm clear com.zhiliaoapp.musically
```

### Netflix

```bash
adb shell pm uninstall --user 0 com.netflix.mediaclient

adb shell pm clear com.netflix.mediaclient
```

### Find Hub

```bash
adb shell pm uninstall --user 0 com.google.android.apps.adm

adb shell pm clear com.google.android.apps.adm
```

### Youtube music

```bash
adb shell pm uninstall --user 0 com.google.android.apps.youtube.music

adb shell pm clear com.google.android.apps.youtube.music

```

### Google keep

```bash
adb shell pm uninstall --user 0 com.google.android.keep

adb shell pm clear com.google.android.keep

adb shell pm disable-user --user 0 com.google.android.keep
```

### Google contacts

```bash
adb shell pm uninstall --user 0 com.google.android.contacts

adb shell pm clear --user 0 com.google.android.contacts

adb shell pm disable-user --user 0 com.google.android.contacts
```

### Android Auto

```bash
adb shell pm uninstall --user 0 com.google.android.projection.gearhead

adb shell pm clear --user 0 com.google.android.projection.gearhead

adb shell pm disable-user --user 0 com.google.android.projection.gearhead
```

### Youtube

```bash
adb shell pm uninstall --user 0 com.google.android.youtube

adb shell pm clear --user 0 com.google.android.youtube

adb shell pm disable-user --user 0 com.google.com.youtube

```

### Get IEMI

```bash
adb shell dumpsys iphonesybinfo

```

## SIM card

1. Once you’re in the ADB shell, type the following command to access the SIM card settings: settings put global sim_card_operator \`\<operator_name>1

1. Replace `<operator_name>` with the name of your mobile carrier.

1. You will see a list of SIM card settings, including APN settings and more.
