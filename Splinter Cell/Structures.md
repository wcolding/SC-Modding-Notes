### ESam
This structure is the main class for Sam, holding some stats and pointers to other structures

| Offset | Size | Type | ID |
| --- | --- | --- | ------------|
| 0xD4 | 4 | float | X Position |
| 0xD8 | 4 | float | Y Position |
| 0xDC | 4 | float | Z Position (Height) |
| 0xE4 | 2 | ushort | Y Rotation |
| 0x2A8| 4 | ptr | EPlayerController pointer |
| 0x2E4 | 4 | float | JumpZ (Jump force) |
| 0x330 | 4 | int | Current Health (max 200) |


### EPlayerController

| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x2B0 | 4 | float | FOV |
| 0x5BC | 4 | int | m_curWalkSpeed | Value 1-5, modified by mouse wheel |
