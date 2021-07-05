### ESam
This structure is the main class for Sam, holding some stats and pointers to other structures

| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| - |
| 0xD4 | 4 | float | X Position |
| 0xD8 | 4 | float | Y Position |
| 0xDC | 4 | float | Z Position | Height |
| 0xE4 | 2 | ushort | Z Rotation |
| 0x140 | 4 | ptr | Mesh pointer| Rigged mesh (samAMesh et al) |
| 0x150 | 4 | float | DrawScale | Modified by 'ChangeSize' command |
| 0x178 | 1 | byte | AmbientGlow | Self-illumination |
| 0x2A8| 4 | ptr | EPlayerController pointer |
| 0x2E4 | 4 | float | JumpZ | Jump Force |
| 0x330 | 4 | int | Current Health | Max 200 |


### EPlayerController

| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x2B0 | 4 | float | FOV |
| 0x5BC | 4 | int | m_curWalkSpeed | Value 1-5, modified by mouse wheel |
