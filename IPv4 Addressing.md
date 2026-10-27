### IPv4 Address Structure

IPv4 addresses are written in [[#^2a8420|dotted-decimal notation]], Ex. 192.168.1.4:
* 4 octets, each representing an 8-bit binary number, for 32 bits total
* Split into a network portion and a host portion by a [[#^ef2332|subnet mask]]
* Usually written with [[#^9fdbb8|CIDR notation]], Ex. 192.168.1.4/24

### Address Classes

IP addresses are broken into classes:

| Class | 1st octet value | Default subnet mask | Possible hosts |
| --- | --- | --- | --- |
| A | 1–127 | 255.0.0.0 | 16.7 million |
| B | 128–191 | 255.255.0.0 | 65,536 |
| C | 192–223 | 255.255.255.0 | 256 |
| D | 224–239 | n/a | n/a, special class for [[#^4bb7b7\|multicast]] |
| E | 240–255 | n/a | n/a, experimental. Should not be used in production. |

A [[#^7c04fb|classful mask]] is a class's default mask. A [[#^66276c|classless mask]] borrows host bits, which is what CIDR does.

### Public and Private Addresses

IPv4 addresses are either:
* [[#^52acdc|Public (routable)]]: unique on the internet, leased or purchased from your ISP
* [[#^03b4e6|Private (non-routable)]]: used inside a LAN, not accessible over the internet

[[#^5d6b02|NAT]] lets devices with private addresses reach the internet.

| Class | Private IP range |
| --- | --- |
| A | 10.0.0.0 – 10.255.255.255 |
| B | 172.16.0.0 – 172.31.255.255 |
| C | 192.168.0.0 – 192.168.255.255 |

The private ranges are defined in an [[#^0c61ea|RFC]] (RFC 1918).

Two other special addresses:
* [[#^decbd5|Loopback (localhost)]]: 127.0.0.1
* [[#^f5ceb6|APIPA]]: 169.254.0.0 – 169.254.255.255

Public addresses are managed globally by [[#^1f4b67|ICANN]], which divides management into 5 [[#^3286ba|regional internet registries (RIRs)]]:
* ARIN: North America
* LACNIC: Latin America
* AFRINIC: Africa
* APNIC: Asia Pacific
* RIPE: Europe

### Assigning IPv4 Addresses

Addresses are assigned either manually (static) or dynamically (automatic). Dynamic assignment uses one of four methods:
* [[#^0fa865|BOOTP]]
* [[#^069c30|DHCP]]
* [[#^f5ceb6|APIPA]]
* [[#^5ddef9|ZeroConf]]

### Glossary

Dotted-Decimal Notation: How IPv4 addresses are written, Ex. 192.168.1.4. Each of the 4 octets represents an 8-bit binary number, making the entire address 32 bits. ^2a8420

Subnet Mask: Determines which portion of an IP address is the network portion and which is the host portion. ^ef2332

CIDR Notation: Classless Inter-Domain Routing notation, Ex. 192.168.1.4/24. The number after the slash represents the subnet mask: the number of 1s in the mask. ^9fdbb8

Classful Mask: The default subnet mask for a given class of IP addresses. ^7c04fb

Classless Mask: Borrows some of the host bits from an IPv4 address, which is known as Classless Inter-Domain Routing (CIDR). ^66276c

Multicast Address: An identifier for a group of hosts in a computer network. ^4bb7b7

Public (Routable) Address: A unique IP address assigned to each device on the internet that allows it to communicate with other devices using IPv4. Must be leased or purchased from your ISP. ^52acdc

Private (Non-routable) Address: Used in a LAN to allow communication between devices in that network without a public IP address. Not accessible over the internet. Private addresses fall in the ranges 10.x.x.x, 172.16.x.x – 172.31.x.x, or 192.168.x.x. ^03b4e6

Network Address Translation (NAT): A method that allows a device, usually a router, to act as an agent between the internet and a local, private network. ^5d6b02

Request for Comments (RFC): A formal publication from the Internet Society and the Internet Engineering Task Force (IETF). ^0c61ea

Internet Corporation for Assigned Names and Numbers (ICANN): Manages all IPv4 addresses globally. ^1f4b67

Regional Internet Registry (RIR): One of the 5 regional organizations ICANN divides IPv4 address management into: ARIN, LACNIC, AFRINIC, APNIC, and RIPE. ^3286ba

Loopback Address (Localhost): Always 127.0.0.1. Creates a loopback to the host, and is often used for troubleshooting and testing the network protocol on a system. ^decbd5

Automatic Private IP Address (APIPA): An address the OS assigns itself when the network's DHCP server is unavailable and no IP address has been statically assigned. Range is 169.254.0.0 – 169.254.255.255. ^f5ceb6

BOOTP: Automatically assigns IP addresses and allows a workstation to load a copy of its boot image over the network. ^0fa865

DHCP: Assigns an IP address from an assignable scope, or pool, of addresses, and can configure numerous other options. The modern version of BOOTP. ^069c30

ZeroConf: A newer technology based on APIPA that provides many of the same features, plus some new ones. ^5ddef9
