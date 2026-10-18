### Transmission Control Protocol (TCP)

[[#^3c4d5e|TCP]] operates at the Transport Layer (Layer 4) and is widely used due to its reliability. It breaks larger messages down into smaller packets and uses the [[Layer 4 (Transport Layer)#^9f2b3c|three-way handshake]] to verify receipt: the client sends a SYN packet, the server responds with a SYN-ACK, and the client sends back an ACK.

TCP uses sequence numbers to make sure messages arrive in the correct order. It also uses [[Layer 4 (Transport Layer)#^b14d5e|windowing]] for flow control and performs error checking with checksums.

Ports are important to TCP because they allow multiple network applications to coexist.

### User Datagram Protocol (UDP)

[[#^4d5e6f|UDP]] also operates at the Transport Layer (Layer 4). It works on a connectionless data model: data is sent to recipients without establishing data paths, there is no three-way handshake, and UDP does not keep track of packets at all after sending them.

UDP is known for its low latency and reduced processing overhead, but it lacks the error checking and recovery services of TCP. It is best used where speed is critical and error checking is non-essential, such as media transfer like streaming video.

UDP packets are much simpler and smaller than TCP packets (8-byte headers vs. TCP's 20 to 60 bytes).

### Internet Control Message Protocol (ICMP)

[[#^5e6f70|ICMP]] is a Network Layer (Layer 3) protocol. It is not used for sending data. Instead, it is used to diagnose communication issues and provide hosts with information about network problems, which makes it essential for error reporting and testing. It can report:
* When a service or host is unreachable
* When a packet's time to live has expired
* When a router cannot forward packets because its buffer is full

The `ping` command uses ICMP to send an ICMP echo request message to test whether a host on a network is reachable.

ICMP messages have a simple structure, with a header made up of three things:
* Type:
* Code:
* Checksum:

ICMP lacks the reliability mechanisms of TCP. It prioritizes speed and simplicity over data integrity and security. Attackers have used it for:
* [[#^6f7081|ICMP Flood Attacks]]
* [[#^708192|Ping of Death]]

Because of these vulnerabilities, network administrators sometimes choose to block ICMP traffic.

### Glossary

Transmission Control Protocol (TCP): A fundamental protocol in the Internet protocol suite, made up of a set of rules that govern the exchange of data. Reliable and connection-oriented. ^3c4d5e

User Datagram Protocol (UDP): Communication protocol used across the internet for time-sensitive transmissions, especially in applications where losing some packets is acceptable over delayed receipt. ^4d5e6f

Internet Control Message Protocol (ICMP): Integral part of the Internet Protocol Suite, which is the set of protocols used for internet traffic. A Layer 3 protocol primarily used for diagnosing communication issues and providing hosts with information about network problems. ^5e6f70

ICMP Flood Attack: Overloading a target machine with a large number of ICMP Echo Request packets, leading to a DoS attack. ^6f7081

Ping of Death: Exploits a vulnerability in older systems where the attacker sends malformed or oversized packets via ICMP. When the target tries to load a packet over its maximum allowed size, it can cause a buffer overflow. ^708192

Distributed Denial of Service Attack (DDoS): Attacker uses a network of compromised computers (botnets) to generate a significant amount of traffic and overwhelm a network. ^8192a3
