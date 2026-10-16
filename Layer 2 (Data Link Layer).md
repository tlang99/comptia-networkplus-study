The Data Link Layer is the 2nd level of the OSI model. It's job is to package bits received from Layer 1 into Frames, and then transmit the frames across the network. Layer 2 operates in the logical topology and dictates when it is a devices turn to transmit on the network

Layer 2 utilizes MAC Addresses to identify and 

Communication across Layer 2 can be synchronized to three different schemes:
* Isochronous: Network devices use a common reference clock source and create time slots for transmission.
* Synchronous: Network devices agree on clocking method to indicate beginning and end of frames and can use control characters.
* Asynchronous: Network devices reference internal clocks and use start and stop bits for synchronization. No real control over when a device is allowed to communicate.

Layer 2 devices include: NICs, Bridges, Switches

Switches are able to use logic to learn which physical ports are attached to which MAC addresses.

### Glossary

Frame: 

Media Access Control (MAC): Physical addressing system for a device which operates on a logical topology. There is a unique, 48-bit MAC Address assigned to every Network Interface Card (NIC) produced. MAC Addresses are always written hexadecimally, Ex. D2:51:F1:3A:34:65. The first 6 digits are the Organizationally Unique Identifier (OUI), which identifies the manufacturer or vendor of the NIC. The remaining 6 digits are the unique value assigned to that specific NIC.

MAC Address: A unique, 48-bit hexadecimal chain of 12 digits assigned to every Network Interface Card (NIC) produced.

Network Interface Card (NIC): Hardware component that 

Organizationally Unique Identifier: The first 6 digits of a MAC address that Identifies the manufacturer or vendor of a NIC.

Logical Link Control (LLC): Provides connection services and allows acknowledgement of receipt of messages. It is the most basic form of flow control. It also provides basic error control functions, such as allowing the receiver to inform the sender that a frame wasn't received or was received corrupted. It does this using a Checksum.

Checksum: Even or odd. If even, assumes good. If last bit is odd, and all numbered are added up to an odd number, this is also good. If not, will ask for a retransmission of the frame.