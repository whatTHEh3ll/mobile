---
title: "5G networks: A comprehensive cheat sheet"
source: https://www.techrepublic.com/article/5g-mobile-networks-a-cheat-sheet/
author:
  - "[[TechRepublic Staff]]"
published: 2022-08-23
created: 2026-05-15
description: Looking for a guide on 5G networks? Get an introduction to 5G networks with our comprehensive cheat sheet.
tags:
  - Android
---
Looking for a guide on 5G networks? Get an introduction to 5G networks with our comprehensive cheat sheet.

With the advent of widespread [Internet of Things](https://www.techrepublic.com/article/internet-of-things-iot-cheat-sheet/) adoption in enterprise applications including manufacturing, agriculture, healthcare and more — alongside an increasing dependence on smartphones and [always-connected computers](https://www.techrepublic.com/topic/hardware/) — the constraints of 4G LTE technology prompted mobile network operators to embark on [an accelerated rollout of 5G communications](https://www.techrepublic.com/topic/5g/) to keep pace with the current and upcoming network demands.

This cheat sheet is an introduction to 5G mobile networks, as well as their benefits and challenges. The article will be updated periodically as new 5G technologies are standardized and as mobile network operators deploy 5G networks worldwide.

## What is 5G?

5G refers to the fifth generation of mobile phone networks. It’s a standard for transmitting data, whereas calls and SMS messages still go through 3G or 4G networks.

Since the introduction of the first standardized mobile phone network in 1982, succeeding standards have been adopted and deployed approximately every nine years. GSM, the 2nd generation wireless network, was first deployed in 1992, while a variety of competing 3G standards began deployment in 2001. The 4G LTE wireless technology standard was deployed by service providers in 2010.

Now, technology companies and mobile network operators have actively deployed 5G cellular networks around the world for new mobile devices. These 5G deployments accompany transitional LTE technologies such as LTE Advanced and LTE Advanced Pro, which are used by network operators to provide faster speeds on mobile devices.

**SEE:** [**Top keyboard shortcuts you need to know (free PDF)**](https://www.techrepublic.com/resource-library/downloads/top-keyboard-shortcuts-you-need-to-know-free-pdf/?r=1752442988) **(TechRepublic)**

Principally, 5G refers to “5G NR (New Radio),” which is the standard adopted by 3GPP, an international cooperative responsible for the development of the 3G UMTS and 4G LTE standards. Other 5G technologies do exist. Verizon’s 5G TF network operates on 28 and 39 GHz frequencies and is used only for fixed wireless broadband services, not in smartphones. Verizon’s 5G TF deployments [were halted in December 2018](https://www.techrepublic.com/topic/5g/) and will be transitioned to 5G NR in the future. Additionally, 5G SIG was used by Korean Telecom provider KT for a demonstration deployment during the 2018 Winter Olympics in Pyeongchang.

### Mobility must-reads

- [Big Apple OS Makeover: Here’s What to Expect & When](https://www.techrepublic.com/article/apple-operating-system-revamp/)
- [MWC 2025: Nothing Shows Off (3A) Phones With AI Organization Tool](https://www.techrepublic.com/article/nothing-phone-3a-essential-space/)
- [Bad News for App Developers: Most Apps Fail to Hit $1,000 Monthly Revenue Within Two Years](https://www.techrepublic.com/article/news-apps-revenue-developers/)
- [Mobile Device Computing Policy](https://www.techrepublic.com/resource-library/whitepapers/mobile-device-computing-policy/)

5G NR allows for networks to operate on a wide variety of frequencies, including the frequencies vacated by decommissioning previous wireless communications networks. The 2G DCS frequency bands, the 3G E-GSM and PCS frequency bands and the digital dividend of spectrum vacated by the transition to digital TV broadcasts are some of the bands available for use in 5G NR.

5G standards divide frequencies into two groups: FR1 (450 MHz – 6 GHz) and FR2 (24 GHz – 52 GHz). Most early deployments will be in the FR1 space. Research is ongoing into using FR2 frequencies, which are also known as extremely high frequency or millimeter wave frequencies. Discussions of the suitability of millimeter wave frequencies have been published in IEEE journals as far back as 2013.

Millimeter wave frequencies allow for faster data speeds, though they do come with disadvantages. Because of the short distance of communication, millimeter wave networks have a much shorter range; for densely-populated areas, this requires deploying more base stations. While this would be advantageous in certain use cases, it would be a poor fit for use in [rural areas](https://www.techrepublic.com/topic/5g/). Additionally, millimeter wave communication can be susceptible to atmospheric interference. Effects such as rain fade make it problematic for outdoor use and even nearby foliage can disrupt a signal.

For mobile network operators, the 3GPP has identified three aspects for which 5G should provide meaningful advantages over existing wireless mobile networks. These three heterogenous service types will coexist on the same infrastructure using network slicing, allowing network operators to create multiple virtual networks with differing performance profiles for differing service needs.

### eMBB (Enhanced Mobile Broadband)

Initial deployments of 5G NR focused on eMBB, which provides greater bandwidth, enabling improved download and upload speeds, as well as moderately lower latency compared to 4G LTE. eMBB will be instrumental in enabling rich media applications such as mobile AR and VR, 4K and 360° video streaming and [edge computing](https://www.techrepublic.com/article/edge-computing-the-smart-persons-guide/).

### URLLC (Ultra Reliable Low-Latency Communications)

URLLC is targeted toward extremely latency sensitive or mission-critical use cases, such as factory automation, robot-enabled remote surgery and driverless cars. According to a [white paper](https://arxiv.org/pdf/1801.01270.pdf) by Mehdi Bennis, Mérouane Debbah and H. Vincent Poor of the IEEE, URLLC should target 1ms latency and block error rate of 10−9 to 10−5, although attaining this “represents one of the major challenges facing 5G networks,” as it “introduces a plethora of challenges in terms of system design.”

Technologies that enable URLLC are still being standardized and were outlined further in [3GPP Release 16](https://www.3gpp.org/release-16).

### mMTC (Massive Machine Type Communications)

mMTC is a narrowband access type for sensing, metering and monitoring use cases. Some mMTC standards that leverage LTE networks were developed as part of 3GPP Release 13, including eMTC and NB-IoT. These standards will be used in conjunction with 5G networks and extended to support the demands of URLLC use cases on 5G networks and frequencies in the future.

The ways in which 5G technologies will be commercialized are still being debated and planned among mobile network operators and communications hardware vendors. As different groups have differing priorities, interests and biases, including spectrum license purchases made with the intent of deploying 5G networks, the advantages of 5G will vary between different geographical markets and between consumer and enterprise market segments.

### Proactive content caching

Particularly for millimeter wave 5G networks, which require deploying more base stations compared to LTE and previous communications standards, those base stations in turn require connections to wired backhauls to transmit data across the network. By providing a cache at the base station, access delays can be minimized and backhaul load can be reduced. This has the added benefit of reducing end-to-end delay. As 4K video streaming services — and smartphones with 4K screens — become more widespread, this caching capability will be important to improve quality of service.

### Multiple-hop networks and device-to-device communication

In LTE networks, cellular repeaters and femtocells bridge gaps in areas where signal strength from traditional base stations is inadequate to serve the needs of customers. These can be in semi-rural areas where population density complicates serving customers from one base station, as well as in urban areas where architectural design obstructs signal strength. Using multiple-hop networks in 5G extends the cooperative relay concept by leveraging device-to-device communication to increase signal strength and availability.

### Seamless vertical handover

Although proposals for 5G position it as the “one global standard” for mobile communications, allowing devices to seamlessly switch to a Wi-Fi connection or fall back to LTE networks without delay, dropped calls or other interruptions, is a priority for 5G.

Additional 5G standards in 3GPP [Release 17](https://www.3gpp.org/release-17) provides additional advantages for businesses and consumers using 5G, but due to the Coronavirus pandemic the completion of this release was delayed until earlier this year.

## How fast is 5G and what is the difference between 5G and 4G?

5G can be significantly faster than 4G, delivering up to 20 Gigabits-per-second peak data rates and 100+ Megabits-per-second average data rates. 5G has more capacity than 4G, and 5G is designed to support a 100x increase in traffic capacity and network efficiency.

It is vital to remember that 5G is not an incremental or backward-compatible update to existing mobile communications standards. It does not overlap with 4G standards like LTE or WiMAX and it cannot be delivered to existing phones, tablets or wireless modems by means of tower upgrades or software updates, despite AT&T’s attempts to brand LTE Advanced as “5G E.” While upgrades to existing LTE infrastructure are worthwhile and welcome advances, these are ultimately transitional 4G technologies and do not provide the full range of benefits of 5G NR.

For an overview of when 5G smartphones are being released, as well as the benefits and drawbacks of 5G smartphones, check out TechRepublic’s cheat sheet about 5G smartphones.

## What is the best 5G mobile network carrier?

In August 2022, Rootmetrics.com released a [report](https://rootmetrics.com/en-US/content/US-state-of-5G-1H-2022) awarding T-Mobile the slot of best U.S. 5G network in terms of speed and availability. It also indicated Verizon and AT&T have improved their offerings as well.

## What performance issues are involved with 5G?

Things have improved since the onset of 5G in terms of device power. Visermark.com [estimates](https://www.visermark.com/post/the-battery-life-impact-on-4g-and-5g-what-s-the-difference#:~:text=Since%20the%20launch%20of%20the,5SA%20than%204G%20as%20expected) that using 5G networks consumes about 10% more battery life than 4G. 9to5Mac.com provided this [chart](https://9to5mac.com/2022/03/21/5g-iphone-battery-life-impact/) outlining the power consumption on various iPhone models using 5G versus 4G which correlates with Visermark’s estimate.

Since Apple presents a closed system compared with the open environment Android is based upon, 5G battery consumption will vary across Android phones based on manufacturer, model, quality of connection and running apps.

If you’re interested in testing the battery consumption of 5G compared to 4G, charge your phone to 100% and then toggle between the two, generally under Settings / Network & Internet (or Connections) and then the option related to Mobile Networks. Use the phone on either network for two hours and compare the battery drain.

## What are the pros of 5G networks?

As previously stated, speed and greater bandwidth are the primary benefits along with lower latency and greater capacity where the carrier infrastructure is sufficient. In addition, 5G offers the ability to connect with a broad range of devices such as drones and sensors and can serve to drive interactive services such as artificial intelligence, machine learning, and augmented or virtual reality.

## What are the cons of 5G networks?

Aside from increased battery consumption, the very popularity of 5G is producing some latency issues. Research firm JD Power recently [found](https://www.jdpower.com/business/press-releases/2022-us-wireless-network-quality-performance-study-volume-2) the network quality decrease to be caused by the sheer number of devices operating on 5G networks. Slow operation and delays loading content were the most common issues found.

Granted this isn’t so much a limitation of 5G itself but rather the infrastructure behind them, and the solution here is to switch to Wi-Fi or 4G for less important tasks and for carriers to improve their capacity to support the increasing number of 5G users.

A strange twist in the saga of 5G entails claims that the electromagnetic waves it relies on can damage the human body, leading to cancer or other health problems. Forbes [addressed these concerns](https://www.forbes.com/health/body/is-5g-safe/) earlier this year presenting both sides of the argument, pointing out that “The World Health Organization and FDA declare 5G safe.”

In addition, while 5G has made great strides, there are still areas around the globe where it needs to branch out or improve existing capacity. 5G does not broadcast as far as 4G and can be interfered with by man-made or natural structures.

## Whom does 5G benefit?

### Remote workers and off-site job locations

One of the major focuses of 5G is the ability to use wireless networks to supplant traditional wireline connections by increasing data bandwidth available to devices and minimizing latency. For telecommuters, this greatly increases flexibility in work locations, allowing for cost-effective communication with your office without being tied to a desk in a home office with a wireline connection.

For situations that involve frequently changing off-site job locations, such as location movie shoots or construction sites, lower technical requirements for 5G deployment allow for existing devices to connect to a 5G router via Wi-Fi. For scenes of live breaking news, 5G technologies can be used to supplant the traditional satellite truck used to transmit audio and video back to the newsroom. Spectrum formerly allocated to high-speed microwave satellite links has been repurposed for 5G NR communication.

### Internet of Things devices and networks

One priority for the design of 5G networks is to lower barriers to network connectivity for IoT devices. While some IoT devices have LTE capabilities, the practical limitations of battery sizes that can be included in wearable devices and the comparatively high power requirements of LTE limit the usefulness of mobile network connectivity in these situations. Proposals for 5G networks focusing on reducing power requirements and the use of lower-power frequencies such as 600 MHz will make connecting IoT devices more feasible.

3GPP’s Release 16 included its [5G for Industry 4.0 standards](https://www.3gpp.org/news-events/2122-tsn_v_lan), which describe how 5G, as standardized by 4GPP, can be used in industrial IoT settings in cooperation with [IEEE time-sensitive networks standards](https://1.ieee802.org/tsn/) to build better IIoT networks.

### Smart cities, office buildings, arenas and stadiums

The same properties that make 5G technologies a good fit for IoT devices can also be used to improve the quality of service for situations in which large numbers of connected devices make extensive use of the mobile network in densely populated areas. These benefits can be realized easily in situations with variable traffic — for instance, arenas and [stadiums](https://www.techrepublic.com/resource-library/downloads/how-the-nfl-and-its-stadiums-became-leaders-in-wi-fi-monetizing-apps-and-customer-experience/) are generally only populated during sporting events, music concerts and other conventions. Large office towers, such as the 54-story Mori Tower in Tokyo’s Roppongi Hills district, are where thousands of employees work during the week. Additionally, densely populated city centers can benefit from the ability of 5G networks to provide service to more devices in physically smaller spaces.

### ISP customers

High-band 5G, described above as mmWave, has its shortcomings, but its [speed is incredible](https://www.techrepublic.com/topic/5g/) compared to even mid- and low-band 5G. Because it only has a range of 1,500 feet, it’s not practical for use with mobile devices, but it could become a wireless solution for home and office internet that eliminates the need for wiring telecom cables to homes.

## How secure are 5G networks?

5G’s transport security algorithms are more robust than their 4G predecessors. Encryption is used to protect data across the board. That being said, the popularity of 5G invariably means that as more devices are connected, the chance of cybersecurity attacks will increase. The diversity of such devices as IoT, drones, sensors and others means that there is a broader attack surface with which to exploit any found vulnerabilities.

**SEE:** [**Mobile Device Security Policy**](https://www.techrepublic.com/resource-library/downloads/mobile-device-security-policy/?r=783534122) **(TechRepublic Premium)**

That goes for related software and virtual hardware as well. As these components are integrated with 5G, they might be exposed to risk as well. Devices operating on 5G could also be a cause for security-related concerns, as hardware components could be compromised via malware by malicious individuals.

A white paper from [Ericsson.com](https://www.ericsson.com/en/reports-and-papers/white-papers/5g-security---enabling-a-trustworthy-5g-system) lists “the five core properties that contribute to the trustworthiness of the 5G system: Resilience, communication security, identity management, privacy and security assurance.” Ericsson believes that these properties of the 5G system contribute toward creating a trustworthy communications platform that is an ideal foundation on which to build large-scale, security-sensitive systems, including those used in industrial settings.

Enterprises should also analyze the concept of “network slicing” to create virtual networks for hosting certain applications or services over their 5G networks.

As with any software, 5G management applications may be vulnerable to attacks as exploited, and it’s important to keep in mind that a compromised or breached carrier or enterprise infrastructure could result in a devastating impact. Private 5G networks are a promising option for companies seeking to reduce their risk footprints.

A centralized security operations division as well as consumer education should be implemented by companies to protect their workers utilizing company-issued or BYOD 5G devices via mobile device controls. Patching devices and related applications is a must to ensure continued security via 5G operations.

The security market for global 5G is expanding drastically, emphasizing the concerns over securing these networks as well as developments related thereto. GlobeNewswire produced a [report](https://www.globenewswire.com/news-release/2022/08/17/2499759/0/en/5G-Security-Global-Market-Report-2022-Increasing-Operator-Investments-for-Dynamic-Infrastructure-Demand-for-Private-5G-Across-Enterprises-Governments-and-Industrial-Sectors-Present.html) in August 2022 outlining the opportunities related to demand for private 5G across enterprise, governments and industrial sectors that stated: “The publisher forecasts the global 5G security Market size is expected to grow USD 1.3 billion in 2022 to USD 7.2 billion by 2027, at a Compound Annual Growth Rate of 41.6% during the forecast period.” This signifies the determination security companies have to ensure 5G meets business and consumer expectations.

***Note: This article was updated by Scott Matteson.***

[![TechRepublic Staff](https://assets.techrepublic.com/uploads/2023/10/cropped-TR_Flag_wbg_400x400.png?w=256)](https://www.techrepublic.com/meet-the-team/us/techrepublic-staff/)