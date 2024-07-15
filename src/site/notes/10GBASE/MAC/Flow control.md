---
{"dg-publish":true,"permalink":"/10-gbase/mac/flow-control/"}
---


**Ethernet flow control** is a mechanism for temporarily stopping the transmission of data on [Ethernet](https://en.wikipedia.org/wiki/Ethernet "Ethernet") family [computer networks](https://en.wikipedia.org/wiki/Computer_network "Computer network"). The goal of this mechanism is to avoid [packet loss](https://en.wikipedia.org/wiki/Packet_loss "Packet loss") in the presence of [network congestion](https://en.wikipedia.org/wiki/Network_congestion "Network congestion").

The first flow control mechanism, the [[10GBASE/MAC/Pause frame\|Pause frame]], was defined by the **IEEE 802.3x** standard. The follow-on **priority-based flow control**, as defined in the **IEEE 802.1Qbb** standard, provides a link-level flow control mechanism that can be controlled independently for each [class of service](https://en.wikipedia.org/wiki/Class_of_service "Class of service") (CoS), as defined by [IEEE P802.1p](https://en.wikipedia.org/wiki/IEEE_P802.1p "IEEE P802.1p") and is applicable to [data center bridging](https://en.wikipedia.org/wiki/Data_center_bridging "Data center bridging") (DCB) networks, and to allow for prioritization of voice over IP (VoIP), video over IP, and database synchronization traffic over default data traffic and bulk file transfers.

## Subsequent efforts
[[10GBASE/MAC/PFC\|PFC]]: Priority flow control
[[10GBASE/MAC/LFC\|LFC]]: Link level flow control