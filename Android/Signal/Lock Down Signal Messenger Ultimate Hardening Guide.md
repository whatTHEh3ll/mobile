---
title: "Lock Down Signal Messenger: Ultimate Hardening Guide"
source: "https://www.youtube.com/watch?v=DPjg3651oJM"
author:
  - "[[Techlore]]"
published: 2024-08-09
created: 2026-05-17
description: "Signal is one of the safest messengers, but that doesn't mean we can't make it safer! Welcome to the ultimate Signal hardening guide to make it as private, secure, & safe as possible. This video tutor"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=DPjg3651oJM)

Signal is one of the safest messengers, but that doesn't mean we can't make it safer! Welcome to the ultimate Signal hardening guide to make it as private, secure, & safe as possible. This video tutorial applies to iOS, Android, and touches on desktop devices using not just native Signal settings, but also other hardening techniques.

Thank you to our sponsor Notesnook! Visit their site to learn more about keeping your data safe with E2EE notes: https://notesnook.com

Messenger Comparison Video: https://youtu.be/rPp4rQnrG44
Molly Review: https://youtu.be/P-2z2c3XBkQ
Lockdown Mode Video: https://youtu.be/ENuGWhz10UY
Recent Signal Vulnerability: https://youtu.be/Gvc1XKLt3aw
Become Anonymous Guide: https://youtu.be/a1i-3xwcSGA
Guide to Verifying Signal Safety Numbers: https://discuss.techlore.tech/t/a-guide-to-verifying-signal-safety-numbers/2289
External Guides:
https://cert.europa.eu/publications/security-guidance/security-guidance-22-002---hardening-signal/pdf
https://freedom.press/training/locking-down-signal/
https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/

00:00 Intro
00:50 Chapter 1: Basic Configuration Settings
01:00 Signal Pin & Registration Lock
01:53 Signal Username and hiding phone number
02:42 Verifying Signal Safety Numbers
04:40 Screen Lock Password
05:20 App Switcher Privacy Settings
05:48 Notification Privacy Settings
06:40 Chapter 2: Advanced Configuration Settings
06:54 Disappearing Messages
09:04 Relaying Calls
09:50 Disabling iOS Integrations
10:44 Incognito Keyboard Function on Android
11:28 Disabling Link Previews in chats
12:38 Chapter 3: Advanced Hardening Advice
12:56 Basic endpoint security tips
13:48 Encrypted backups
14:04 Enabling lockdown mode on Apple devices
14:28 Google advanced protection program
14:36 Custom ROMs
14:44 VPNs
15:50 Limiting linked devices
16:56 Obfuscating your Signal Phone Number
18:30 Molly the Signal client
20:14 Closing Remarks

🔐 Techlore Homepage: https://techlore.tech
🕵 Go Incognito Course: https://techlore.te[[]]ch/goincognito
💻 Techlore Community: https://discuss.techlore.tech
🏫 Techlore Coaching: https://techlore.tech/coaching
💬 Signal Group: https://discuss.techlore.tech/t/signal-usernames-are-here-join-our-signal-group-techlore/7640

We cannot provide our content without our Patrons, huge thanks to:
BRIGHTSIDE Clark Ente Larry Richard Afonso Brad JohnnyO kevin 'love your content' Poaclu x
🧡 Join them on Patreon: https://www.patreon.com/techlore
💚 To see our production gear, privacy tools we use, and other affiliates: https://techlore.tech/affiliates
💖 All Techlore Support Methods: https://techlore.tech/support
#signal #techlore #guide

## Transcript

**0:00** · signal is my main messenger and I love it but nothing is perfect so while signal has notoriously one of the best reputations for privacy and security there are things that by default it may not offer every user now it goes without saying this is for people already using signal there are signal Alternatives I've covered in a different video I'll leave it in the card if you want to go see signal stacked against some of the competitors and my final disclaimer is of course this is not a you have to do

**0:29** · every step in this video in fact I don't think anyone will do every step and you probably shouldn't do every step unless you truly need to because a lot of the steps especially further along in the video have pretty significant drawbacks the way we're going to break this video down is we're going to start with basic configuration which is pretty much a configuration built into signal using native tools pretty simple stuff but it does get quite a bit more advanced as we go along because we're going to enter Advanced configuration which is still using native signal tools and then we'll

**0:57** · go into actual hardening which pretty much takes place outside of what signal can offer you directly first thing is your PIN so when you register for Signal you're going to be asked to set up a pin this is used to recover your profile your settings your contacts and a lot more it's also used as a prevention from someone registering on a new device with your phone number so make sure this is really strong on both Android and iOS

**1:20** · you're going to go into your settings you're going to go into your account settings and you're going to go into your signal pin and make sure you create a new pin in this menu you want to use a strong alpha numeric pin so you can use a password manager for this if you really want to make this as good as you possibly can instead of just sticking with like a four-digit pin which might be pretty easy to crack the next step is actually already here so make sure you enable this registration lock if you forget the pin and you enable this you're only going to be locked out of your account for 7 Days um this is a

**1:49** · temporary but very important measure to prevent your account from being broken into we'll cover ways to better OB thecate your signal number later in the video but for now we're going to use built-in tools and Signal recent ly unveiled their most requested feature which is usernames which allow you to hide your phone number from your contacts to do this go into your settings and go into your profile and then you're going to set a username to get started with a non- number identifier once you do that you're not done you're going to go into your privacy settings you're going to go into your phone number and you're going to select who can see my number to nobody

**2:20** · and who can find me by number to num you're going to select who can find me by number to nobody you should disable both of those if you're somebody who wants to hide your phone number from your contacts and from Discovery for new people trying to locate you this means that people will have to have your username to message you and even people who already messaged you in the past will no longer be able to see your phone number now let's talk about basic configuration options to protect the security between you and your contacts

**2:48** · so safety numbers are a feature and signal that allow you to verify the people you're chatting with are always who they say they are I have a pretty tight requirement where all of my main contacts are verified so every conversation is is going to have a unique safety number that's the same for both people so with Jordan who's one of our team members you can view the safety number and I'm blocking it out so you all can't see it but Jordan's going to see the same number on their screen as well the only time this number is going to change is if someone let's say Jordan

**3:17** · installs signal on a new phone and then they're going to get a new safety number which is going to reset our safety number the reason this is important is if Jordan's signal account was ever compromised and someone was able to essentially impersonate Jordan um I would have a brand new signal safety number and if that happened signal will actually warn me um that my safety number is no longer verified then I should not send the message until I

**3:42** · reverifying this QR code or you can compare the numbers directly you might be wondering how you verify this if you just started talking to someone on Signal this only works if you have an already established safe place to communicate if you've been messaging your friend on iMessage for years and you're migrating to Signal you would share the safety number with each other on iMessage and approve each other there

**4:04** · the best case scenario is you compare these numbers in person with the other person with a QR code or you can just Compare the numbers by eye and if the number ever changes again signal will prevent you from messaging them until you

**4:20** · reverifying security of your end to-end encryption between your contacts even if it's a bit inconvenient to set up um I do highly suggest for the best safety you agree on on a protocol with your contacts in advance on what to do in case the safety number ever changes so you both know what to do and how to communicate in the event that someone's possibly compromised next up is a bit of endpoint security with some basic configuration settings and signal so if somebody gets a hold of your device while it's unlocked they can simply open

**4:49** · The Signal app and look at your conversations this is a super easy thing to fix um with the screen lock options so you're going to go into your settings you're going to go into privacy and you're going to turn on the screen lock here you also have the option for a timeout so the shorter the interval the more often you're going to have to use your phone's credentials to log into signal but it is technically more secure so it's your call what you want to do I have mine set to 30 minutes but you can do shorter if you want something a little bit more secure on a similar note and in a very similar location signal

**5:20** · allows you to prevent a preview of the app being shown in the app switcher to avoid a situation where you don't want a sensitive conversation exposed when navigating your phone if I pull up my note to self and I swipe up to the multitasking panel you'll see that signal is hidden and that's because of that screen security feature you enable that right here the hid screen and app switcher on Android uh this will also prevent screenshots of signal on your own Android device so you won't be able to take screenshots or screen record things within signal if you have the screen security enabled now even if you do these security features and you have

**5:51** · a strong password to get into your phone anyone can still read your messages and sender names from your lock screen depending on your phone's configur configuration within signal you can hide message content and sender name or just message content itself depending on what you want so you're going to go into your notifications you're going to go to show and you can change what signal will actually show in the notifications through signal do keep in mind though that on both iOS and I believe most Android devices they have their own options that make this less of an issue

**6:22** · um these can actually be a better solid Middle Ground so you can essentially allow all the notification content with signal which means you'll get names content and actions but only on an unlocked device and those are the basics if you do these things you're already better than most people and there's no issue in calling it good there but for people who need more protection we're going to dive into signals built-in configuration options but the advanced version many of these will only help in Niche scenarios or they're inconvenient to use for many users but that doesn't

**6:51** · mean they don't apply for some people so let's get into it so while Communication in signal is and encrypted which protects pretty much the communication in transit the messages are still available on each device unless they are manually deleted to avoid having all your messages just stored in this place for an indefinite amount of time it is good practice to set up a feature called disappearing messages and Signal settings so that any chats you start will disappear after a specified amount of time has passed do note that

**7:20** · disappearing messages disappear for everyone in the chat so it's not just on your side so make sure that all your contacts are aware of this so if you want to do this this on a per contact basis go into your chat settings with a specific person this also works in your note to self for people who use signal note toelf and you just select disappearing messages and you can set a custom time where you can do one of the pre-selected ones it's also worth mentioning that you can change this on the Fly for more sensitive conversations you want to disappear sooner so if I

**7:49** · want to send like a password to somebody I can set it to 30 seconds go here and I can put in password send it that'll disappear in 30 seconds and you can actually see the count there um next to the read receipt start to move and then I can go here and set it back to 2 weeks which is what I had it set to and now we're going to see it disappear right now boom password's gone so you can do that on a per contact basis or if you go

**8:15** · into your settings and you go to privacy and disappearing messages you can set a global default I opt to use four weeks here as a Baseline and then I can adjust from there per contact so some contacts might be one week some of them might be one day but I have just kind of Baseline of 4 weeks so everything by default disappears is in my signal client which is a pretty cool little workflow one final tip is that signal has Snapchat like functionality when it comes to sending photos so if I take a photo here you can set this to 1x on the bottom right and then I can send it and it's a

**8:46** · 1x media I can't view it here but if it was to another person they would open it and then it would disappear and they can't view it again kind of like Snapchat and that works independently of your disappearing messages so if this was set to two weeks and you sent the 1X photo they could view it 13 days later

**9:02** · but only once it works independently of the other feature so by default signal when you make a phone call may share your IP address with your contacts this isn't a big deal assuming you trust your contacts but in the event you want more protection against this built directly into signal signal does allow you to relay all calls through a signal server

**9:22** · to avoid repeat revealing your IP address to your contact it may reduce call Quality though I haven't done experiments side to side to know how much of a different it makes but if you want to enable this you go into your privacy settings you're going to scroll down to Advanced and then you're going to see here always relay calls one important thing here even if you have this off for incoming calls from people who aren't in your contacts it will always be relayed through signal no matter what so that a random person can't just call you to get your IP address there are two quick things here that only apply to iOS so signal allows

**9:54** · you to see your call history from your phone app on iOS depending on your iCloud configuration this may sync your call history with iCloud which some people might not want so just confirm it's off if you want to be safe go into your privacy settings scroll down and you're going to see calling here show calls in recents make sure that's off if you don't want to synchronize to the phone app the second iOS integration that isn't inherently a problem but maybe depending on your threat model is sharing contacts with iOS if you enable this uh iOS will be able to access your

**10:25** · signal contacts and features for suggestions and whatnot it's a nice bonus protection for those who want it you can find it in chats you're going to see share contact with iOS I have this enabled because I don't think it's a huge deal for myself but for people who want to keep all their signal contacts within signal and not have it possibly linked to the operating system then you can turn that off now if you just laughed at iOS users because you didn't have to do the last option I have a fun option for you Android users to look at next so on some Android devices you can turn on Incognito keyboard in privacy

**10:55** · and Incognito keyboard to enable an optional keyboard privacy flag that's provided by the operating system this makes it so your keyboard app may stop learning from your input entries may not be saved and autocorrect may be less reliable to help improve your privacy within the signal app essentially your keyboard's less likely to collect uh what you're typing within signal keep in mind though that keyboard apps don't actually have to respect this option it's kind of like do not track on websites it's like please don't track me but keyboards can ignore it ultimately I

**11:23** · would say you have a lot of trust in your keyboard app in general so just make sure you have a safe keyboard app on your Android device signal also offers the ability to retrieve previews of web pages linked within a conversation to generate a nice pretty preview you can see this if I type out our website tech.

**11:38** · Tech it generates a little preview image and it's pretty cool there is a slight problem with this though which is that websites that you input into this to generate a preview can retrieve basic information about you as if you were visiting the website directly you can disable link previews if this is a concern of yours by going into chats and then and also uh disabling generate link previews keep in mind that link previews are generated locally on your device meaning that

**12:07** · theoretically your contacts can still keep this enabled and still send you PR pretty messages with the link previews but that won't jeopardize you because the preview is being generated on their end before they send the message it's not actually fetching on your end so you might still see pretty messages you just can't send them this is a very Niche

**12:25** · privacy concern that not everyone needs to concern themselves with unless their threat metal calls for it if you feel like it's safe enough to access the website it's probably fine to access it through signal but again just keep it in mind that when you're generating a link preview it is uh pinging the website when you do that and now we're going to get to the more lesser known signal device that is found outside of signals default privacy and Security Options and as you might guess many of these options are geared towards higher threat models and likely aren't necessary for most people but for those who need it or those who are just curious and want to have fun let's get into it so first you

**12:57** · either want to ensure you have automatic updates for signal or you have your own method of getting updates as soon as possible signal regularly patches security issues and you want to make sure you're always using the newest version on a similar note leaving your signal app a bit ensure that you're on secure operating systems that are also receiving active security updates it's also important and on all of your signal devices make sure you have a strong password to get into your device enable fold dis encryption on devices that don't use it by default like most desktop operating systems you have to enable it you also want to reboot your

**13:28** · device as frequently as as well especially mobile devices in the event that you get malware installed in your device a daily reboot can sometimes remove the malware from your device thanks to built-in protection in your devices to prevent persistent malware so do reboots I do suggest enabling things like wipe device after 10 attempts which is something on iOS you can do to help avoid someone breaking into your phone with repeated attempts finally make sure you're doing encrypted device backups uh especially if you're somehow including signal as part of your backup process if

**13:57** · signal is included in that process without encryption then someone can get access to your messages from the backup instead of needing to break anything directly so just keep that in mind for more endpoint security we just covered some Basics but let's chat about some device specific endpoint Security on iOS and other Apple devices you have access to lockdown mode I've made a whole video on lockdown mode what it does what it doesn't do and what it's like to use as

**14:20** · someone who uses it lockdown mode will in many ways Elevate the security of your Apple devices and it's one more step you can take to protect the endpoint security I'll leave that video in a card there and on Android you have access to Google's Advanced Protection Program which can offer some security benefits as well on Android some users may prefer to go the custom ROM route but keep in mind not all ROMs are created equal so make sure you're choosing trusted ROMs to keep you safe if you're not sticking with something like stock Android so a VPN can actually be nice for a couple things first we chatted earlier about call relaying to

**14:50** · avoid your IP address being sent to your contacts we talked about how to enable that if you want to alternatively use a VPN then you can go that route instead instead of relying on the signal server to do it for you you can also use both to maximize your protection the other consideration which is for a very extreme Edge case um in particularly novel research is to prevent a unique side Channel attack so some researchers were recently able to pinpoint General locations of contacts based on delivery

**15:19** · times of messages it doesn't say this in the research directly but based on my understanding of how they pulled off this attack a VPN might obfuscate delivery times at least partially to make attack like this harder to pull off I can't express how advanced this is and how you probably don't need to worry about this I mostly just find it fascinating but it's something I'm including as an FYI for those who need more robust IP protection there's also

**15:44** · tour which you can access through services like Orbot on both IOS and Android so those are your options now out of principle Please be aware that every device you link to your signal account is one more device that opens you up to security issues so just out of principles try to reduce your attack Surface by keeping signal on as few devices as you can you can take this a step further because uh security model

**16:08** · of mobile operating systems especially um when signals involved is just a lot more compatible with keeping you safe so for those needing the utmost protection try to stick to mobile only signal workflows I just covered a recent desktop vulnerability that allowed an attacker to duplicate your active signal desktop session to their own device and

**16:27** · they can receive and send new messages on a totally different device and you don't even see it in your linked devices it's pretty crazy um I'll leave that in the card desktop operating systems also typically don't have as much protection when it comes to letting other programs Access Data from each other and desktops have a harder time preventing persistent malware so it's things like this that make mobile devices a bit more compelling for security purposes but um again a lot of people might need signal on their desktop just be aware it's not quite as secure as just the phone might be now down to the two final hard tips

**16:59** · of the video the first is your registration number which is half of what someone needs to log into your signal account during the AI in trilo data breaches some users were at risk of their signal accounts being logged into signal actually had to reach out to these impacted users to alert them of the problem now even in the worst case scenario someone still wouldn't get access to your message history your profile information or your contact list

**17:23** · even if they got in but especially if you enable registration lock and have an account pin like we covered how to do earlier in the video again it's going to be in your account settings set up a pin set up a registration lock but for some of you you may want to take this to the next level to avoid this kind of issue in the first place and the way you do that is by getting a number that's only used for exclusively signal and nothing else which is also hidden from everyone like we covered earlier with a username

**17:51** · this means that your login number for your signal account is OB fiscated and hidden from just about everybody to do this uh I personally use a viip service I like my sudo but you can also use Google Voice and there's a ton of other viip services out there signal is not picky whatsoever with viip phone numbers so most if not all numbers should work in short treat your signal number like a part of your password and make sure it's kept private if you want to be extra safe with your login credentials but I

**18:20** · want to remind you that most of the benefit is right here with your registration lock and your PIN if you're just someone that wants to go a little bit further then you try to opis get your phone number beyond that and now we're on our final hardening tip on Android you can consider using Molly which is a fork of the signal mobile client with a few extra features so I

**18:39** · want to mention Molly is independent they are a signal Fork they are not from signal but it does have some features like locking the app at rest securely shredding unused Ram data and they also have a direct route via tour another cool benefit to Molly that really was nice for me is you can set up Molly as a linked device so for those of you who are compartmentalizing between m mobile phones especially if you're an IOS and Android User you can actually use signal on two mobile phones with Molly being one of them which is traditionally not something you can do uh signal doesn't

**19:09** · let you set up two phones um so that feature alone can open up other privacy and Security benefits in other places because now you can compartmentalize things further and still have access to the same signal account but that's not a guarantee for everybody it's just for people like me where you can get a nice benefit from that now there is a trade-off though because now now like we covered earlier you have a larger attack service with signal being on two mobile phones now and it's not all sunshines and rainbow because Molly is now another

**19:39** · party you're trusting and there will always be a delay in security updates even if it's minimal um because you're not getting those updates from a primary party so yes Molly can and I really want to emphasize here can make your signal usage more secure but it's very personal preference depends on where you're trying to maximize your safety and it kind of depends on your workflow and your general configuration so that's

**20:02** · what I have to say about Molly I think it's a great service great client just be aware that it's not for everybody and it doesn't solve every problem it's just a possible tool that can help your signal account be a little bit more secure if you're the right person for it now I want to remind everyone watching that signal is one of the safest Messengers you can use uh they're Court proven they offer some incredibly welcome privacy and Security benefits natively but I hope that this guide can help you take it to the next level it was somewhat inspired by that last video I did with the security issue that they

**20:31** · had on desktop and I figured well a lot of people don't know how to make signal more secure so um that's when this guide came about for those wondering where this guide came from It's a combination of my own experience using signal for years along with a few other signal guides that I'll link in the description from freedom of the press privacy guides and the CT EU team those are also great

**20:49** · guides they're down below I also want to shout out again my video comparing signal to a ton of Messengers uh I'll leave that in either a card or down in the description so you can see if any other messenger may actually be better for you in certain situations I also want to push you to our become Anonymous guide which is a great guide showing you kind of similar tips but for pretty much your entire digital life not just signal and finally I want to thank all of our patrons which you can also be one too to help support this content and keep it free for everyone and allow us to do things like this I want to thank our

**21:19** · supporters on other support platforms like Kofi librae Monero and many others and finally I want to thank our gold sponsor notes snook for sponsoring our content I'll see you all next time on Tech give this a thumbs up took a lot of time and I hope it benefits some people out there see you next time
