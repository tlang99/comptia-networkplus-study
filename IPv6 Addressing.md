### IPv6 Addressing

IPv6 was created because of [[#^a6b8f0|address exhaustion]]: running out of IPv4 addresses.
* IPv4: 32 bits, written in decimal
* [[#^2a1d26|IPv6]]: 128 bits, written in hexadecimal, NOT decimal

An IPv6 address is 8 groups of 4 hexadecimal digits (32 hex digits total), separated by colons. Each group is 16 bits. Ex. 2001:0db8:0000:0000:0000:ff00:0042:8329

Addresses can be shortened two ways:
* Shorthand: a group of four 0s (0000) can be written as a single 0, and leading 0s in any group can be dropped
* Zero compression: multiple groups that are all 0s in a row can be replaced with a double colon (::). This can only be used once per address.

Ex. 2001:0db8:0000:0000:0000:ff00:0042:8329 → 2001:db8::ff00:42:8329

A single interface can be assigned multiple IPv6 addresses.

### Address Types

There are three IPv6 address types:

| Type | Starts with | Identifies |
| --- | --- | --- |
| [[#^e15a99\|Unicast]]: [[#^4261be\|globally routed]] | 2000 – 3FFF | A single interface, routable on the internet |
| [[#^e15a99\|Unicast]]: [[#^73888d\|link-local]] | FE80 | A single interface, only usable on the LAN, like a private IPv4 address |
| [[#^060c20\|Multicast]] | FF | A group of interfaces |
| [[#^01c708\|Anycast]] | No way to tell from unicast by looking at it | A set of interfaces, where a packet goes to any one member |

### Address Assignment

* [[#^c8777d|SLAAC]]: hosts configure their own addresses, using [[#^9916fb|EUI-64]]
* [[#^240347|DHCPv6]]: allows DHCP with IPv6, but it's not really needed because of EUI-64
* [[#^7dc1b2|NDP]]: determines the Layer 2 (MAC) addresses on a network

NOTE: Dion says you don't need to know NDP in depth, but know that it's used in IPv6 and borrows functions from Layers 2 and 3 for router advertisement and neighbor discovery. He says to remember:
* IPv6 is 128 bits, compared to IPv4's 32 bits
* Shorthand notation and zero compression
* IPv6 is written in hexadecimal, NOT decimal
* The three IPv6 address types: unicast, multicast, and anycast

### IPv4 and IPv6 Compatibility

IPv6 is backward compatible with IPv4, so both can coexist during the slow transition. These technologies make it possible:
* [[#^682bf8|Dual stack]]: runs both on the same network, preferring IPv6
* [[#^575c7c|Tunneling]]: carries IPv6 packets inside IPv4 packets
* [[#^8835b9|NAT64]]: translates between IPv6-only devices and IPv4 devices, through a [[#^947084|NAT64 gateway]]

### Glossary

Address Exhaustion: Running out of network addresses in IPv4. ^a6b8f0

IPv6: A 128-bit addressing scheme written in hexadecimal, created to solve IPv4 address exhaustion. Uses 8 groups of 4 hex digits separated by colons. ^2a1d26

Unicast Address: An IPv6 address that identifies a single interface. Either globally routed or link-local. ^e15a99

Globally Routed Address: A unicast address that is routable on the internet. Always begins with 2000 through 3FFF. ^4261be

Link-local Address: A unicast address used like a private IPv4 address. Only usable on the LAN, and always begins with FE80. ^73888d

IPv6 Multicast Address: Identifies a group of interfaces. Always begins with FF. ^060c20

Anycast Address: Identifies a set of interfaces, so a packet can be sent to any member of the set. There's no way to tell it apart from a unicast address by looking at it. ^01c708

Stateless Address Auto-configuration (SLAAC): Eliminates the need to obtain addresses or other configuration information from a central server. Uses EUI-64 to accomplish this. ^c8777d

Extended Unique Identifier (EUI-64): Allows a host to assign itself a unique 64-bit IPv6 interface identifier, obtained from its MAC address. Takes the first 6 hex digits of the MAC (the OUI), inserts FF:FE, then places the remaining 6 digits after it. ^9916fb

DHCPv6: Allows DHCP to be used with IPv6, though it isn't really needed because of EUI-64. ^240347

Neighbor Discovery Protocol (NDP): Used in IPv6 to determine the Layer 2 (MAC) addresses on a given network. Borrows functions from Layers 2 and 3 for router advertisement and neighbor discovery. ^7dc1b2

Dual Stack: A network architecture that allows IPv4 and IPv6 to coexist and run simultaneously on the same network infrastructure. Routers, switches, and hosts are configured to understand both types of addresses. Prefers IPv6 by default, but falls back to IPv4 if necessary. ^682bf8

Tunneling: Enables one network protocol to communicate within another by encapsulating packets of a different protocol. Here, IPv6 packets are encapsulated in IPv4 packets. ^575c7c

NAT64: A network address translation mechanism that lets IPv6-only devices communicate with IPv4 servers and devices, converting IPv6 to IPv4 and vice versa as needed. ^8835b9

NAT64 Gateway: When an IPv6-only device sends traffic to an IPv4 address, the traffic is directed to this gateway, which converts it to IPv4, or vice versa. It keeps a table to track the translation mappings. ^947084
