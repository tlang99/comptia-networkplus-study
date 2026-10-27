### Subnetting

[[#^630dfc|Subnetting]] divides a larger network into smaller ones. The formulas:
* Number of subnets: 2^s, where s is the number of bits borrowed from the host portion
* Assignable IP addresses: 2^h − 2, where h is the total number of host bits. The minus two is for the network ID (the first IP) and the broadcast ID (the last IP), since neither can be assigned to a host.
* Block size: 256 − the octet of the subnet mask that isn't 255 or 0. This is the [[#^1fb2cd|magic number]].

[[#^3edb4f|VLSM]] allows subnets of different sizes on the same network.

### Computer Mathematics

Computers work with IP addresses in [[#^6e99b5|base-2 (binary)]]. Ex. counting in binary: 0, 1, 10, 11, 100, 101.

### VLSM Chart

| CIDR | Subnets | IPs |
| --- | --- | --- |
| /24 | 1 | 256 |
| /25 | 2 | 128 |
| /26 | 4 | 64 |
| /27 | 8 | 32 |
| /28 | 16 | 16 |
| /29 | 32 | 8 |
| /30 | 64 | 4 |

Subnets = how many subnets a /24 splits into. IPs = addresses in each subnet, which is also the block size. Usable IPs = IPs − 2 (network ID and broadcast).

### Magic Number Method

A shortcut for finding a host's network address, broadcast address, and usable range without binary. The magic number is the same as the block size.

1. Find the interesting octet: the octet of the subnet mask that isn't 255 or 0.
2. Find the magic number: 256 − the interesting octet.
3. Find the network address: count up by the magic number in that octet, and stop at the last multiple that isn't bigger than the host's number. Every octet after it is 0.
4. Find the broadcast address: the next multiple − 1. Every octet after it is 255.
5. Usable range = network + 1 through broadcast − 1. Usable hosts = magic number − 2 (when the interesting octet is the last one).

Ex. 10.0.5.200 /27
* Mask: 255.255.255.224, so the interesting octet is the 4th
* Magic number: 256 − 224 = 32
* Count by 32: 0, 32, 64, 96, 128, 160, 192, 224. 192 is the last one not bigger than 200
* Network: 10.0.5.192
* Broadcast: 224 − 1 = 10.0.5.223
* Usable range: 10.0.5.193 – 10.0.5.222, 30 hosts

It also works when the interesting octet isn't the last one. Ex. 172.16.37.10 /20
* Mask: 255.255.240.0, so the interesting octet is the 3rd
* Magic number: 256 − 240 = 16
* Count by 16 in the 3rd octet: 0, 16, 32, 48. 32 is the last one not bigger than 37
* Network: 172.16.32.0
* Broadcast: 48 − 1 = 47 in the 3rd octet, 255 after it = 172.16.47.255
* Usable range: 172.16.32.1 – 172.16.47.254

### Glossary

Subnetting: Taking a larger network and subdividing it into smaller portions. ^630dfc

Variable-Length Subnet Mask (VLSM): Allows subnets of various sizes to be used, and requires a protocol that supports it. ^3edb4f

Base-2 (Binary): The number system computers use for IP addresses, made of only 0s and 1s. ^6e99b5

Magic Number: 256 − the interesting octet of the subnet mask. The same as the block size. ^1fb2cd
