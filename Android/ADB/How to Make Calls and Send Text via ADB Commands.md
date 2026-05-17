______________________________________________________________________

title: "How to Make Calls and Send Text via ADB Commands"
source: "https://technastic.com/make-calls-send-message-adb-commands/"
author:

- "\[[Rakesh Shukla]\]"
  published: 2025-05-12
  created: 2026-05-14
  description: "ADB commands can perform many tasks. You can make calls, send text messages, and input text on your Android device with ADB Shell commands."
  tags:
- "clippings"

______________________________________________________________________

I don’t know how many people ever get into a situation where they have to make a call or send a text message using commands. ADB allows Android users to perform various tasks, such as managing apps, capturing screenshots, recording screen activity, and transferring files between devices and computers. This tutorial purports to introduce our readers to the extensive capabilities of ADB in controlling Android devices from a command-line interface.

You can send and execute ADB commands in 3 ways.

- - [Set up ADB on your Windows, Mac, or Linux system](https://technastic.com/android-sdk-platform-tools-download/)
    \- [Configure ADB over Wi-Fi](https://technastic.com/set-up-adb-over-wifi-android/)
    \- [Using a terminal app like aShell or Termux](https://technastic.com/adb-fastboot-android/)

Table of Content

## ADB Command to Make a Call

The quickest way to make phone calls is via the Phone app. However, if your phone’s touchscreen is non-functional, you can use ADB commands to dial a number. Follow the steps below to make a call from your Android device without touching it.

1. [Launch a PowerShell window](https://technastic.com/open-powershell-windows-11-10/) with the path of the ‘platform-tools’ folder.
1. To invoke ADB Shell, type **`adb shell`** in the command window and press Enter.
1. Now type or paste the following command in PowerShell.
   ```
   am start -a android.intent.action.CALL -d tel:+19792211000
   ```
1. Replace the phone number in the command with the number you want to call.
1. When you hit Enter, your Android device will dial the number.[![adb shell command to make phone calls](https://technastic.com/wp-content/uploads/2024/01/adb-shell-command-make-phone-call.png)](https://technastic.com/wp-content/uploads/2024/01/adb-shell-command-make-phone-call.png)

### Picking up and Ending a Call with a Command

You can make calls, pick up an incoming call, or cancel it. Here’s how to do that. Launch a PowerShell window and execute the following command to accept an incoming call on Android:

```
adb shell input keyevent KEYCODE_CALL
```

To cut or hang up an incoming call, execute the command given below:[![adb command to hang up phone call on android](https://technastic.com/wp-content/uploads/2024/01/cancel-call-adb-shell-command.png)](https://technastic.com/wp-content/uploads/2024/01/cancel-call-adb-shell-command.png)

```
adb shell input keyevent KEYCODE_ENDCALL
```

## ADB Command to Send Text Message

You can also send text messages to any phone number from your Android device via the command-line interface on your Windows, Mac, or Linux computer.

1. Open a PowerShell window and execute the **`adb shell`** command.
1. Right after the dollar sign ($), type the following command. Do not forget to replace the phone number and message body (highlighted in blue).
   ```
   am start -a android.intent.action.SENDTO -d sms:+17007800006 --es sms_body "Test Message from Technastic.com"
   ```
1. This command will open the Messages app and input the message content in the text field.
1. To send your message, you’ll need to execute the following key event commands one after another to send your message to the recipient.
   ```
   input keyevent 22
   ```
   ```
   input keyevent 66
   ```
   [![ADB COMMAND TO SEND TEXT MESSAGE]
