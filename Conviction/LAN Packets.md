Conviction seems to send LAN packets over UDP on port 9103

Below are different types of packets with examples:

#### Unknown (Possibly sync message?)  
Length of 13  
Example packets:
```
11 11 64 83 0A 01 AF E3 B8 00 00 00 5F   // p1 machine to p2 machine
11 11 4C FC B1 01 AF E3 B8 00 00 00 67   // p2 to p1

11 11 64 FC B1 01 AF E3 B9 00 00 00 81   // p2 to p1
11 11 4C 83 0A 01 AF E3 B9 00 00 00 47   // p1 to p2

11 11 64 83 0A 01 AF E3 B9 00 00 00 60   // p1 to p2
11 11 4C FC B1 01 AF E3 B9 00 00 00 68   // p2 to p1

11 11 64 FC B1 01 AF E3 BC 00 00 00 84   // p2 to p1
11 11 4C 83 0A 01 AF E3 BC 00 00 00 4A   // p1 to p2
```
Structure:
| Offset | Length | Description | Note |
| ---- | ------ | ----------- | ---- |
| 0x0  | 2 | Header? | Always 11 11 |
| 0x02 | 1 | Type? | 64=request, 4C=response?| 
| 0x03 | 2 | Client ID? | |
| 0x05 | 4 | Session length? | Increments over time |
| 0x09 | 4 | Sync value? | Cycles? |
