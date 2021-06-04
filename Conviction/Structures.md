### ESam
This structure holds the positional/transform data of Sam/Archer/Kestrel.

| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x28 | 4 | int | Scene Counter |
| 0x40 | 4 | int | BlackBox id? |
| 0x53 | 1 | byte | Flags | 0x02 = Gravity Disabled, 0x04 = Noclip |
| 0x94 | 4 | float | X Position |
| 0x98 | 4 | float | Z Position |
| 0x9C | 4 | float | Y Position | Height |
| 0xA4 | 2 | ushort | Y Rotation |
| 0x1C0 | 4 | float | X Velocity |
| 0x1C4 | 4 | float | Z Velocity |
| 0x1C8 | 4 | float | Y Velocity |
| 0x450 | 4 | float | Unknown float | 1.00 normally, 0 when in GhostState |
| 0x664 | 4 | ptr | Pointer to Current Weapon |

### Current Weapon
| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x828 | 4 | int | m_CartridgeCapacity |
| 0x82C | 4 | int | m_CurrentCartridgeAmmo |

### Engine.PlayerInput

| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x4 | 1 | bool | bInvertMouseUp |
| 0x4C | 8 | double | MouseSensitivity | 0-100 |

### L3D Data
This structure stores applied L3D effects

| Offset | Size | Type | ID |
| --- | --- | --- | ------------|
| 0x44 | 1 | bool | Character Lighting |
| 0xD5 | 1 | bool | Shadows |
| 0xD8 | 1 | bool | Post Effects |
