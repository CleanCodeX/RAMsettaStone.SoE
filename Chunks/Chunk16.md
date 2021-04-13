# Chunk16 (101 bytes)

###### CurrentMapId
* [EquippedWeapon](../Items/Enums/EquippedWeapon.md) CurrentEquippedWeapon # [S:240|xF0]  [$7E:0ABA]  (2 bytes)

###### Unknown 9
* UInt16 Unknown9 # [S:242|xF2]  [$7E:0ABC]  (2 bytes)

###### ArmorStatsPointers (only WRAM?)
* UInt16 DogCollarStatsPointer # [244|xF4]  [$7E:0ABE]  (2 bytes)
* UInt16 BoyVestsStatsPointer # [246|xF6]  [$7E:0AC0]  (2 bytes)
* UInt16 BoyHatsStatsPointer # [S:248|xF8]  [$7E:0AC2]  (2 bytes)
* UInt16 BoyBraceletStatsPointer # [S:250|xFA]  [$7E:0AC4]  (2 bytes)

###### Moneys
* [Moneys](../Items/Moneys.md) Moneys # [252|xFC]  [$7E:0AC6-0AD1]  (12 bytes)

###### EquippedAlchemies
* byte[9] EquippedAlchemies # [S:264|x108]  [$7E:0AD2-0ADA]  (9 bytes)

###### CurrentMapId
* UInt16 CurrentMapId # [S:273|x111]  [$7E:0ADB]  (1 byte)

###### Weapon Levels
* [WeaponLevels](../Items/WeaponLevels.md) WeaponLevels # [S:275|x113]  [$7E:0ADD-0AF8]  (28 bytes)

###### Unknown 11
* byte[14] Unknown11 # [S:303|x12F]  (14 bytes)

###### The dogs's attack level
* [WeaponLevel](../Items/WeaponLevel.md) DogAttackLevel # [S:317|x13D]  [$7E:0B07]  (2 bytes)

###### Action screen (8 bytes) 
* UInt16 BoyCombativeness # [S:319|x13F]  [$7E:0B09] 0-6 
* UInt16 BoyAIWeaponCharging # [S:321|x142]  [$7E:0B0B] Even numbers 0,2,4,6
* UInt16 DogCombativeness # [S:323|x144]  [$7E:0B0D] 0-6
* UInt16 DogAIWeaponCharging # [S:325|x146]  [$7E:0B0F] Even numbers 0,2,4,6

###### Window Prefs screen (4 bytes)
* UInt16 WindowPrefs_Pattern # [S:327|x148]  [$7E:0B15] 24, 34, ... A4
* UInt16 WindowPrefs_Border # [S:329|x14A]  [$7E:0B17] Even numbers 0-14, inclusive
* UInt32 ScriptedEventTimer # [S:331|x14B]  [$7E:0B19]

###### Control Prefs screen (6 bytes)
* UInt16 ControlsPrefs_Configuration # [S:335|x14F]  [$7E:0B21] 0, 2
* UInt16 ControlPrefs_RunButton # [S:337|x151]  [$7E:0B23]
* UInt16 ControlPrefs_AttackButton # [S:339|x153]  [$7E:0B25]
