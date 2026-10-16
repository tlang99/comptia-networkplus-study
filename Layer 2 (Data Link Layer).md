The Data Link Layer is the 2nd level of the OSI model. Its job is to package [[Layer 1 (Physical Layer)#^f1d365|bits]] received from Layer 1 into Frames, and then transmit the frames across the network. Layer 2 operates in the logical topology and dictates when it is a device's turn to transmit on the network.

Layer 2 utilizes [[#^9f3e27|MAC Addresses]] to identify and 

Communication across Layer 2 can be synchronized to three different schemes:
* [[#^2a7d4e|Isochronous]]
* [[#^8c1f03|Synchronous]]
* [[#^e4b962|Asynchronous]]

Layer 2 devices include: [[#^c06a85|NICs]], Bridges, Switches

Switches are able to use logic to learn which physical ports are attached to which MAC addresses.

### Glossary

Isochronous: Network devices use a common reference clock source and create time slots for transmission. ^2a7d4e

Synchronous: Network devices agree on a clocking method to indicate the beginning and end of frames, and can use control characters. ^8c1f03

Asynchronous: Network devices reference internal clocks and use start and stop bits for synchronization. No real control over when a device is allowed to communicate. ^e4b962

Media Access Control (MAC): Physical addressing system for a device which operates on a logical topology. There is a unique, 48-bit MAC Address assigned to every Network Interface Card (NIC) produced. MAC Addresses are always written hexadecimally, Ex. D2:51:F1:3A:34:65. The first 6 digits are the [[#^7b28f1|Organizationally Unique Identifier (OUI)]], which identifies the manufacturer or vendor of the NIC. The remaining 6 digits are the unique value assigned to that specific NIC. ^51d0ac

MAC Address: A unique, 48-bit hexadecimal chain of 12 digits assigned to every [[#^c06a85|Network Interface Card (NIC)]] produced. Used to identify a network card on a local network. ^9f3e27

Network Interface Card (NIC): Hardware component that  ^c06a85

Organizationally Unique Identifier: The first 6 digits of a MAC address, which identify the manufacturer or vendor of a NIC. ^7b28f1

Logical Link Control (LLC): Provides connection services and allows acknowledgement of receipt of messages. It is the most basic form of flow control. It also provides basic error control functions, such as allowing the receiver to inform the sender that a frame wasn't received or was received corrupted. It does this using a [[#^a64c1b|Checksum]]. ^3d95e0

Checksum: Even or odd. If all bits add up to an even number, it is assumed good. If the last bit is odd and all numbers add up to an odd number, this is also good. If not, it will ask for a retransmission of the frame. ^a64c1b
