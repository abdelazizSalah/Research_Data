S7 Communication – Header and Parameter Field Meanings
1. Protocol ID (0x32)

Always 0x32 for S7Comm.

Identifies the packet as a Siemens S7 Protocol Data Unit (PDU).

2. ROSCTR (ROS Control)

Defines the type of S7 message:

Value	Meaning
0x01	Job (client → PLC request)
0x03	Ack Data (PLC → client response)