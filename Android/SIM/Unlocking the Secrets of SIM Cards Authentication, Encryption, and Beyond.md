______________________________________________________________________

title: "Unlocking the Secrets of SIM Cards: Authentication, Encryption, and Beyond"
source: "https://medium.com/@ali.pourbazargan/unlocking-the-secrets-of-sim-cards-authentication-encryption-and-beyond-4d7c8d8b3c58"
author:

- "\[[Ali Pourbazargan]\]"
  published: 2024-04-18
  created: 2026-05-14
  description: "TL;DR: This article delves into the role of SIM cards in mobile security, primarily focusing on identity authentication and the complex encr"
  tags:
- "sim"

______________________________________________________________________

![](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*VgcLUVE_lNCyi4PtNQ4sfg.jpeg)

by DALLE!

**TL;DR:** This article delves into the role of SIM cards in mobile security, primarily focusing on identity authentication and the complex encryption mechanisms they utilize. It explains how SIM cards store critical data and manage secure communication independently from the device’s CPU and baseband. Key processes such as the authentication sequence, encryption key generation, and security protocols are discussed, illustrating how SIM cards safeguard against unauthorized access and ensure secure mobile communication.

Three weeks ago, I had no idea what a SIM card really is or how it works. At best, I thought it was a memory chip used to store just a few things like identity numbers and a small amount of storage for contacts, which nobody uses anymore.

My curiosity was piqued while I was researching RF in mobile broadband — how it works and whether it is possible to crack it. During this process, I discovered that the radio communications in mobile phones are handled by an independent chip called the baseband. I already knew a bit about the baseband, but what was new to me was learning about a chip that operates completely independently from the main CPU. This chip communicates between networks and SIM cards, relaying only the final, decoded, ready-to-use results to the CPU.

So, I’ve decided to break this project into several phases, starting from scratch with communication between phones and SIM cards. Then, I’ll explore what this thing really is and how it works in normal phone usage.

My basic understanding was that when I turn on my device, it reads the specific number (IMSI) stored on my SIM card and uses it for subsequent communications. However, if you think about it for more than five seconds, you realize this is quite dangerous because if an attacker knows this number, it is enough to hijack your identity. Fortunately, the authentication process is more complicated, and most importantly, it is conducted directly on the SIM card chip!

## What is in it?

SIM cards feature a microprocessor with 8–16 bits and a speed of 10–30 MHz, along with about 512 KB of memory. This memory is used to store read-only information such as the IMSI, Authentication Key (Ki), and phone number, as well as contacts and SMS messages you have saved on it. It usually operates at 1.8-5 volts, depending on the SIM card’s specifications.

## Initial Registration

The main duty of a SIM card is to authenticate the owner on the mobile network. Let’s see how this happens.

**Scanning networks:**

When the phone turns on, it begins scanning broadcast packets to gather basic information about the surrounding cell towers. Since the SIM card contains information about the home network (the network to which your SIM card belongs) and suggestions for other networks (in case of roaming), it decides to initiate authentication with one of them.

**Asking to start the process:**

1. Random Access Channel (RACH):

The process starts by sending a message as a random access channel (RACH) that indicates the device’s intention to initiate communication.

2\. Initial NAS (Non-Access Stratum):

The network sends back a response, and if it is successful, the device sends a request. This request is a signaling message that includes the IMSI. This message is part of the NAS protocol, which operates above the access (radio) network protocols.

3\. Session Establishment:

The network verifies the IMSI, checks the subscriber’s status, and either accepts or denies the registration. If accepted, the network sends an accept message that may include an assigned TMSI for future communications.

## Authentication

Once the network has the IMSI (or TMSI if the IMSI has been previously established and a temporary identity can be used instead) generate some vectors like the below:

**RAND**: is a binary value and is typically represented as a string of 16 bytes (128 bits). It is a randomly generated number by the network’s Authentication Center (AuC).

Although it’s binary data, for practical purposes in documentation or during analysis, it is often displayed as a hexadecimal string. For example, a RAND might look something like this: `AF 34 9C 56 BA CD 12 78 90 EF AB 34 CD 56 EF 78`.

**AUTN:** is also a binary value, typically 16 bytes long, just like RAND. It verifies that the RAND was sent by a legitimate network and has not been tampered with.

AUTN is usually represented as a hexadecimal string. An example AUTN might look like this: `5A 6B AF 34 9C 56 12 78 90 EF CD AB 34 56 EF 78`.

**XRES** (Expected Response): The response that the network expects to receive if the SIM card is valid.

**Authentication Request:**

The network sends an Authentication Request message to the device, which includes the RAND and AUTN.

## Get Ali Pourbazargan’s stories in your inbox

Join Medium for free to get updates from this writer.

**SIM Card Processing:**

The SIM card uses its stored secret key (*Ki*) and the received RAND to compute a response using the same algorithm (Usually A3) that the network used to generate the SRES and A8 algorithm to generate Kc (Ciphering Key). The SRES will be sent back to the network to verify the RAND challenge and Kc has local usage to encrypt and decrypt voice and data communication traffic.

**How Kc is Used**

Kc is used to generate the encryption stream for the A5 algorithm, which is the algorithm responsible for encrypting the data transmitted between the mobile and the network. Since both the network and the device calculate the Kc independently using the same inputs (RAND and *Ki*), they both synchronize their encryption and decryption processes without the need to exchange the ciphering key itself. This arrangement allows the mobile device and the network to establish a secure communication channel, maintaining confidentiality and integrity of the communications without risking the exposure of critical cryptographic material.

The algorithms (A3 and A8) are not public, and their implementations are specific to each operator. For the sake of illustration, let’s assume a simple operation to compute these values. In practice, these would be done using proprietary cryptographic functions.

## Hypothetical Calculation (Pseudo-code)

Let’s create a simplified pseudo-code for calculating SRES and Kc using RAND and Ki:

```c
def simple_A3_A8(rand, ki):
    # Simulating a cryptographic function for A3/A8
    sres = hash_function(rand + ki)[:4]  # Taking first 4 bytes for SRES
    kc = hash_function(rand + ki)[4:12]  # Taking next 8 bytes for Kc
    return sres, kc

# Example using hexadecimal values for RAND and Ki
rand = "AF349C56BACD127890EFAB34CD56EF78"
ki = "0F1571C947D9E8590CB7ADD6AF7F6798"

sres, kc = simple_A3_A8(rand, ki)
```

**SRES (Signed Response):**

The computed signed response is sent back to the network for verification.

## Network Verification

The network compares the SRES received from the mobile device with the XRES (Expected Response) it computed using the same RAND and the *Ki* it has associated with the IMSI of the subscriber.

If the SRES matches the XRES, the authentication is deemed successful. The mobile device is considered legitimate, confirming that it holds the correct *Ki* and is authorized to access the network.

If the SRES does not match the XRES, the authentication fails. This failure might lead to the mobile device being denied access to the network services, and typically, the network may request another attempt or deny services based on security protocols.

## After Successful Authentication:

**Sync encryption config:**

Following successful authentication, the network sends a command to the mobile device to establish or configure security settings. This includes selecting encryption and integrity algorithms.

**Generating a TMSI:**

To enhance privacy and security, the network might assign a new TMSI (Temporary Mobile Subscriber Identity) to replace the IMSI for internal network communications. This TMSI is then used in all future interactions with the network to help protect the subscriber’s identity. The network sends the new TMSI to the device in an encrypted format, using the newly established encryption method.

**Setup communication channels:**

The network proceeds to set up the bearers (communication channels) for voice and data services. This includes allocating bandwidth and other resources necessary for the device to begin communication services.

**Service Initiation:**

Once all the security and resource setups are completed, the mobile device is ready to initiate voice calls, send SMS, and use data services securely encrypted by the established keys and algorithms.

**Periodic Updates:**

To maintain security and service availability, the mobile device and network periodically perform location updates and re-authentication. This ensures that the mobile device is continuously authorized to use the network as it moves across different network cells or changes its status.

## Conclusion

As you can see, the responsibility of a SIM card is not just to store information and data; it continuously authenticates and generates suitable encryption/decryption tokens independently of the device’s CPU and even the baseband, all within the SIM card itself. It’s important to note that this process repeats periodically based on the network’s security policy, especially as you move and switch between cell towers. You might wonder about eSIMs (Embedded SIMs). They are essentially the same type of chips, soldered into devices, but with additional functionality to synchronize with new operators selected by the user.

It was also interesting to learn that these communications between the network, the device, and the SIM are handled by the baseband chip, and the device’s main CPU and OS have no idea what’s happening behind the scenes. Therefore, you cannot monitor their communications like you would other network protocols using tools like Wireshark.

In this article, I’ve focused on identity authentication, which is the main function of SIM cards. However, if you delve into the beauty behind this, you’ll find there is much more to learn. For example, SIM cards have the ability to run Java applications written in a specific version of Java called Java Card, and use the SIM Toolkit API (STK). Isn’t that amazing?
