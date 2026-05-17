---
title: "Every Android Setting in the Developer Options Explained!"
source: "https://www.youtube.com/watch?v=JkV78G4UXDM"
author:
  - "[[HowToMen]]"
published: 2021-08-24
created: 2026-05-17
description: "▣ UPDATED VIDEO: \"15 Hidden Features Found in the Developer Options\"https://youtu.be/lHguzVqAdqk________________________________________­­_Use LINER now for an easier way to find reliable informati"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=JkV78G4UXDM)

▣ UPDATED VIDEO: "15 Hidden Features Found in the Developer Options"
https://youtu.be/lHguzVqAdqk
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_­­\_
Use LINER now for an easier way to find reliable information on the web:
https://dynamic-link.getliner.com/howtomen

LINER also timestamped this video with their YouTube highlighting feature
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_­­\_
The Complete Developer Options Video Guide! In this video, I explain every single setting that is within the Developer option in great detail. If you ever wanted to know what that specific setting meant in the developer options, this video will most likely explain it. So sit back, grab your coffee, and enjoy!
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_­­\_

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_­­\_
➨ DisplayPort Alt Mode Supported devices:
https://en.everybodywiki.com/List\_of\_devices\_with\_video\_output\_over\_USB-C
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_­­\_
Timestamps
0:00 Developer Options Explained
2:07 How to Enable Developer Options
2:52 First Section of Settings
8:10 LINER
10:03 Debugging
14:30 Networking
19:30 Input
19:47 Drawing
21:18 Hardware accelerated rendering
22:59 Media
23:16 Monitoring
23:42 Apps
28:05 Autofill
28:43 Storage
28:55 Final thoughts

## Transcript

### Developer Options Explained

**0:00** · deep down within the system settings there's a secret hidden menu called the developer options and this menu is filled with juicy valuable features that most people don't even know exists for example you know when you connect your phone to the computer and you need to do the annoying process of dropping down the status bar and selecting the bottom notification just to change the usb

**0:20** · preference to transfer files why do we need to do all that well within the developer options there's a setting called default usb configuration and that lets you select file transfer as your default choice so now whenever you connect your phone to the computer your files will automatically pop up without needing to do those extra steps another excellent feature is that if you have an app that doesn't support split screen mode like instagram you can still force it to open it in split screen anyway by enabling force activities to be resizable within the developer options

**0:55** · that's just two useful features found within this vast list of developer options and in this video i'll be explaining each setting not missing a single one and what i would recommend modifying for a better smartphone experience i promise you that there is no other video form page ready or article that explains every single developer option setting in great detail all at once they may just show off some of their favorite options but not explain every single setting in there so if you were ever curious about what a specific option did in this menu this is

**1:24** · the best video guide i even time stamped each section properly according to how the developer options are organized so that if you just want to jump to that specific section for a specific setting you can do so so make sure to save this video for future reference drop a thumbs up if you change a setting and get subscribed with the notification bell turned on if i made you change two or more here we try to stand out from the competition by making videos that no one else wants to make and i do it for you guys now let's jump into rock bottom and figure out what those weird toggles actually do

**1:56** · \[Music\] i still can't read the sign i want to go home now the first thing i have to do is show you how to enable the developer options it varies between most phones but usually within the system settings you scroll down to the bottom tap on about phone scroll down again until you see build number and tap it seven times

### How to Enable Developer Options

**2:22** · it'll have you confirm your passcode and then you'll receive a toast message that says you're now a developer from there go back to the previous screen tap on system and then there it is developer options now depending on what android version you're running and what oem you have your developer options could be a bit different from mine you could have a few more toggles or a few missing toggles it all depends on what phone you're using for those curious i'll be explaining the developer options with my google pixel 5 running android 12 beta

**2:51** · 4. now the first option at the top is called memory and it's pretty self-explanatory it tells you how much memory your phone has and the average amount of time that is being used it's not in real time but it does tell you the average memory used for the past 3 hours or you can change it to 6 hours 12

### First Section of Settings

**3:07** · hours or 1 full day not only that but you can even see what apps are consuming your memory usually it's system apps but diving in deeper you can tap on any of them to see how frequently they're using your memory and their maximum usage on the rare occasion that there is a pesky memory leaching app that you rarely ever use i recommend uninstalling it however

**3:27** · if you like to see your memory running in real time scroll down a bit further and you'll see an option called running services here you'll see what apps and services are currently running in the background if you find a service that is taking up too much memory you can quickly terminate it capturing bugs is mainly a developer thing but if you're ever experiencing any issues with an app or maybe even your system interface then you can use bug report found within the developer options to capture these bugs

**3:53** · so that you can send them to the developers so that they can fix the problem the bug report feature will keep a log of every action that you begin to do and it'll even capture the issue you're experiencing to share the bug report you just tap on the notification pretty easy and it really helps developers find issues faster

**4:11** · plus within the developer options if you scroll down even further you can have the bug report button appear in your power menu for easier access by default the bug reports don't show your device specific vendors such as samsung oneplus google etc but you can add this additional information in your bug reports by enabling verbose vendored logging within the developer options it just helps out the developer by letting him know what phone manufacturer you have you can also

**4:36** · determine which app handles the bug report shortcut on your device so since i'm on a beta version of android 12 i changed the bug report handler to the android beta feedback option basically reporting bugs directly to the google team that is working on android 12. they also created a feedback app that does a really great job of making it easy for anyone to report an issue they're having with an app or the interface

**4:59** · moving on most of you probably don't know this but you can backup your phone's data and app data onto your computer with a simple adb command called adb backup dash all and whatever directory your command prompt is set to it'll save this backup as a file called backup.ab if a date comes that you need to restore it then you type in adb restore along with the file path in which the backup.ab file is located in simple just

**5:27** · make sure you have adb installed on your computer and usb debugging enabled and that's pretty much it also within the developer options you can even set a password to encrypt these full desktop backups under the menu called desktop backup passwords the stay awake toggle keeps your phone awake indefinitely while you charge it until you manually press the lock key enable bluetooth hci

**5:48** · snoop log will not call up snoop dogg to perform at your birthday party instead it's a lot more boring than that and mainly for developers just like the bug report feature this will create a log of your bluetooth usage over time oem unlocking is one of the most important toggles within the developer options when you enable this you're allowing your bootloader to become unlocked after you do a simple adb command and from there the possibilities are endless since you can obtain root and do things like install custom roms obtain magisk

**6:17** · manager for a bunch of awesome modifications and a lot more webview implementation just lets you choose between a different webview app and for those who don't know what webview is it's basically an in-app browser whenever you tap on a link within an app such as twitter or instagram that webview app gets used personally the default android system webview works just fine so i just stick with that next some devices have an advanced reboot option which is really useful for anyone who is rooted since you can quickly jump into the recovery or bootloader through the power menu

**6:49** · automatic system updates just lets you automatically apply any available software updates whenever your phone restarts dsu loader is strictly for developers who want to test their apps on stock android since it lets them install the latest gsi from google without needing to input any adb or fastboot commands system ui demo mode is what i like to use in most of my videos since it cleans up my status bar by removing any notification icons keeping the time the

**7:15** · same and it matches the android version number plus my battery level is always at a beautiful 100 percent so no distractions on what notifications i received quick settings developer tiles is self-explanatory it allows you to put some of the settings found within your developer options into your quick settings panel a lot of them are meant for developers but the two that i like to use are sensors off and wireless debugging sensors off disables almost every sensor on your phone including the cameras gps and microphone perfect for

**7:44** · staying private while wireless debugging lets you connect your phone to your command prompt wirelessly so that you can quickly launch any adb command so i can literally install apps reboot my phone launch into the bootloader and a lot more without needing a cable you just have to make sure your phone and computer are connected to the same wi-fi network the connection is a hit or miss situation though the most reliable way is still by using a usb cable

### LINER

**8:10** · now before i continue to other sections filled with other very useful features i wanted to show up a fantastic chrome extension slash app that makes finding reliable information a lot faster and easier it's called liner and they are the sponsor of this video check this out whenever i jump into a web page or a pdf file liner lets me highlight any text that i deem important and even if i refresh the page the highlighting stays

**8:33** · there it's just like when you highlight in a book the fun doesn't stop there though i can also add any comments to organize my thoughts share with anyone who isn't even using liner add tags for easier retrievals and each highlight gets automatically saved so that i can quickly find it later within my highlights it's a fantastic tool that's helped me stay organized and consistent with my research plus you can take your highlights on the go when you download their free app from the play store or app store it works just like the chrome extension and has most of the same highlighting features

**9:05** · but that's not even the best part because with liner you can mark and comment on any critical moments within a youtube video so that later on you can quickly jump to it now tell me that's not the coolest thing you've ever seen the mobile app will also soon receive this youtube highlighting feature as well which i'm also pumped about as if that wasn't enough liner also makes your google searches a lot more reliable and personal whenever you search for anything a mint bar appears next to the pages that liner recommends this is

**9:30** · extremely useful since the recommendations are based on the number of total highlights made from other users on the page the mobile app will also receive this google search assistant feature in the future plus within liner's platform they have a for you section and a search engine which lists out content of your interest that you may have missed making it easier to get recommendations for things you couldn't find with a google search so if you like an easier way to find reliable information and keep track of it whenever you read an article pdf or watch a video download liner now on both

**10:00** · your desktop and smartphone through the link in the description whenever you grant usb debugging access to any computer then anyone can just control your phone without needing to unlock it so if you don't want that make sure to tap on revoke usb debugging authorizations within the developer options so that any previous computer authorizations get revoked now in the future those same computers will need you to unlock the phone again to grant it access

### Debugging

**10:27** · finally by default any adb authorizations get automatically revoked after seven days of not reconnecting to your computer but if you like to disable this timeout just toggle on disable adb authorization timeout if you ever want to spook your current location you can do so with select mock location app you just need to download an app like fake gps location from the play store to get this to work forceful gnss measurements are just for

**10:54** · developers who want to accurately calculate positions within apps by continuously tracking satellites the enable view attribute inspection is just for developers to help them debug their apps select debug app is also for app developers to help debug their app individually without using long adb commands or a debugger so there's no need to mess with these two previous options also wait for debugger is an

**11:16** · option that attaches the above debugged app instantly when a debugger is detected whenever you install an app with the usb through adb commands google will scan it to make sure that it's not infected with malicious content you just need to make sure that verify apps over usb is enabled and your installed app should be safe but if you're trying to install a reliable app over usb and it's

**11:38** · not working try disabling this toggle but only disable it if you know the app doesn't have any malicious code within it the verify by code of debuggable apps toggle that's mouthful is a little more complicated but just leave it enabled if you must know this toggle allows android's runtime to verify the bytecode for apps that you install when you record audio your microphones need a miniscule amount of time to analyze the sounds coming into your phone the time is referred to as buffer size and within the developer options you can choose the logger size of each buffer

**12:10** · but honestly unless you're in big time audio file i wouldn't mess with it you know those experimental features found within google chrome labeled as flags while feature flags within the developer options is pretty much the same concept it was heavily used back in android 10 and 11 to enable apple features that the google team were still testing and working as of now it's not currently active in android 12 beta 4 but just keep an eye on this menu if you ever update to a beta software gpu debug

**12:36** · layers is yet another feature that is only for game developers so there's no need to enable it if you're a big gamer you may be able to improve your gaming experience with graphics driver preferences in this menu you can select the graphics driver on a perhaps basis personally for every game that i had i just selected system graphics driver as my preference it's

**12:54** · useful if your phone doesn't come with a gaming mode installed like the pixel devices running android 11 otherwise you don't really need to modify this menu new api features get released for applications whenever the android os gets updated and developers usually need to run adb commands to test them out however since android 11 a new sub menu in the developer options called app compatibility changes makes it really easy to quickly toggle new platform behavior changes instead of typing many adb commands it saves that developers a ton of time if your phone has a 90 or 120hz display

**13:28** · chances are not every app or screen is running at those high refresh rates they most likely drop at 60 hertz to save battery life my pixel 5 for example drops to 60 hertz whenever i'm not interacting with the screen or when i'm in the camera app how do i know this well a toggle called show refresh rate lets me know for the

**13:47** · apps that have the permission called display over other apps you can also have them show their floating windows when you're in the system settings you just need to enable allow screen to overlays on settings and also for those curious i'm using an app called floating apps for this demonstration not everyone has this toggle called force peak refresh rate but if you do enabling it will force your display to always stay at the maximum refresh rate no matter what app you use so in my case my pixel

**14:14** · 5 no longer drops down to 60 hertz it may seem like an awesome toggle but your battery life is going to suffer system tracing is just for app developers it lets them collect system activity to learn about what's going on with the device and how they can improve performance when their app is being run now we're getting into the networking section the first option called wireless displayed certification is only useful if you own a mirror cast support display the next option wi-fi verbose logging lets you keep a more advanced logging of your wi-fi connections and network signal strength nothing fancy here wi-fi

### Networking

**14:46** · scan throttling helps save your battery life and improves the network performance by limiting how often apps can scan for wi-fi in other words this option is there so apps cannot just scan for wi-fi whenever they want that would be terrible to be more precise foreground apps can only run four wi-fi scans every two minutes while background apps can only run a scan every 30 minutes so just leave it on wi-fi non-persistent mac randomization causes

**15:11** · your device to change the mac address each time you connect to a wi-fi network it's just for privacy reasons so that your device doesn't use the same mac address for everything i actually toggle this on the next option called mobile data always active keeps your wireless data connection always on even when you're connected to wi-fi and the only reason they do this is for faster network switching but honestly it's a huge battery trainer if you live outside of the us i would definitely recommend turning it off but if you live in the us you probably shouldn't because if you're like me you probably still use mms

**15:41** · because of iphone users and having this toggle off will make it so that you won't be able to send or download mms messages when you're on wi-fi tethering hardware acceleration is a bit more complicated to explain but essentially on supported devices and support networks the android os will use hardware instead of software for tethering your data connection to other devices and will ask the hardware to manage it it's a more efficient method and saves you battery when using tethering however i'm not 100 sure what

**16:10** · phones support this feature my guess is if the toggle isn't enabled by default then your device is most likely not supported still i personally enabled it on my pixel 5 just in case because if it does work then why not save that battery whenever you try to pair to a new bluetooth device your phone automatically finds the name of the devices so that you can more easily identify them but some bluetooth devices get hidden by the android os it's usually those that don't have names just mac addresses and on some rare occasions

**16:36** · this can lead you to not being able to find the bluetooth device that you're trying to pair well if you enable show bluetooth devices without names in the developer options then every bluetooth device including those with just mac addresses will appear when you try to pair it's just like enabling the show hidden files and folders option within windows 10. by default when connected

**16:55** · your phone and bluetooth device both control the same volume level generally this is convenient because who likes messing with two separate volume levels but in some rare occasions this can cause some volume issues or lack of control so if you turn on disable absolute volume you'll then be able to separate the two you can set your bluetooth device's volume to an acceptable level then use your phone's volume buttons for fine tune adjustments it comes in handy if you have an overly loud speaker as if the settings could have gotten even more bizarre there's an option called enable gable doors this enables

**17:28** · google's new upcoming bluetooth stack called gable dorsch before andrew relied on the fluoride stack now they're trying to transition to a new stack called gable dorche it's going to help improve the security and reliability of bluetooth connections as of now i'm not sure if it even works though because there hasn't been any word from google on this setting for over a year so just

**17:48** · leave it off the next couple of bluetooth options are really just there if you're experiencing any bluetooth issues not just with one bluetooth device but with any device that your phone connects to it's really rare and usually only occurs when you update to an alpha or beta version of a software or you just get a new phone that got released that same month and the software is not fully stable yet if you're experiencing bluetooth issues then the last resort would be to hop into the developer options and try to activate disable bluetooth a2dp hardware

**18:17** · offload another option would be to lower the bluetooth av rcp version number or higher the map version one at a time though and as always when you modify these things make sure to reboot each time to activate the change of course i'm not saying this will solve the problem you're having but it's worth a shot moving on if you like to make sure that those wireless earbuds or bluetooth speaker have the best possible sound profile then within the developer options there's something called bluetooth audio codec and in this menu

**18:44** · you can select an even better profile if it's available if you're on android 11 or higher your phone will automatically disable any codecs that your bluetooth device doesn't support once you're connected generally speaking aac already provides really great sound quality so if you have that option choose it sbc is the lowest audio quality so try to avoid that qualcomm aptx hd audio is just as good as aac with some saying it provides even better quality and finally ldac is

**19:13** · sony's proprietary bluetooth streaming codec which provides the highest quality so if you have that option i envy you and definitely go with that plus you can increase the sampling rate audio bits and channel mode i personally didn't have those options since my headphones didn't support it but if you do try to see what you can do within the input section you can choose to show the taps this is great when you're screen recording anything and want to show the person exactly what you're tapping on

### Input

**19:38** · pointer location draws a tracer line showing a more precise drawing of where the screen has been swiped that option is definitely for developers and that's it for the input section drawing section is mostly just stuff for app developers to help them make their apps more compatible with other devices starting with show surface updates this helps developers see what part of their app is doing work it does this by flashing the screen rapidly shell layout bounds is even fancier since it clearly marks every border clip bound margin etc it's

### Drawing

**20:06** · used during the app development to validate the positioning and alignment of visual items on the screen if you'd like to flip the entire screen from right to left you can do so with force rtl layout direction it's kind of weird though and gives me a ton of brain farts actually now i think about it it would actually be a good prank on a friend the following three options are the most popular selections within the developer options you can increase decrease or

**20:30** · just stop the window animation transition animation and animator duration i personally just keep those at 1x but i know that a few people like to go with 0.5 x for the extra speed simulate secondary displays does as the title implies it enables a second screen

**20:47** · with your choice of resolution it's just for developers so that they can see how their app would look on different screen sizes it's kind of cool and trippy smallest width lets you change the density independent pixels or dp of your display so that you can have everything be smaller or bigger some people even like to make the dp even bigger to see even more stuff at once on the screen display cutout lets you hide your notch or hole punch if your screen has one or

**21:12** · at least tries to but it's also used by developers to make their apps more compatible with different types of displays the hardware accelerated rendering section is to help game developers improve the games with the view updates you can have parts of the screen flash red whenever the gpu is operating an object the hardware layers updates does pretty much the same thing but it differs by flashing a green light whenever updates are made to the hardware layers it helps the game developers optimize the performance whenever there is a severe amount of green flashes the debug gpu overdraw

### Hardware accelerated rendering

**21:44** · will tell you when the same place on the screen has been drawn over multiple times by different objects and it shows you this by color coding the overdrawn views it helps developers improve the performance when using their app because the fewer layers they have the faster and more efficient their app is override force dark is in my top three favorite toggles found within the developer options it forces most apps that don't have a dark mode to have one so apps like amazon google opinion rewards and geeky bench 5 can now all

**22:12** · have a dark theme with a simple switch of a button force 4x msaa is for gamers to help them have better graphics and improve the overall visual experience but it does take up a lot of performance and is a huge battery trainer so i wouldn't enable this even if you are a gamer i still wouldn't recommend it because honestly we all know that it's performance over looks when it comes to competitive gaming disabled hardware overlays is a bit more complicated to explain basically in short every app

**22:39** · shares video memory and without a hardware overlay they'll need to constantly check for collision and clipping costing a lot more cpu power so just leave this option turned off simulate color space is an option that developers can use to see what their apps would look like to colorblind users it's pretty cool and you can also use this to turn your screen black and white

### Media

**23:00** · in the media group there are only two options the first one is for audio files it disables automatic routing to usb audio peripherals like a usb dock and then the second option lets you configure some options for when your sound or video gets transcoded i personally didn't touch these two settings there are times when apps take longer than usual to do operations whether it be in the background or foreground which can cause battery drain well when you enable strict mode you'll know exactly when this happens because the screen will flash profile hw ui

### Monitoring

**23:31** · rendering is pretty sick it allows you to display a graph on the screen of how the gpu is working under the hood in real time so whenever you open an app or run an animation you'll see the graph shoot up the app section has by far the best group of options in the developer options this is where all the gold is at the first option called don't keep activities force closes every app you leave which can seem like a good thing and it is if you're looking at it from a privacy standpoint but from a battery

### Apps

**23:55** · standpoint this is a terrible option since you're forced to close every app you leave and the cpu will need to work overtime whenever you open an app because it'll never be on standby so i would highly suggest leaving this option off the next option called background process limit will allow you to choose how many apps or processes are allowed to run in the background and just like with the previous option i wouldn't change it because otherwise they only allow you to choose at most four processes like why so little

**24:24** · wait wait wait a minute this ain't enough make it enough for whatever reason you could have some apps preventing your phone from going into a deep sleep it's rare but it happens background check lets you quickly find those pesky apps and you can stop them with a switch of a button if you don't see any in this menu you're in the clear though remember back in the day when an app that froze would bring up a crash window that allowed you to choose between closing the app or just waiting well after the android 9.0

**24:54** · update google decided to remove it all together and instead automatically crash the app in some cases though that can be annoying so if you'd like to bring back that dialogue turn on always show crash dialogue within the developer options for apps that crash in the background you'll need to instead enable show background anrs this next option allows

**25:13** · you to freeze zap so that they can't use any of the cpu cycles while they're cached being that there are sometimes misbehaving apps that may attempt to run while being cached the suspend execution for cached apps stops them and helps reduce the power consumption greatly that's why i had this option enabled the notification channel warnings are just for developers to make sure that their apps are properly displaying notifications so there's no need to enable this if you're running under 12 you can prioritize some notifications over others so that they always appear at the top but if you like to reset the notification importance you can do it

**25:45** · from the developer options standby apps is a juicy setting here you'll see a list of all your apps installed and you can place each app into a group there are five groups and the higher and the happiest on the list the more important it is for example apps placed in the active activity are at the highest level and don't have any restrictions so they can keep functioning as per their default settings this includes apps like messaging or the phone app working set puts a medium level restriction but the apps can keep functioning as usual this

**26:14** · can be apps like google maps or chrome frequent puts stronger restrictions but is still able to run i put some games in this setting rare puts strict rules on their ability to run in the background receive messages and can't connect to the internet while in the background and restricted means that they just can't run or do anything in the background at all based on how you use your phone the os will automatically determine which profile is set on each app so you don't really need to worry about this but if you like to modify it for specific apps you can do that this next one's pretty useful if your phone has an sd card and

**26:46** · you try to install an app on it but it doesn't work you can enable force allow apps on external and this will force the app to let you store it on the card that way you can save space on your internal memory believe it or not apps can become floating windows on android so you can literally be scrolling on your home screen and have twitter be on top of the screen to do this just turn on enable freeform windows within the developer options then within the recent menu tap on the apps icon that you'd like to turn into a window and tap on freeform it's a

**27:14** · bit difficult to resize the window but you can do so by pulling the corners it's a cool feature but it's pretty useless says since you can't open another app at the same time besides your stock launcher and you can't freeform another app simultaneously your android could have a

**27:30** · desktop mode allowing you to run android apps on the big screen in the developer options you just need to enable force desktop mode and from there with a type c to hdmi cable you can connect your phone to an external monitor and boom there you have desktop mode just keep in mind that this only works on phones that support displayport alt mode not every phone supports this including the pixel 5 so i'll leave a link with a partial

**27:52** · list of supported devices the shortcut manager rate limiting option is specifically for developers it resets the rate limit to allow background apps to continue to call shortcut apis until the rate limit is reached again the autofill section is by far the most boring part of the developer options it's just filled with a bunch of things you will never touch unless you're a developer working with the autofill service starting with the login level this is just a way of classifying entries in a log file in terms of urgency and android supports various log levels including info warnings mirror

### Autofill

**28:23** · errors verbose and debug in the developer options when keeping logs you can choose between the debug type which is standard or you can choose verbose which provides more detailed information the other two options below let the developers set the maximum request for the autofill service in one session and the maximum visible data set plus you can reset those values back to default finally i'm not 100 sure what shared

### Storage

**28:46** · data is since i couldn't find anything on the internet about it but i'm assuming that it's any data on your phone that you're allowing to be shared with a private or public server i could be wrong though anyways that's every single setting explained within the developer options again there's no video forum page ready or even an article that has explained what each setting does in

### Final thoughts

**29:06** · one full setting so for that all i ask is that you please drop a thumbs up also if i helped you discover a setting or two please consider subscribing here on this channel is quality over quantity either way thank you guys for watching and i'll catch you guys in the next one.
