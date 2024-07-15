---
{"dg-publish":true,"permalink":"/10-gbase/mac/lfc/"}
---

Link level flow control (LFC) is a way to alleviate system congestion by pausing data transmission.

When a receiving device is congested, it communicates with the transmitting device by sending a PAUSE frame that instructs the device to stop data transmission for a specific time. This feature is available for each port in all front ports and applies to all traffic on the link. Extreme supports the generation (Tx) and reception (Rx) of PAUSE frames for each physical interface or port channel.