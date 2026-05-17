______________________________________________________________________

title: "Understanding LTE Signal Strength Values (2026)"
source: "https://custommapposter.com/article/understanding-lte-signal-strength-values/2420"
author:
published: 2026-05-15
created: 2026-05-15
description: "Below is a chart that shows what values are considered good and bad for the LTE signal strength values:Below are explanations of these values (and also RSSI in relation to LTE):SINR/SNR – The signal-to-noise ratio of the given signal.RSRP – The average power received from a single Reference signal,..."
tags:

- "clippings"

______________________________________________________________________

Below is a chart that shows what values are considered good and bad for the LTE signal strength values:

![Understanding LTE Signal Strength Values (1)](https://www.digi.com/getattachment/Support/knowledge-base/understanding-lte-signal-strength-values/Chart.png?lang=en-US "Understanding LTE Signal Strength Values (1)")

Below are explanations of these values (and also RSSI in relation to LTE):

**SINR/SNR** – The signal-to-noise ratio of the given signal.
**RSRP** – The average power received from a single Reference signal, and Its typical range is around -44dbm (good) to -140dbm(bad).
**RSRQ** – Indicates quality of the received signal, and its range is typically -19.5dB(bad) to -3dB (good).
**RSSI** – Represents the entire received power including the wanted power from the serving cell as well as all cochannel power and other sources of noise and it is related to the above parameters through the following formula:

See Also

[Field Test Mode: What it is and How To Enable it on Your Phone](https://custommapposter.com/article/field-test-mode-what-it-is-and-how-to-enable-it-on-your-phone/2420) [LTE RSRP, RSRQ, RSSI Calculator - arimas](https://custommapposter.com/article/lte-rsrp-rsrq-rssi-calculator-arimas/2420) [How to improve RSRP signal strength?](https://custommapposter.com/article/how-to-improve-rsrp-signal-strength/2420)[RSSI values for good/bad signal strength - Mist](https://custommapposter.com/article/rssi-values-for-good-bad-signal-strength-mist/2420)

**RSRQ=N\*(RSRP/RSSI)**

Where N is the number of Resource Blocks of the E-UTRA carrier RSSI measurement bandwidth.
