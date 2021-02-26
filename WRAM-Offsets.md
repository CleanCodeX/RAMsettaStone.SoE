# W-RAM Offsets

## W-RAM <-> S-RAM Mappings

(in order of W-RAM offset)

* [Chunk5](Chunks/Chunk05.md): [xA35|2613]  (2 bytes)      => S-RAM: [x8E|142]
* [Chunk6](Chunks/Chunk06.md): [xA3F|2623]  (13 bytes)     => S-RAM: [x90|144]
* [Chunk7](Chunks/Chunk07.md): [xA50|2640]  (4 bytes)      => S-RAM: [x9D|157]
* [Chunk12](Chunks/Chunk12.md): [xA7F|2687]  (2 bytes)     => S-RAM: [xCF|207]
* [Chunk13](Chunks/Chunk13.md): [xA89|2697]  (13 bytes)    => S-RAM: [xD1|209]
* [Chunk14](Chunks/Chunk14.md): [xA9A|2714]  (4 bytes)     => S-RAM: [xDE|222]
* [Chunk16](Chunks/Chunk16.md): [xABA|2746]  (101 bytes)   => S-RAM: [xF0|240]
* [Chunk1](Chunks/Chunk01.md): [x2210|8720]  (72 bytes)    => S-RAM: [x26|038]

* [Chunk18](Chunks/Chunk18.md): [x2258|8792]  (146 bytes)  => S-RAM: [x1F7|503]
* [Chunk19](Chunks/Chunk19.md): [x22FF|8959]  (92 bytes)   => S-RAM: [x289|649]
* [Chunk20](Chunks/Chunk20.md): [x2361|9057]  (44 bytes)   => S-RAM: [x2E5|741]
* [Chunk21](Chunks/Chunk21.md): [x2513|9491]  (32 bytes)   => S-RAM: [x311|785]

* [Chunk17](Chunks/Chunk17.md): [x2F52|12114]  (162 bytes) => S-RAM: [x155|341]

* [Chunk2](Chunks/Chunk02.md): [x4EB3|20147]  (2 bytes)    => S-RAM: [x6E|110]
* [Chunk3](Chunks/Chunk03.md): [x4ECF|20175]  (24 bytes)   => S-RAM: [x70|112]

* [Chunk4](Chunks/Chunk04.md): [x4F23|20259]  (6 bytes)    => S-RAM: [x88|136]
* [Chunk8](Chunks/Chunk08.md): [x4F29|20265]  (14 bytes)   => S-RAM: [xA1|161]
* [Chunk9](Chunks/Chunk09.md): [x4F61|20321]  (2 bytes)    => S-RAM: [xB1|177]
* [Chunk10](Chunks/Chunk10.md): [x4F7D|20349]  (24 bytes)  => S-RAM: [xAF|175]
* [Chunk11](Chunks/Chunk11.md): [x4FD1|20433]  (6 bytes)   => S-RAM: [xC9|201]
* [Chunk15](Chunks/Chunk15.md): [x4FD7|20439]  (14 bytes)  => S-RAM: [xE2|226]

All Offsets belong to 7E address space. Meaning offset 0000 is located at $7E:0001

* [Chunk5](Chunks/Chunk05.md)
WRAM		Length	Description (Boy stats)
> 0A35		0x02	Max HP

* [Chunk6](Chunks/Chunk06.md)
WRAM		Length	Description (Boy stats)
> 0A3F		0x02	Attack
> 0A41		0x02	Defense
> 0A43		0x02	Magic Def
> 0A45		0x02	Evade %
> 0A47		0x02	Hit %
> 0A49		0x03	Experience (3 bytes)

* [Chunk7](Chunks/Chunk07.md)
WRAM		Length	Description (Boy stats)
> 0A50		0x02	Level
> 0A52		0x02	Max Chargeup
The values below are curious. As far as I can tell, after saving your game, these values will always be 0x4F. It seems an oversight of the game programmers, as the game copies these values from $30:4Fxx, which is open bus. The values below will always be 0x4F in a save file, but it seems the programmers meant to copy the values from 4Fxx.

* [Chunk12](Chunks/Chunk12.md)
WRAM		Length	Description (Dog stats)
> 0A7F		0x02	Max HP

* [Chunk13](Chunks/Chunk13.md)
WRAM		Length	Description (Dog stats)
> 0A89		0x02	Attack
> 0A8B		0x02	Defense
> 0A8D		0x02	Magic Def
> 0A8F		0x02	Evade %
> 0A91		0x02	Hit %
> 0A93		0x03	Experience (3 bytes)

* [Chunk14](Chunks/Chunk14.md)
WRAM		Length	Description (Dog stats)
> 0A9A		0x02	Level
> 0A9C		0x02	Max Chargeup
The values below are curious. As far as I can tell, after saving your game, these values will always be 0x4F. It seems an oversight of the game programmers, as the game copies these values from $30:4Fxx, which is open bus. The values below will always be 0x4F in a save file, but it seems the programmers meant to copy the values from 4Fxx.

* [Chunk16](Chunks/Chunk16.md)
WRAM		Length	Description (various things)
> 0ABA		0x02	Current equipped weapon
> 0ABC		0x02	unknown
> 0ABE		0x02	Dog - Pointer to current Collar stats
> 0AC0		0x02	Boy - Pointer to current Armor stats
> 0AC2		0x02	Boy - Pointer to current Helmet stats
> 0AC4		0x02	Boy - Pointer to current Armband stats
> 0AC6		0x03	Money - Talons
> 0AC9		0x03	Money - Jewels
> 0ACC		0x03	Money - Gold Coins
> 0ACF		0x03	Money - Credits
> 0AD2-0B1E	0x4D	Most are listed in Secret_of_Evermore:RAM_map

* [Chunk1](Chunks/Chunk01.md)
WRAM		Length	Location	Description (checksum and strings)
> 2210		0x24	Boy name (zero padded, must end with byte 0x00)
> 2234		0x24	Dog name (zero padded, must end with byte 0x00)

* [Chunk18](Chunks/Chunk18.md)
WRAM		Length	Description (unknowns)
> 2258-22E9	0x92	unknown

* [Chunk19](Chunks/Chunk19.md)
WRAM		Length	Description (Alchemy ingredients and Inventory)
> 22FF-235A	0x5C	Most are listed in Secret_of_Evermore:RAM_map

* [20](Chunks/Chunk20.md)
WRAM		Length	Description (unknowns)
> 2361-238C	0x2C	unknown

* [Chunk21](Chunks/Chunk21.md)
WRAM		Length	Description (Trade good amounts)
> 2513-2532	0x20 	Most are listed in Secret_of_Evermore:RAM_map

* [Chunk17](Chunks/Chunk17.md)
WRAM		Length	Description (Alchemy levels and unknowns)
> 2F52		0x46	Alchemy spell levels (low component)
> 2F98		0x46	Alchemy spell levels (high component)
> 2FDE-2FF3	0x16	unknown

* [Chunk2](Chunks/Chunk02.md)
WRAM		Length	Description (Boy stats)
> 4EB3		0x02	Current HP

* [Chunk3](Chunks/Chunk03.md)
WRAM		Length	Description (Boy stats)
> 4ECF		0x02	Status 1 - Status ID
> 4ED1		0x02	Status 1 - Main Timer
> 4ED3		0x02	Status 1 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 4ED5		0x02	Status 2 - Status ID
> 4ED7		0x02	Status 2 - Main Timer
> 4ED9		0x02	Status 2 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 4EDB		0x02	Status 3 - Status ID
> 4EDD		0x02	Status 3 - Main Timer
> 4EDF		0x02	Status 3 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 4EE1		0x02	Status 4 - Status ID
> 4EE3		0x02	Status 4 - Main Timer
> 4EE5		0x02	Status 4 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval

* [Chunk4](Chunks/Chunk04.md)
WRAM		Length	Description (unknowns)
> 4F23		0x02	unknown
> 4F25		0x02	unknown
> 4F27		0x02	unknown

* [Chunk8](Chunks/Chunk08.md)
WRAM		Length	Open bus	Description (Boy stats)
> 4F29		0x02	$30:4F29	Overall boost to Attack statistic
> 4F2B		0x02	$30:4F2B	Overall boost to Defense statistic
> 4F2D		0x02	$30:4F2D	Overall boost to Evade % statistic
> 4F2F		0x02	$30:4F2F	Overall boost to Hit % statistic
> 4F31		0x02	$30:4F31	Overall boost to Magic Defense statistic
> 4F33		0x02	$30:?		Last damage taken.
> 4F35		0x02	$30:4F35	Regenerate (Horace) or Pixie Dust protection in effect

* [Chunk9](Chunks/Chunk09.md)
WRAM		Length	Description (Dog stats)
> 4F61		0x02		Current HP

* [Chunk10](Chunks/Chunk10.md)
WRAM		Length	Description (Dog stats)
> 4F7D		0x02	Status 1 - Status ID
> 4F7F		0x02	Status 1 - Main Timer
> 4F81		0x02	Status 1 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 4F83		0x02	Status 2 - Status ID
> 4F85		0x02	Status 2 - Main Timer
> 4F87		0x02	Status 2 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 4F89		0x02	Status 3 - Status ID
> 4F8B		0x02	Status 3 - Main Timer
> 4F8D		0x02	Status 3 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval
> 4F8F		0x02	Status 4 - Status ID
> 4F91		0x02	Status 4 - Main Timer
> 4F93		0x02	Status 4 - Boost provided to statistic(s), OR Time since/until last/next damage/healing interval

* [Chunk11](Chunks/Chunk11.md)
WRAM		Length	Description (unknowns)
> 4FD1		0x02	unknown
> 4FD3		0x02	unknown
> 4FD5		0x02	unknown

* [Chunk15](Chunks/Chunk15.md)
WRAM		Length	Description (Boy stats)
> 4FD7		0x02	Overall boost to Attack statistic
> 4FD9		0x02	Overall boost to Defense statistic
> 4FDB		0x02	Overall boost to Evade % statistic
> 4FDD		0x02	Overall boost to Hit % statistic
> 4FDF		0x02	Overall boost to Magic Defense statistic
> 4FE1		0x02	Last damage taken.
> 4FE3		0x02	Regenerate (Horace) or Pixie Dust protection in effect
