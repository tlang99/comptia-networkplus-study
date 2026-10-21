### Wireless Frequencies

Wireless networks send and receive data as radio waves on different frequency bands:
* [[#^735fab|2.4 GHz band]]
* [[#^950978|5 GHz band]]
* [[#^9903fe|6 GHz band]]

| Band | Range | Penetrates solid objects | Channels |
| --- | --- | --- | --- |
| 2.4 GHz | Longest | Best | Many overlap. Only 1, 6, and 11 don't |
| 5 GHz | Shorter | Worse | 24 non-overlapping 20 MHz channels |
| 6 GHz | Shortest | Least | Even more channels, 20 to 160 MHz wide |

### 2.4 GHz Channels

Each band is divided into [[#^8110c1|channels]]. You don't need to remember the frequency of each channel, but you do need to know how many channels the 2.4 GHz band has, which depends on where you are in the world:
* US and Canada: channels 1 through 11
* Japan: channels 1 through 14
* Rest of the world: channels 1 through 13

NOTE: Many of the 2.4 GHz channels overlap. Channels 1, 6, and 11 do not overlap, and they should always be chosen to avoid interference. Important to remember for the exam.

### Other Frequency Features

* [[#^22743d|Channel bonding]]: merges neighboring channels into one wider channel
* [[#^17ee82|802.11h]]: uses [[#^0f5109|Dynamic Frequency Selection (DFS)]] and [[#^c18249|Transmit Power Control (TPC)]]
* [[#^8a51bd|Band steering]]: moves capable clients onto the faster, less congested bands

### Wireless Standards

[[#^4e0b42|802.11]] is the standard used for wireless networks, and it has several versions. Dion says to remember the name, frequency band, max speed, and max range of each one.

| Standard | Name | Band | Max speed | Range |
| --- | --- | --- | --- | --- |
| 802.11a | Wireless a | 5 GHz | 54 Mbps | 35 m |
| 802.11b | Wireless b | 2.4 GHz | 11 Mbps | 140 m |
| 802.11g | Wireless g | 2.4 GHz | 54 Mbps | 140 m |
| 802.11n | Wireless n | 2.4 and 5 GHz | 600 Mbps | 35 m |
| 802.11ac | Wi-Fi 5 | 5 GHz | Over 6.9 Gbps, uses MU-MIMO | |
| 802.11ax | Wi-Fi 6 | 2.4, 5, and 6 GHz | 9.6 Gbps, backward compatible with all previous types | |

By band:
* 2.4 GHz: b, g, n, and ax
* 5 GHz: a, n, ac, and ax
* 6 GHz: ax

NOTE: Dion says to ONLY rely on this info, not on vendor packaging, since vendors use marketing terms that can be misleading.

Newer standards use multiple antennas:
* [[#^a021f4|MIMO]]
* [[#^44bbb1|MU-MIMO]]

### Glossary

2.4 GHz Band: One of the most widely used frequencies for wireless networking. Known for long range and better penetration through solid objects. Many of its channels overlap. Channels 1, 6, and 11 do not. ^735fab

5 GHz Band: Contains frequencies from 5.725 GHz to 5.875 GHz, with 24 non-overlapping channels of 20 MHz each. Less interference and better performance, but shorter range, and it doesn't penetrate solid objects as well. ^950978

6 GHz Band: The newest band, ranging from 5.925 to 7.125 GHz. Offers even more channels and bandwidth for faster connections and less congestion. Each channel can be 20, 40, 80, or 160 MHz wide. Shortest distances and least object penetration. ^9903fe

Channel: The medium through which wireless networks send and receive data. Similar to a copper cable, but virtual. ^8110c1

Channel Bonding: Creates a wider channel by merging two or more neighboring channels into a single wider channel. Up to 8 channels can be bonded into a virtual channel 160 MHz wide. More susceptible to interference, however. ^22743d

802.11h Standard: Developed to comply with European regulations, mainly because 5 GHz was interfering with military signals. Uses dynamic frequency selection and transmit power control. ^17ee82

Dynamic Frequency Selection (DFS): A feature that requires devices to actively monitor the environment for radar signals. ^0f5109

Transmit Power Control (TPC): Allows devices to adjust their transmitting power to the minimum required to maintain a good-quality connection. ^c18249

Band Steering: Optimizes how client devices are distributed across frequency bands. Relevant where two or more bands are in use. Works by detecting clients that can operate on the less congested, faster bands like 5 or 6 GHz and moving them over to those bands. ^8a51bd

802.11: The standard used for wireless networks, with several versions (a, b, g, n, ac, and ax). ^4e0b42

Multiple-Input Multiple-Output (MIMO): Data is split across multiple antennas and multiplexed into a single stream for processing. ^a021f4

Multi-User MIMO (MU-MIMO): Multipath wireless technology that allows multiple users to access the wireless network and access point at the same time. MIMO acts sort of like a hub, while MU-MIMO acts more like a switch and helps avoid collisions. ^44bbb1
