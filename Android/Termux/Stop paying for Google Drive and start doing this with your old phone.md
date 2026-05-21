---
title: Stop paying for Google Drive and start doing this with your old phone
source: https://www.makeuseof.com/stop-paying-google-drive-start-doing-this-with-phone/
author:
  - "[[Yadullah Abidi]]"
published: 2025-11-20
created: 2026-05-21
description: Why pay for storage when you've got free storage in your drawer?
tags:
  - Android
  - guide
---
If you want cloud storage, Google Drive's measly 15GB is going to run out quickly. Unless you're willing to pay, cloud storage really isn't the all-encompassing storage solution you're hoping it is.

But if you've got an old Android phone gathering dust, you can turn it into your own file server. All you need is this simple file server tool that's even [giving Nextcloud a run for its money](https://www.makeuseof.com/nextcloud-didnt-expect-competition-like-this/).

## Copyparty brings self-hosting to Android

### Your phone can become a fully fledged file server

[Copyparty](https://github.com/9001/copyparty) is a lightweight file server that can convert just about any device into a file server that you can access over a local network or the internet. The entire file server and all its features are compressed into one Python file. Drop the file into the root directory of the drive you want to use, and run it to start the server. That's it.

![Copyparty android file server on a web browser.](https://static0.makeuseofimages.com/wordpress/wp-content/uploads/wm/2025/11/copyparty-android-file-server-on-a-web-browser-1.JPG?q=49&fit=crop&w=500&dpr=2)

Credit: Yadullah Abidi / MakeUseOf

Apart from being incredibly easy to get started, Copyparty is fast. Not just reasonably fast for a free, self-hosted tool, but legitimately faster than many alternatives, including Nextcloud.

It doesn't skimp on any features either. You get resumable downloads and uploads, file deduplication, batch renaming, tagging for file organization, built-in media and thumbnail support, and on-the-fly compression. On top of that, Copyparty supports just about every file transfer protocol you'd want to use, including HTTP, HTTPS, WebDAV, FTP, FTPS, and TFTP.

This elaborate feature set and light footprint make Copyparty an excellent choice for running file servers on low-powered devices that have plenty of storage. Apart from running it on a Windows, Linux, or macOS machine, you can also use Copyparty to turn your Android (or iOS) phone into a file server.

Copyparty can turn almost any device into a file server with resumable uploads/downloads using any web browser.

[See at GitHub](https://github.com/9001/copyparty)

## Setting up Copyparty on your Android phone

### All you need is a terminal and a Python script

Similar to its PC version, running Copyparty on an Android phone is a matter of running a single command. However, since Android doesn't have a shell ready to go, you're going to have to install Termux first.

Termux is a terminal emulator that lets you run Linux commands on Android. You can download it from [F-Droid](https://f-droid.org/en/packages/com.termux/), but avoid the Google Play Store version of the app as it's no longer actively maintained.

Once Termux is installed, run the following command to install Termux:API and download the Copyparty script. Make sure you give Termux storage access permissions when prompted.

```
yes | pkg upgrade && termux-setup-storage && yes | pkg install python termux-api && python -m ensurepip && python -m pip install --user -U copyparty && { grep -qE 'PATH=.*\.local/bin' ~/.bashrc 2>/dev/null || { echo 'PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc && . ~/.bashrc; }; } echo $?
```

![Copyparty dependency installation command on Termux.](https://static0.makeuseofimages.com/wordpress/wp-content/uploads/wm/2025/11/copyparty-dependency-installation-command-on-termux.JPG?q=49&fit=crop&w=500&dpr=2)

Credit: Yadullah Abidi / MakeUseOf

If you want thumbnails for photos and videos and are okay spending another 132 MB of storage, run the following command.

```
pkg install ffmpeg && python3 -m pip install --user -U pillow
```

![Copyparty thumbnail dependency installation command on termux.](https://static0.makeuseofimages.com/wordpress/wp-content/uploads/wm/2025/11/copyparty-thumbnail-dependency-installation-command-on-termux.JPG?q=49&fit=crop&w=500&dpr=2)

Credit: Yadullah Abidi / MakeUseOf

And that's it. Copyparty is now ready to run on your Android. Just type **copyparty** anywhere in the terminal and a server will automatically start. You can also add the **\--qr** flag to get a handy QR code pointing to your file server.

![Copyparty qr code command on Termux.](https://static0.makeuseofimages.com/wordpress/wp-content/uploads/wm/2025/11/copyparty-qr-code-command-on-termux.JPG?q=49&fit=crop&w=500&dpr=2)

Credit: Yadullah Abidi / MakeUseOf

You'll also see the address to your file server mentioned in the terminal. Type this into any browser on any device that can connect to your network, and you'll be able to upload or download files to your phone's storage instantly.

## Why use a phone as the cloud?

### It's fast, free, and a whole new way to share files

Most relatively modern phones come with at least 128 GB. With Android installed, you still have give or take 100 GB of empty storage just sitting on an old phone. Running a file server on a laptop that you'd otherwise use for other tasks can also be tricky.

With an old phone, however, you can just hook it up to the Wi-Fi, plug it into the wall, and have it quietly sit in a corner of your house. You get significantly more storage than any other cloud storage service will offer while maintaining full control of your data and privacy.

![Copyparty file server qr code on Android.](https://static0.makeuseofimages.com/wordpress/wp-content/uploads/wm/2025/11/copyparty-file-server-qr-code-on-android.JPG?q=49&fit=crop&w=500&dpr=2)

Credit: Yadullah Abidi / MakeUseOf

Speed matters too. Copyparty is genuinely fast—several times faster than most cloud alternatives. In fact, I no longer use USB storage or external SSDs to move data between my laptops. Copyparty is plenty fast for most data transfers, regardless of their size.

This is one of the [best ways to reuse an old Android phone](https://www.makeuseof.com/make-old-android-phone-useful/) that's collecting dust in a drawer. It doesn't cost you anything other than a few minutes of tinkering, and you might come away with a genuinely useful tool. If you don't have an old phone, installing Copyparty on your main phone can be a great way to wirelessly share files between your phone and any other device.

## Your old hardware has a lot to offer

### Put that wasted storage to good use

Paying monthly subscriptions for cloud storage feels standard now, but it doesn't have to be. That old phone represents actual hardware you already own. Repurposing it costs nothing, gives you better privacy, faster data transfer speeds, and complete data ownership.

Copyparty isn't just a technical hack, it's practical proof that sometimes the best cloud storage is the one you host yourself. Your next personal file server is already sitting in your drawer, and I highly recommend you give it a shot.
