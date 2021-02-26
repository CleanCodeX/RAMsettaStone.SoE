# S-RAM Offsets

[Credits](Credits.md)

(in order of offset)

### S-RAM (absolute)
> AudioMode: [0]
> LastSaveSlotId: [1]
> FirstSaveSlot: [2]
> Unknown1: [3_270|xCC6]

### Save slot (relative)
> Checksum: [0]

> [Chunk1](Chunks/Chunk01.md): [x26|38] 

> [Chunk2](Chunks/Chunk02.md): [x6E|110] 
> [Chunk3](Chunks/Chunk03.md): [x70|112] 
> [Chunk4](Chunks/Chunk04.md): [x88|136] 

> [Chunk5](Chunks/Chunk05.md): [x8E|142] 
> [Chunk6](Chunks/Chunk06.md): [x90|144] 
> [Chunk7](Chunks/Chunk07.md): [x9D|157] 

> [Chunk8](Chunks/Chunk08.md): [xA1|161] 
> [Chunk9](Chunks/Chunk09.md): [xAF|175] 
> [Chunk10](Chunks/Chunk10.md): [xB1|177] 

> [Chunk11](Chunks/Chunk11.md): [xC9|201] 
> [Chunk12](Chunks/Chunk12.md): [xCF|207] 
> [Chunk13](Chunks/Chunk13.md): [xD1|209]
> [Chunk14](Chunks/Chunk14.md): [xDE|222] 
> [Chunk15](Chunks/Chunk15.md): [xE4|226]
> [Chunk16](Chunks/Chunk16.md): [xF0|240]

> [Chunk17](Chunks/Chunk17.md): [x155|341] 

> [Chunk18](Chunks/Chunk18.md): [x1F7|503]
> [Chunk19](Chunks/Chunk19.md): [x289|649] 
> [Chunk20](Chunks/Chunk20.md): [x2E5|741] 
> [Chunk21](Chunks/Chunk21.md): [x311|785]

* [Chunk1](Chunks/Chunk01.md)
SRAM	Length	WRAM	Description (checksum and strings)
> 0x26	0x24	0x2210	Boy name (zero padded, must end with byte 0x00)
> 0x4A	0x24	0x2234	Dog name (zero padded, must end with byte 0x00)

* [Chunk2](Chunks/Chunk02.md)
SRAM	Length	WRAM	Description (Boy stats)
> 0x6E	0x02	0x4EB3	Current HP

* [Chunk3](Chunks/Chunk03.md)
SRAM	Length	WRAM	Description (Boy stats)
> 0x70	0x02	0x4ECF	Status 1 - Status ID
> 0x72	0x02	0x4ED1	Status 1 - Main Timer
> 0x74	0x02	0x4ED3	Status 1 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 0x76	0x02	0x4ED5	Status 2 - Status ID
> 0x78	0x02	0x4ED7	Status 2 - Main Timer
> 0x7A	0x02	0x4ED9	Status 2 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 0x7C	0x02	0x4EDB	Status 3 - Status ID
> 0x7E	0x02	0x4EDD	Status 3 - Main Timer
> 0x80	0x02	0x4EDF	Status 3 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 0x82	0x02	0x4EE1	Status 4 - Status ID
> 0x84	0x02	0x4EE3	Status 4 - Main Timer
> 0x86	0x02	0x4EE5	Status 4 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval

* [Chunk4](Chunks/Chunk04.md)
SRAM	Length	WRAM	Description (unknowns)
> 0x88	0x02	0x4F23	unknown
> 0x8A	0x02	0x4F25	unknown
> 0x8C	0x02	0x4F27	unknown

* [Chunk5](Chunks/Chunk05.md)
SRAM	Length	WRAM	Description (Boy stats)
> 0x8E	0x02	0x0A35	Max HP

* [Chunk6](Chunks/Chunk06.md)
SRAM	Length	WRAM	Description (Boy stats)
> 0x90	0x02	0x0A3F	Attack
> 0x92	0x02	0x0A41	Defense
> 0x94	0x02	0x0A43	Magic Def
> 0x96	0x02	0x0A45	Evade %
> 0x98	0x02	0x0A47	Hit %
> 0x9A	0x03	0x0A49	Experience (3 bytes)

* [Chunk7](Chunks/Chunk07.md)
SRAM	Length	WRAM	Description (Boy stats)
> 0x9D	0x02	0x0A50	Level
> 0x9F	0x02	0x0A52	Max Chargeup
The values below are curious. As far as I can tell, after saving your game, these values will always be 0x4F. It seems an oversight of the game programmers, as the game copies these values from $30:4Fxx, which is open bus. The values below will always be 0x4F in a save file, but it seems the programmers meant to copy the values from 0x4Fxx.

* [Chunk8](Chunks/Chunk08.md)
SRAM	Length	WRAM	Description (Boy stats)
> 0xA1	0x02	0x4F29	Overall boost to Attack statistic
> 0xA3	0x02	0x4F2B	Overall boost to Defense statistic
> 0xA5	0x02	0x4F2D	Overall boost to Evade % statistic
> 0xA7	0x02	0x4F2F	Overall boost to Hit % statistic
> 0xA9	0x02	0x4F31	Overall boost to Magic Defense statistic
> 0xAB	0x02	0x4F33	Last damage taken.
> 0xAD	0x02	0x4F35	Regenerate (Horace) or Pixie Dust protection in effect

* [Chunk9](Chunks/Chunk09.md)
SRAM	Length	WRAM	Description (Dog stats)
> 0xAF	0x02	0x4F61	Current HP

* [Chunk10](Chunks/Chunk10.md)
SRAM	Length	WRAM	Description (Dog stats)
> 0xB1	0x02	0x4F7D	Status 1 - Status ID
> 0XB3	0x02	0x4F7F	Status 1 - Main Timer
> 0xB5	0x02	0x4F81	Status 1 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 0xB7	0x02	0x4F83	Status 2 - Status ID
> 0xB9	0x02	0x4F85	Status 2 - Main Timer
> 0xBB	0x02	0x4F87	Status 2 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 0xBD	0x02	0x4F89	Status 3 - Status ID
> 0xBF	0x02	0x4F8B	Status 3 - Main Timer
> 0xC1	0x02	0x4F8D	Status 3 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 0xC3	0x02	0x4F8F	Status 4 - Status ID
> 0xC5	0x02	0x4F91	Status 4 - Main Timer
> 0xC7	0x02	0x4F93	Status 4 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval

* [Chunk11](Chunks/Chunk11.md)
SRAM	Length	WRAM	Description (unknowns)
> 0xC9	0x02	0x4FD1	unknown
> 0xCB	0x02	0x4FD3	unknown
> 0xCD	0x02	0x4FD5	unknown

* [Chunk12](Chunks/Chunk12.md)
SRAM	Length	WRAM	Description (Dog stats)
> 0xCF	0x02	0x0A7F	Max HP

* [Chunk13](Chunks/Chunk13.md)
SRAM	Length	WRAM	Description (Dog stats)
> 0xD1	0x02	0x0A89	Attack
> 0xD3	0x02	0x0A8B	Defense
> 0xD5	0x02	0x0A8D	Magic Def
> 0xD7	0x02	0x0A8F	Evade %
> 0xD9	0x02	0x0A91	Hit %
> 0xDB	0x03	0x0A93	Experience (3 bytes)

* [Chunk14](Chunks/Chunk14.md)
SRAM	Length	WRAM	Description (Dog stats)
> 0xDE	0x02	0x0A9A	Level
> 0xE0	0x02	0x0A9C	Max Chargeup
The values below are curious. As far as I can tell, after saving your game, these values will always be 0x4F. It seems an oversight of the game programmers, as the game copies these values from $30:4Fxx, which is open bus. The values below will always be 0x4F in a save file, but it seems the programmers meant to copy the values from 0x4Fxx.

* [Chunk15](Chunks/Chunk15.md)
SRAM	Length	WRAM	Description (Boy stats)
> 0xE2	0x02	0x4FD7	Overall boost to Attack statistic
> 0xE4	0x02	0x4FD9	Overall boost to Defense statistic
> 0xE6	0x02	0x4FDB	Overall boost to Evade % statistic
> 0xE8	0x02	0x4FDD	Overall boost to Hit % statistic
> 0xEA	0x02	0x4FDF	Overall boost to Magic Defense statistic
> 0xEC	0x02	0x4FE1	Last damage taken.
> 0xEE	0x02	0x4FE3	Regenerate (Horace) or Pixie Dust protection in effect

* [Chunk16](Chunks/Chunk16.md)
SRAM		Length	WRAM		Description (various things)
> 0xF0		0x02	0x0ABA		Current equipped weapon
> 0xF2		0x02	0x0ABC		unknown
> 0xF4		0x02	0x0ABE		Dog - Pointer to current Collar stats
> 0xF6		0x02	0x0AC0		Boy - Pointer to current Armor stats
> 0xF8		0x02	0x0AC2		Boy - Pointer to current Helmet stats
> 0xFA		0x02	0x0AC4		Boy - Pointer to current Armband stats
> 0xFC		0x03	0x0AC6		Money - Talons
> 0xFF		0x03	0x0AC9		Money - Jewels
> 0x102		0x03	0x0ACC		Money - Gold Coins
> 0x105		0x03	0x0ACF		Money - Credits
> 0x108		0x4D	0x0AD2-0B1E	Most are listed in Secret_of_Evermore:RAM_map

* [Chunk17](Chunks/Chunk17.md)
SRAM		Length	WRAM		Description (Alchemy levels and unknowns)
> 0x155		0x46	0x2F52		Alchemy spell levels (low component)
> 0x19B		0x46	0x2F98		Alchemy spell levels (high component)
> 0x1E1-1F6	0x16	0x2FDE-2FF3	unknown

* [Chunk18](Chunks/Chunk18.md)
SRAM		Length	WRAM		Description (unknowns)
> 0x1F7-288	0x92	0x2258-22E9	unknown

* [Chunk19](Chunks/Chunk19.md)
SRAM		Length	WRAM		Description (Alchemy ingredients and Inventory)
> 0x289-2E4	0x5C	0x22FF-235A	Most are listed in Secret_of_Evermore:RAM_map

* [Chunk20](Chunks/Chunk20.md)
SRAM		Length	WRAM		Description (unknowns)
> 0x2E5-310	0x2C	0x2361-238C	unknown

* [Chunk21](Chunks/Chunk21.md)
SRAM		Length	WRAM		Description (Trade good amounts)
> 0x311-330	0x20	0x2513-2532	Most are listed in Secret_of_Evermore:RAM_map

Credits:
Offsets taken from SoE RAMsetta Stone by Phonymike.

