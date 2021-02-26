# S-RAM Save Slot (817 bytes)

###### Checksum
* UInt16 Checksum # [0x0] : (2 bytes)

###### Chunk00
* [LastSavePointName](Items/FixedLengthString.md) # [x02|2] : (36 bytes, null terminated)

###### Chunk01
* [BoyNameDogName](Chunks/Chunk01.md) # [x26|38] : (72 bytes)

###### Chunk02 
* [BoyCurrentHp](Chunks/Chunk02.md) # [x6E|110] : (2 bytes)

###### Chunk03 
* [BoyStatusBuffs](Chunks/Chunk03.md) # [x70|112] : (24 bytes)

###### Chunk04 
* [Chunk04](Chunks/Chunk04.md) # [x88|136] : (6 bytes)

###### Chunk05 
* [BoyMaxHp](Chunks/Chunk05.md) # [x8E|142] : (2 bytes)

###### Chunk06 
* [BoyStats1](Chunks/Chunk06.md) # [x90|144] : (13 bytes)

###### Chunk07 
* [BoyLevel](Chunks/Chunk07.md) # [x9D|157] : (2 bytes)

###### Chunk08 
* [BoyStats2](Chunks/Chunk08.md) # [xA1|161] : (14 bytes)

###### Chunk09 
* [DogCurrentHp](Chunks/Chunk09.md) # [xAF|175] : (2 bytes)

###### Chunk10
* [DogStatusBuffs](Chunks/Chunk10.md) # [xB1|177] : (24 bytes)

###### Chunk11
* [Unknown 7](Chunks/Chunk11.md) # [xC9|201] : (6 bytes)

###### Chunk12 
* [DogMaxHp](Chunks/Chunk12.md) # [xCF|207] : (2 bytes)

###### Chunk13
* [DogStats1](Chunks/Chunk13.md) # [xD1|209] : (13 bytes)

###### Chunk14 
* [DogLevel](Chunks/Chunk14.md) # [xDE|222] : (2 bytes)

###### Chunk15
* [DogStats2](Chunks/Chunk15.md) # [xE4|226] : (14 bytes) 

###### Chunk16 (Equipped Weapon, Moneys, Equipped Alchemies, Weapon Lvls, DogAttack Lvl)
* [EquippedStuff_Moneys_Levels](Chunks/Chunk16.md) # [xF0|240] : (101 bytes)

###### Chunk17 
* [AlchemyLevels](Chunks/Chunk17.md) # [x155|341] : (162 bytes)

###### Chunk18 (Alchemies, Charms, Spots, Weapons)
* [Collectables_Spots](Chunks/Chunk18.md) # [x1F7|503] : (146 bytes)

###### Chunk19 (Ingredients, Items, Armors, Ammo, FlyingMachine)
* [PossessedStuff](Chunks/Chunk19.md) # [x289|649] : (92 bytes)

###### Chunk20
* [LastLanding_CurrentWeapon](Chunks/Chunk20.md) # [x2E5|741] : (44 bytes)

###### Chunk21 
* [TradeGoods](Chunks/Chunk21.md) # [x311|785] : (32 bytes)
