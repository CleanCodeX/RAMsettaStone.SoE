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
SRAM	Size	WRAM	Description (checksum and strings)
> x26	x24		x2210	Boy name (zero padded, must end with byte x00)

> x4A	x24		x2234	Dog name (zero padded, must end with byte x00)

* [Chunk2](Chunks/Chunk02.md)
SRAM	Size	WRAM	Description (Boy stats)
> x6E	2		x4EB3	Current HP

* [Chunk3](Chunks/Chunk03.md)
SRAM	Size	WRAM	Description (Boy stats)
> x70	2		x4ECF	Status 1 - Status ID
> x72	2		x4ED1	Status 1 - Main Timer
> x74	2		x4ED3	Status 1 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> x76	2		x4ED5	Status 2 - Status ID
> x78	2		x4ED7	Status 2 - Main Timer
> x7A	2		x4ED9	Status 2 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> x7C	2		x4EDB	Status 3 - Status ID
> x7E	2		x4EDD	Status 3 - Main Timer
> x80	2		x4EDF	Status 3 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> x82	2		x4EE1	Status 4 - Status ID
> x84	2		x4EE3	Status 4 - Main Timer
> x86	2		x4EE5	Status 4 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval

* [Chunk4](Chunks/Chunk04.md)
SRAM	Size	WRAM	Description (unknowns)
> x88	2		x4F23	unknown
> x8A	2		x4F25	unknown
> x8C	2		x4F27	unknown

* [Chunk5](Chunks/Chunk05.md)
SRAM	Size	WRAM	Description (Boy stats)
> x8E	2		x0A35	Max HP

* [Chunk6](Chunks/Chunk06.md)
SRAM	Size	WRAM	Description (Boy stats)
> x90	2		x0A3F	Attack
> x92	2		x0A41	Defense
> x94	2		x0A43	Magic Def
> x96	2		x0A45	Evade %
> x98	2		x0A47	Hit %
> x9A	3		x0A49	Experience (3 bytes)

* [Chunk7](Chunks/Chunk07.md)
SRAM	Size	WRAM	Description (Boy stats)
> x9D	2		x0A50	Level
> x9F	2		x0A52	Max Chargeup
The values below are curious. As far as I can tell, after saving your game, these values will always be x4F. It seems an oversight of the game programmers, as the game copies these values from $30:4Fxx, which is open bus. The values below will always be x4F in a save file, but it seems the programmers meant to copy the values from x4Fxx.

* [Chunk8](Chunks/Chunk08.md)
SRAM	Size	WRAM	Description (Boy stats)
> xA1	2		x4F29	Overall boost to Attack statistic
> xA3	2		x4F2B	Overall boost to Defense statistic
> xA5	2		x4F2D	Overall boost to Evade % statistic
> xA7	2		x4F2F	Overall boost to Hit % statistic
> xA9	2		x4F31	Overall boost to Magic Defense statistic
> xAB	2		x4F33	Last damage taken.
> xAD	2		x4F35	Regenerate (Horace) or Pixie Dust protection in effect

* [Chunk9](Chunks/Chunk09.md)
SRAM	Size	WRAM	Description (Dog stats)
> xAF	2	x4F61	Current HP

* [Chunk10](Chunks/Chunk10.md)
SRAM	Size	WRAM	Description (Dog stats)
> xB1	2		x4F7D	Status 1 - Status ID
> 0XB3	2		x4F7F	Status 1 - Main Timer
> xB5	2		x4F81	Status 1 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> xB7	2		x4F83	Status 2 - Status ID
> xB9	2		x4F85	Status 2 - Main Timer
> xBB	2		x4F87	Status 2 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> xBD	2		x4F89	Status 3 - Status ID
> xBF	2		x4F8B	Status 3 - Main Timer
> xC1	2		x4F8D	Status 3 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> xC3	2		x4F8F	Status 4 - Status ID
> xC5	2		x4F91	Status 4 - Main Timer
> xC7	2		x4F93	Status 4 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval

* [Chunk11](Chunks/Chunk11.md)
SRAM	Size	WRAM	Description (unknowns)
> xC9	2		x4FD1	unknown
> xCB	2		x4FD3	unknown
> xCD	2		x4FD5	unknown

* [Chunk12](Chunks/Chunk12.md)
SRAM	Size	WRAM	Description (Dog stats)
> xCF	2		x0A7F	Max HP

* [Chunk13](Chunks/Chunk13.md)
SRAM	Size	WRAM	Description (Dog stats)
> xD1	2		x0A89	Attack
> xD3	2		x0A8B	Defense
> xD5	2		x0A8D	Magic Def
> xD7	2		x0A8F	Evade %
> xD9	2		x0A91	Hit %
> xDB	3		x0A93	Experience (3 bytes)

* [Chunk14](Chunks/Chunk14.md)
SRAM	Size	WRAM	Description (Dog stats)
> xDE	2		x0A9A	Level
> xE0	2		x0A9C	Max Chargeup
The values below are curious. As far as I can tell, after saving your game, these values will always be x4F. It seems an oversight of the game programmers, as the game copies these values from $30:4Fxx, which is open bus. The values below will always be x4F in a save file, but it seems the programmers meant to copy the values from x4Fxx.

* [Chunk15](Chunks/Chunk15.md)
SRAM	Size	WRAM	Description (Boy stats)
> xE2	2		x4FD7	Overall boost to Attack statistic
> xE4	2		x4FD9	Overall boost to Defense statistic
> xE6	2		x4FDB	Overall boost to Evade % statistic
> xE8	2		x4FDD	Overall boost to Hit % statistic
> xEA	2		x4FDF	Overall boost to Magic Defense statistic
> xEC	2		x4FE1	Last damage taken.
> xEE	2		x4FE3	Regenerate (Horace) or Pixie Dust protection in effect

* [Chunk16](Chunks/Chunk16.md)
SRAM	Size	WRAM		Description (various things)
> xF0	2		x0ABA		Current equipped weapon
> xF2	2		x0ABC		unknown
> xF4	2		x0ABE		Dog - Pointer to current Collar stats
> xF6	2		x0AC0		Boy - Pointer to current Armor stats
> xF8	2		x0AC2		Boy - Pointer to current Helmet stats
> xFA	2		x0AC4		Boy - Pointer to current Armband stats
> xFC	3		x0AC6		Money - Talons
> xFF	3		x0AC9		Money - Jewels
> x102	3		x0ACC		Money - Gold Coins
> x105	3		x0ACF		Money - Credits
> x108	x4D		x0AD2-0B1E	Most are listed in Secret_of_Evermore:RAM_map

* [Chunk17](Chunks/Chunk17.md)
SRAM		Size	WRAM		Description (Alchemy levels and unknowns)
> x155		x46		x2F52		Alchemy spell levels (low component)
> x19B		x46		x2F98		Alchemy spell levels (high component)
> x1E1-1F6	x16		x2FDE-2FF3	unknown

* [Chunk18](Chunks/Chunk18.md)
SRAM		Size	WRAM		Description (unknowns)
> x1F7-288	x92		x2258-22E9	unknown

* [Chunk19](Chunks/Chunk19.md)
SRAM		Size	WRAM		Description (Alchemy ingredients and Inventory)
> x289-2E4	x5C		x22FF-235A	Most are listed in Secret_of_Evermore:RAM_map

* [Chunk20](Chunks/Chunk20.md)
SRAM		Size	WRAM		Description (unknowns)
> x2E5-310	x2C		x2361-238C	unknown

* [Chunk21](Chunks/Chunk21.md)
SRAM		Size	WRAM		Description (Trade good amounts)
> x311-330	x20		x2513-2532	Most are listed in Secret_of_Evermore:RAM_map

