### Wireless Authentication

Wireless networks authenticate users in one of two ways:
* [[#^a77a34|Pre-shared key (PSK)]]
* [[#^aee373|802.1X]]

PSK has a few issues:
* Scalability is difficult, since every user needs to know the key
* No individual user accountability
* Not practical for large office use

802.1X fixes these:
* Relies on an authentication server
* Users authenticate individually
* Better scalability and individual user tracking

These match the two modes WPA2 and WPA3 can run in: [[#^a09ec4|personal mode]] (PSK) and [[#^679601|enterprise mode]] (802.1X).

### Wireless Security Protocols

The wireless security and encryption options are:
* [[#^722402|Wired Equivalent Privacy (WEP)]]
* [[#^ff3834|Wi-Fi Protected Access (WPA)]]
* [[#^b96ba7|Wi-Fi Protected Access 2 (WPA2)]]
* [[#^db86d7|Wi-Fi Protected Access 3 (WPA3)]]
* [[#^16e9b8|Wi-Fi Protected Setup (WPS)]], which is not actually an encryption or security protocol

| Protocol | Encryption | Remember it by | Status |
| --- | --- | --- | --- |
| WEP | RC4 | Initialization vectors (IV), which make it weak | Insecure, never use |
| WPA | RC4 with [[#^e74f52\|TKIP]] and [[#^de85b7\|MIC]] | TKIP and RC4 | Vulnerable |
| WPA2 | [[#^9915e8\|AES]] with [[#^aa53ea\|CCMP]] | CCMP and AES | Still heavily used |
| WPA3 | Stronger, with larger 192-bit and 256-bit keys | [[#^097b93\|SAE]] | Newest (2018) |
| WPS | None | Push button configuration | Disable it |

NOTE: Dion's other key points for the exam:
* Any time you see the word [[#^43f9de|open]] in reference to wireless networks, it means no security, no encryption, and no password.
* Pre-shared keys are associated with a password used in a wireless network's personal mode.
* Enterprise mode is associated with an individual username and password for each user.

### Recommended Settings

NOTE: Dion says that for the exam, a secure wireless network should:
* Disable SSID broadcast
* Enable wireless isolation
* Enable MAC filtering
* Disable WPS

### Captive Portals

A [[#^6f01cc|captive portal]] is commonly used for guest and public Wi-Fi. It's used for:
* User authentication
* Policy acceptance
* Data collection

### Glossary

Pre-shared Key (PSK): An authentication method where the same password or key is used on both the WAP and every connecting client device to gain access to the network. ^a77a34

802.1X: The most widely used enterprise-grade authentication method. Relies on an authentication server, and users authenticate individually. More detail in [[OBJ. 4.3#^52fd64|NAC]]. ^aee373

Personal Mode: A wireless security mode that authenticates with a pre-shared key. ^a09ec4

Enterprise Mode: A wireless security mode that authenticates with centralized authentication, using an individual username and password for each user. ^679601

Open Network: A wireless network with no security, no encryption, and no password. ^43f9de

Wired Equivalent Privacy (WEP): The original 802.11 wireless security standard. An insecure protocol that relies on RC4 for encryption. Associated with initialization vectors (IV), which are what make it weak and vulnerable. Should never be used. ^722402

Wi-Fi Protected Access (WPA): The replacement for WEP. Uses the Temporal Key Integrity Protocol (TKIP), still relies on RC4 for encryption, and adds a Message Integrity Check (MIC). Provided individual logins. Vulnerable. ^ff3834

Temporal Key Integrity Protocol (TKIP): The protocol used by WPA, associated with RC4 encryption. ^e74f52

Message Integrity Check (MIC): Used by WPA to hash data before it's sent over the network. ^de85b7

Wi-Fi Protected Access 2 (WPA2): Created as part of the IEEE 802.11i standard. Used with wireless a, g, n, and ac. Still heavily used today. Uses CCMP instead of MIC, and AES instead of RC4 for encryption, which is more secure. Can authenticate in personal mode (with a pre-shared key) or enterprise mode (with centralized authentication). ^b96ba7

Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP): Used by WPA2 in place of MIC. ^aa53ea

Advanced Encryption Standard (AES): The encryption used by WPA2 in place of RC4. More secure. ^9915e8

Wi-Fi Protected Access 3 (WPA3): Introduced in 2018 as an improvement over WPA2. Uses features like SAE and increased encryption strength, allowing larger 192-bit and 256-bit keys. ^db86d7

Simultaneous Authentication of Equals (SAE): A protocol designed to enhance the handshake process used in Wi-Fi authentication. Used by WPA3 to replace the pre-shared key method. More secure. ^097b93

Wi-Fi Protected Setup (WPS): Not an encryption or security protocol, but a network security standard meant to simplify setting up a secure Wi-Fi connection, so non-technical users can set up secure networks more easily. Associated with push button configuration. Vulnerable to brute-force attacks, so WPS should be disabled. ^16e9b8

Captive Portal: A common feature in modern Wi-Fi networks, especially guest and public networks. Intercepts the user's network connection and redirects them to a web page to authenticate or agree to terms of service. ^6f01cc
