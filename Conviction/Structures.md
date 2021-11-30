### ESam
This structure holds the positional/transform data of Sam/Archer/Kestrel.

| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x28 | 4 | int | Scene Counter |
| 0x40 | 4 | int | BlackBox id? |
| 0x53 | 1 | byte | Flags | 0x02 = Gravity Disabled, 0x04 = Noclip |
| 0x94 | 4 | float | X Position |
| 0x98 | 4 | float | Y Position |
| 0x9C | 4 | float | Z Position | Height |
| 0xA4 | 2 | ushort | Z Rotation |
| 0x1C0 | 4 | float | X Velocity |
| 0x1C4 | 4 | float | Y Velocity |
| 0x1C8 | 4 | float | Z Velocity |
| 0x450 | 4 | float | Unknown float | 1.00 normally, 0 when in GhostState |
| 0x664 | 4 | ptr | Pointer to Current Weapon |
| 0x11F4 | 4 | ptr | Pointer to Inventory |

### Inventory
| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x44 | 1 | byte | Equipped Gadget | See Gadget enum below; cannot equip something not in loadout |
| 0x46 | 1 | byte | Weapon to fire | What fires when you shoot, even if guns are put away |
| 0x48 | 4 | ptr | Secondary Weapon | Non-pistol weapon |
| 0x4C | 4 | ptr | Primary Weapon | Pistol weapon |
| 0x50 | 1 | byte | Equipped Weapon Index | 0 = None, 1 = Secondary, 2 = Primary |

### Weapon
| Offset | Size | Type | ID | Note |
| --- | --- | --- | ------------| --- |
| 0x800 | 4 | int | m_PrecisionRange |
| 0x804 | 4 | int | m_ShootingRange |
| 0x808 | 4 | int | m_MaxFalloffRange |
| 0x80C | 4 | float | m_MaxFalloffMultiplier |
| 0x828 | 4 | int | m_CartridgeCapacity |
| 0x82C | 4 | int | m_CurrentCartridgeAmmo |
| 0x830 | 4 | int | m_CurrentSpareAmmo |
| 0x83C | 4 | int | Animation set to use? | 0 = Hand-to-Hand, 1 = Pistol, 2 = Two-handed |
| 0x840 | 4 | float | m_RateOfFire |
| 0xD18 | 4 | int | m_iMarkAndExecCapacity |
| 0xD1C | 4 | int | m_iMaxShotPerExecution |
| 0xD20 | 4 | int | m_iRetributionMarkAndExecCapacity |
| 0xDC0 | 4 | float | m_fWallHitInitSizeMultMin |
| 0xDC4 | 4 | float | m_fWallHitInitSizeMultMax |

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

### Gadget Enum
| Gadget | Value |
| --- | --- |
| Frag Grenade | 2 |
| Remote Mine | 4 |
|	EMP Grenade | 7 |
|	Flashbang | 8 |
|	Proximity Mine | 9 |
|	Portable EMP | 13 |
|	Sticky Camera | 15 |
