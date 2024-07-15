---
{"dg-publish":true,"permalink":"/10-gbase/mac/axi/"}
---


AXI4-Stream is a simplified, lightweight bus protocol designed specifically for high-speed streaming data applications. It supports only unidirectional data flow, without the need for addressing or complex handshaking. An AXI Stream is similar to an AXI write data channel, with some important differences on how the data is arranged:

- no bursts, instead data is packed into packets, frames and data streams
- no limit on the data length which maybe continuous
- data width can be any integer number of bytes

AXI5 Stream protocol introduces wake-up signaling and signal protection using parity.

A single AXI Stream transmitter can drive multiple streams which maybe interleaved but reordering is not permitted.

|Signal|Source|Width|Description|
|---|---|---|---|
|ACLK|Clock|1|ACLK is a global clock signal. All signals are sampled on the rising edge of ACLK.|
|ARESETn|Reset|1|ARESETn is a global reset signal.|
|TVALID|Transmitter|1|TVALID indicates the Transmitter is driving a valid transfer. A transfer takes place when both TVALID and TREADY are asserted.|
|TREADY|Receiver|1|TREADY indicates that a Receiver can accept a transfer.|
|TDATA|Transmitter|TDATA_WIDTH|TDATA is the primary payload used to provide the data that is passing across the interface. TDATA_WIDTH must be an integer number of bytes and is recommended to be 8, 16, 32, 64, 128, 256, 512 or 1024-bits.|
|TSTRB|Transmitter|TDATA_WIDTH/8|TSTRB is the byte qualifier that indicates whether the content of the associated byte of TDATA is processed as a data byte or a position byte.|
|TKEEP|Transmitter|TDATA_WIDTH/8|TKEEP is the byte qualifier that indicates whether content of the associated byte of TDATA is processed as part of the data stream.|
|TLAST|Transmitter|1|TLAST indicates the boundary of a packet.|
|TID|Transmitter|TID_WIDTH|TID is a data stream identifier. TID_WIDTH is recommended to be no more than 8.|
|TDEST|Transmitter|TDEST_WIDTH|TDEST provides routing information for the data stream. TDEST_WIDTH is recommended to be no more than 8.|
|TUSER|Transmitter|TUSER_WIDTH|TUSER is a user-defined sideband information that can be transmitted along the data stream. TUSER_WIDTH is recommended to be an integer multiple of TDATA_WIDTH/8.|
|TWAKEUP|Transmitter|1|TWAKEUP identifies any activity associated with AXI-Stream interface.|

In the AXI specification, five [channels](https://en.wikipedia.org/wiki/Communication_channel "Communication channel") are described:[8](https://en.wikipedia.org/wiki/Advanced_eXtensible_Interface#cite_note-8)

- Read Address channel (AR)
- Read Data channel (R)
- Write Address channel (AW)
- Write Data channel (W)
- Write Response channel (B)

Other than some basic ordering rules,[9](https://en.wikipedia.org/wiki/Advanced_eXtensible_Interface#cite_note-9) each [channel](https://en.wikipedia.org/wiki/Communication_channel "Communication channel") is independent from each other and has its own couple of `xVALID/xREADY` [handshake](https://en.wikipedia.org/wiki/Handshake_(computing) "Handshake (computing)") signals.[10](https://en.wikipedia.org/wiki/Advanced_eXtensible_Interface#cite_note-10)
[[10GBASE/MAC/MASTER-SLAVE INTERFACE\|MASTER-SLAVE INTERFACE]]

