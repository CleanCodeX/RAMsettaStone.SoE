# Chunk20 (44 bytes)

###### Unknown 17C
* UInt16 Unknown17C # [741|x2DD]  [$7E:235D]  (2 bytes) 

###### CurrentEquippedWapon  00 - 1A, even numbers, inclusive. See <see cref="Weapons" /> for weapon order.
* [EquippedWeapon](../Items/Enums/EquippedWeapon.md) CurrentEquippedWapon # [743|x2E7]  [$7E:235F]  (2 byte) 

###### Unknown 17D
* UInt16 Unknown17D # [745|x2E9]  (2 bytes)

###### DogAppearance
* [DogAppearance](../Items/Enums/DogAppearance.md) # [747|x2EB]  (2 byte) 

###### Unknown 17E
* byte[16] Unknown17E # [749|x2ED]  (16 bytes)

###### LastLandingLocation
* [LastLandingLocation](../Items/Enums/LandingLocation.md) LastLandingLocation # [747|x2EB]  (1 byte) 

###### PrizeId ~ ID of prize you're currently retrieving)
* UInt16 PrizeId # [781|x30D]  [$7E:2391]   (2 bytes)

###### PrizeQuantity ~ Quantity of prize you're currently retrieving  (seems to be quickly decremented to 1, though)
* UInt16 PrizeQuantity # [783|x30F]  [$7E:2393]  (2 bytes)