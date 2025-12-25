# S7 Communication – Header and Parameter Field Meanings

## 1. Protocol ID (0x32)
- Always 0x32 for S7Comm.
- Identifies the packet as a Siemens S7 Protocol Data Unit (PDU).

## 2. ROSCTR (ROS Control)
Defines the type of S7 message:
- 0x01: Job (client → PLC request)
- 0x03: Ack Data (PLC → client response)

## 3. Redundancy ID (00 00)
- Used in redundant PLC systems.
- Normally always 00 00.

## 4. PDU Reference (01 00)
- Transaction or message ID.
- PLC copies it back in responses.
- Allows you to match a response to a request.

## 5. Parameter Length
- Size (in bytes) of the Parameter section.

## 6. Data Length
- Size (in bytes) of the Data section after parameters.

## Parameter Section

## 7. Function Code (FC)
Defines the operation (read/write/function).

## 8. Item Count
How many PLC variables are referenced.

## 9. Items
This block specifies which PLC memory address is being accessed.

# Quick Interpretation of Your Example

## Query
- Protocol ID: 32
- ROSCTR: 01
- Parameter Length: 00 0e
- Data Length: 00 00
- Function Code: 04
- Item Count: 01
- Items: 12 0a ..
| Field            | Value      | Meaning         |
| ---------------- | ---------- | --------------- |
| Protocol ID      | `32`       | S7 PDU          |
| ROSCTR           | `01`       | Job (request)   |
| Parameter Length | `00 0e`    | 14 bytes        |
| Data Length      | `00 00`    | No data         |
| Function Code    | `04`       | Read variable   |
| Item Count       | `01`       | One address     |
| Items            | `12 0a ..` | Address to read |



## Response
- Protocol ID: 32
- ROSCTR: 03
- Parameter Length: 00 02
- Data Length: 00 04
- Error Code: 00 00
- Function Code: 04
- Item Count: 01
- Items: 05 ..

| Field            | Value   | Meaning                  |
| ---------------- | ------- | ------------------------ |
| Protocol ID      | `32`    | S7 PDU                   |
| ROSCTR           | `03`    | Ack Data                 |
| Parameter Length | `00 02` | 2 bytes                  |
| Data Length      | `00 04` | 4 bytes of data returned |
| Error Code       | `00 00` | No error                 |
| Function Code    | `04`    | Read response            |
| Item Count       | `01`    | One item                 |
| Items            | `05 ..` | Result data              |
