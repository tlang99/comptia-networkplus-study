Layer 1 is the bottom of the OSI model. Includes physical and electrical network characteristics. 

Data is transmitted in [[#^f1d365|bits]] at this layer

Cables are also part of the physical layer, such as an Ethernet cable with an RJ-45 connector. These cables come in two primary types
* Straight-through
* Crossover

Layer 1 devices view networks from a physical topology perspective.

Data can be transmitted in two ways at this layer via [[#^f11208|Asynchronous]] or [[#^4d0ab6|Synchronous]] communication. Data is transferred as bits utilizing through a medium, such as ethernet, coax, or fiber optic, by signaling 1s and 0s using a method known as [[#^3eb6c2|Transition Modulation]]

The [[#^f05e22|Bandwidth]] of the medium can be utilized in two different ways: 
* [[#^8ca584|Broadband]]
* [[#^a96d8f|Baseband]]

Baseband allows for multiple devices to communicate at the same time utilizing a technology called [[#^31bf91|Multiplexing]]. Multiplexing comes in three varieties:
* [[#^fd2bac|Time-Division Multiplexing]]
* [[#^44a72b|Statistical Time-Division Multiplexing (StatTDM)]]
* [[#^134185|Frequency-Division Multiplexing (FDM)]]

NOTE: Dion stated that the specifics of TDM, StatTDM, and FDM do not need to be memorized for the exam. Only the fact that Multiplexing involves optimizing a limited amount of resources for more efficient utilization, and that multiplexing allows multiple people to use a baseband connection at the same time

Layer 1 Devices: Fiber optic cable, Ethernet Cable, Coax Cable, Bluetooth, Wi-Fi, Near-field Communication (NFC), Hubs, APs, Media Converters.
* Layer 1 devices are essentially repeaters, passing along whatever is received

### Glossary

Bits: Smallest measurement of data. Binary series of 1s and 0s. ^f1d365

Transition Modulation: If a signal over a medium changes during the clock cycle, then a 1 is represented. Otherwise, a 0 is represented. ^3eb6c2

Asynchronous Communication: Uses start and stop bits to indicate when transmissions occur from the sender to the receiver. ^f11208

Synchronous Communication: Uses a synchronous clock to coordinate the transmissions by both sender and receiver. ^4d0ab6

Broadband: Divides bandwidth into two separate channels ^8ca584

Baseband: Uses all available frequencies on a medium to transmit data. Baseband uses a reference clock and communicates synchronously by utilizing Multiplexing ^a96d8f

Bandwidth: The maximum amount of data that can be transmitted over a medium in a specific amount of time. ^f05e22

Time-Division Multiplexing (TDM): Each sessions takes a turn, using time slots, to share the medium between all users. Clients/nodes can only communicate during their given slot ^fd2bac

Statistical Time-Division Multiplexing (StatTDM): Dynamically allocates time slots on an as-needed basis. It is more efficient than TDS as it allows clients/nodes to communicate whenever needed. ^44a72b

Frequency-Division Multiplexing (FDM): Divides the medium into channels based on frequencies and each session is transmitted over a different channel. ^134185

Multiplexing: Combines multiple signals into a single signal and transmits them over a medium. Allows for multiple devices to use the medium synchronously. ^31bf91