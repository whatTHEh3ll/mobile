---
title: "LTE RSRP, RSRQ, RSSI Calculator"
source: "https://custommapposter.com/article/lte-rsrp-rsrq-rssi-calculator-arimas/2420"
author:
published: 2026-05-15
created: 2026-05-15
description: "In this page we present a simpleLTE RSRP & RSRQ calculator. The calculation is performed based on RSSI and channel Bandwidth considered. The formulas used in within the calculator is below, where:RSRP is the Reference Signal Received Power and is measured in a single REof the LTE REsource Block.Henc..."
tags:
  - "clippings"
---
In this page we present a simple **LTE RSRP & RSRQ** calculator. The calculation is performed based on RSSI and channel Bandwidth considered. The formulas used in within the calculator is below, where:

See Also

[How to Determine Good Cellular Signal Strength](https://custommapposter.com/article/how-to-determine-good-cellular-signal-strength/2420)

-  [**RSRP**](https://arimas.com/78-rsrp-and-rsrq-measurement-in-lte/) is the Reference Signal Received Power and is measured in a single REof the LTE REsource Block.Hence, RSRP is also called as average received power of a single reference signal RE (Resource Element)
- [**RSRQ**](https://arimas.com/78-rsrp-and-rsrq-measurement-in-lte/) is the Reference Signal Received Quality
- [**RSSI**](https://arimas.com/78-rsrp-and-rsrq-measurement-in-lte/) is measured over entire bandwidth of occupied RBs (Resource Blocks)

### LTE RSRP and RSRQ CALCULATOR EXAMPLE:

- **Input**: BW = 10 MHz, RSSI = -79 dBm
- **Outputs**: RSRP (dBm) = -106.78 dBm; RSRQ (dBm) = -10.79dBm; PRBs/BW = 50

### LTE RSRP and RSRQ CALCULATOR formula or equations

Following equations are used in the calculator:

#### RSRP=RSSI – 10LOG(12\*N)

#### RSRQ = N\*(RSRP/RSSI) or RSRQ = 10LO(N) + RSRP(dBm) – RSSI(dBm)

Where:

- **N** = Number of RBs as per Channel Bandwidth
- **RSRP** = Average Received Signal Power of a a Singel Resource Element (RE) – In LTE there are 84 RE in a single RB
- **RSRQ** =Power measured over the entire BW of occuped RBs

For any further details please refer to:

See Also

[Field Test Mode: What it is and How To Enable it on Your Phone](https://custommapposter.com/article/field-test-mode-what-it-is-and-how-to-enable-it-on-your-phone/2420) [Understanding LTE Signal Strength Values](https://custommapposter.com/article/understanding-lte-signal-strength-values/2420) [How to improve RSRP signal strength?](https://custommapposter.com/article/how-to-improve-rsrp-signal-strength/2420)[RSSI values for good/bad signal strength - Mist](https://custommapposter.com/article/rssi-values-for-good-bad-signal-strength-mist/2420)