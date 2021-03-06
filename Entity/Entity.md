 # Entity
 As far as i know these methods apply for all entities, however if you somewhat know what youre looking for i recommend looking here first:  
- [Player](https://github.com/ScureX/Titanfall2-ModdingDocumentation/blob/main/Entity/Player.md)
- [Titan](https://github.com/ScureX/Titanfall2-ModdingDocumentation/blob/main/Entity/Titan.md)
- [Weapon](https://github.com/ScureX/Titanfall2-ModdingDocumentation/blob/main/Entity/Weapon.md)

## Methods
```
GetActivePilotLoadoutIndex( player )
GetActiveWeaponPrimaryAmmoLoaded()
GetAngles()
GetAttachmentAngles()
GetAttachmentOrigin()
GetBodyGroupModelCount()
GetCinematicEventFlags()
GetCockpit()
GetFirstPersonProxy()
GetForcedDialogueOnly()
GetGen()
GetLastPingTime()
GetLevel()
GetLifeState()
GetModelName()
GetNextTitanRespawnAvailable()
GetNumPingsAvailable()
GetObjectiveEndTime()
GetObjectiveEntity()
GetObjectiveIndex()
GetObserverMode()
GetOffhandWeapons()
GetOrigin()
GetParent()
GetPersistentSpawnLoadoutIndex( player, "pilot" )
GetPetTitan()
GetPilotLoadoutFromPersistentData( player, loadoutIndex )
GetPingGroupAccumulator()
GetPingGroupStartTime()
GetPlayerGameStat()
GetPlayerGameStat() //PGS_ELIMINATED
GetPlayerNameWithClanTag()
GetPlayerNetBool( "shouldShowWeaponFlyout" )
GetPlayerSettings()
GetPlayerSettingsField( "weaponClass" )
GetShieldHealth()
GetShieldHealthFrac( entity )
GetShieldHealthMax()
GetViewForward()
GetViewModelEntity()
GetViewRight()
GetViewUp()
GetViewVector()
GetXP()
```
```
SetActiveWeaponByName()
SetBodygroup()
SetDodgePowerDelayScale()
SetHealth()
SetLastPingTime()
SetMaxHealth()
SetNumPingsAvailable()
SetNumPingsUsed()
SetOrigin()
SetPowerRegenRateScale()
SetShieldHealth()
SetShieldHealthMax()
SetTitanDisembarkEnabled( bool )
```
```
GiveArmor( entity player, int amount )
GiveOffhandWeapon( "mp_weapon_frag_drone", OFFHAND_ORDNANCE )
GivePilotLoadout( player, loadout )
GiveWeapon()
GiveWeaponPowerUp( entity player, string newWeapon )

TakeOffhandWeapon()
TakeWeaponNow()
```
```
CameraPosition()
CockpitStartDisembark()
ContextAction_IsActive()
ContextAction_IsBusy()
EyeAngles()
EyePosition()
FindBodyGroup()
LookupAttachment()
Lunge_ClearTarget()
Minimap_GetZOrder()
```

## Bools
```
HasBadReputation()
HasMic()
InPartyChat()
IsEjecting()
IsHologram()
IsHuman()
IsInScoreboard( player )
IsInThirdPersonReplay()
IsMuted()
IsPartyLeader()
IsPartyMember( player )
IsPhaseShifted()
IsPlayerEliminated( player )
IsPlayerFemale( player )
IsRespawnAvailable( player )
IsScriptMenuOn()
IsTalking()
IsWatchingKillReplay()
IsWatchingReplay()
IsWeaponDisabled()
Lunge_IsActive()
```
