# Player

## Get player
```
GetLocalViewPlayer() // player youre watching (can be replay)
GetLocalClientPlayer()
```

## Methods
```
GetPlayerName()
GetBossPlayerName()
GetPlayerClass()
GetVelocity()
GetTeam()

GetActiveWeapon()
GetOffhandWeapon(slot)
GetMainWeapons()
GetAntiTitanWeapon()
GetWeaponAmmoStockpile()
GetZoomFrac()

GetMaxHealth()
GetHealthFrac(player)

GetPetTitan()
GetTitanSoul() // if IsTitan() | player.GetPetTitan().GetTitanSoul() if !IsTitan()

AddThreatScopeColorStatusEffect(weaponOwner)
RemoveThreatScopeColorStatusEffect(weaponOwner)

```

## Bools
```
IsValid(player)
IsAlive(player)

IsPlayer()

IsTitan()
IsTitanAvailable(player)

PlayerMelee_IsAttackActive()
IsUsingOffhandWeapon()
```
