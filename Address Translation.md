### Address Translation

[[#^c859cb|NAT]] and [[#^2a3919|PAT]] were two solutions to the depleting supply of IPv4 addresses before IPv6.

| Type | Translation | How the public IP is assigned |
| --- | --- | --- |
| [[#^6a7ae0\|Static NAT (SNAT)]] | One-to-one | Manually |
| [[#^e40c01\|Dynamic NAT (DNAT)]] | One-to-one | Automatically, from a pool |
| [[#^2a3919\|PAT]] | Many-to-one | One public IP shared by a whole LAN, Ex. a household |

### NAT Address Names

These names must be memorized for the exam:

| | Inside device | Outside device |
| --- | --- | --- |
| Local (private) | [[#^9abe20\|Inside local]] | [[#^300e6e\|Outside local]] |
| Global (public) | [[#^dfb5f5\|Inside global]] | [[#^95edef\|Outside global]] |

NOTE: Any time the word global is used, think public. Local, think private.

### Glossary

Network Address Translation (NAT): Used to conserve the limited supply of IPv4 addresses. Translates a private address into a public one for routing over public networks. Also in [[IPv4 Addressing#^5d6b02|IPv4 Addressing]]. ^c859cb

Dynamic NAT (DNAT): Automatically assigns an IP address from a pool, giving a one-to-one translation. ^e40c01

Static NAT (SNAT): Manually assigns an IP address, giving a one-to-one translation. More secure. ^6a7ae0

Port Address Translation (PAT): Multiple private IP addresses share one public IP address, giving a many-to-one translation. Ex. one public IP for a whole LAN, like a household. ^2a3919

Inside Local: A private IP address referencing an inside device. ^9abe20

Inside Global: A public IP address referencing an inside device. ^dfb5f5

Outside Local: A private IP address referencing an outside device. ^300e6e

Outside Global: A public IP address referencing an outside device. ^95edef
