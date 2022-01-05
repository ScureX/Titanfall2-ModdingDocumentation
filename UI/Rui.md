# Rui

## CreateRui
```Squirrel
// To create one, do:
rui = RuiCreate( $"ui/assetname.rpak", topology, drawGroup, sortKey )

// You can then manipulate it using the following:
RuiSetDrawGroup( rui, drawGroup )
RuiSetString( rui, argName, value )
RuiSetBool( rui, argName, value )
RuiSetInt( rui, argName, value )
RuiSetFloat( rui, argName, value )
RuiSetFloat2( rui, argName, value )  // value is a vector; only x and y are used
RuiSetFloat3( rui, argName, value )
RuiSetColorAlpha( rui, argName, color, alpha )  // color is a vector

// To destroy it, just do:
RuiDestroy( rui )
```

## Methods
```Squirrel
RuiSetResolution(rui, GetScreenSize()[0], GetScreenSize()[1] )
RuiSetDrawGroup( rui, drawGroup )

RuiSetString( rui, argName, value )
RuiSetBool( rui, argName, value )
RuiSetInt( rui, argName, value )
RuiSetFloat( rui, argName, value )
RuiSetFloat2( rui, argName, value )  // value is a vector; only x and y are used
RuiSetFloat3( rui, argName, value )
RuiSetColorAlpha( rui, argName, color, alpha )  // color is a vector

RuiDestroyIfAlive( rui )
```

## Assetnames
https://noskill.gitbook.io/titanfall2/game-values/ui-and-hud
```
ui/callsign_bottom_center.rpak
ui/callsign_left.rpak
ui/callsign_right.rpak
ui/callsign_spectator_bottom_right.rpak
ui/hit_indicator.rpak
ui/ready_info.rpak
ui/callsign_basic.rpak
ui/medal_award.rpak
ui/medal_award_crosshair.rpak
ui/killdeath_info.rpak
ui/hit_indicator.rpak
ui/obituary_crawl_earnmeter.rpak
ui/ammo_status_hint.rpak
ui/ability_hud.rpak
ui/inventory_hud.rpak
ui/cockpit_console_text_top_left.rpak
```

## Topologies
```
clGlobal.topoFullScreen
clGlobal.topoCockpitHudPermanent
```
### Create Topology
```
RuiTopology_CreatePlane()
And RuiTopology_CreateSphere()
```

## Drawgroups
```
RUI_DRAW_WORLD
RUI_DRAW_HUD
RUI_DRAW_COCKPIT
RUI_DRAW_NONE
```

## Sortkey
Int to prevent z-fighting. Higher -> in front

## Tracking
```
// VECTOR TYPES
RUI_TRACK_ABSORIGIN_FOLLOW,                   // Create at absorigin, and update to follow the entity
RUI_TRACK_POINT_FOLLOW,                       // Create on attachment point, and update to follow the entity
RUI_TRACK_OVERHEAD_FOLLOW,                    // Create at the top of the entity's bbox
RUI_TRACK_EYEANGLES_FOLLOW,

// FLOAT TYPES
RUI_TRACK_HEALTH,                   // Health as fraction from 0 to 1
RUI_TRACK_FRIENDLINESS,                   // 0 if ent is enemy, 1 if it's friendly
RUI_TRACK_PLAYER_SUIT_POWER,                   // Player's suit power from 0 to 1
RUI_TRACK_PLAYER_GRAPPLE_POWER,                   // Player's grapple power from 0 to 1
RUI_TRACK_PLAYER_SHARED_ENERGY,                   // Players shared energy value
RUI_TRACK_WEAPON_CHARGE_FRACTION,                   // Weapon charge as fraction from 0 to 1
RUI_TRACK_WEAPON_SMART_AMMO_LOCK_FRACTION,                   // Smart ammo weapon lock fraction from 0 to N
RUI_TRACK_WEAPON_READY_TO_FIRE_FRACTION,                   // Weapon cooldown as fraction from 0 to 1
RUI_TRACK_WEAPON_RELOAD_FRACTION,                   // Weapon reloading as fraction from 0 to 1
RUI_TRACK_WEAPON_DRYFIRE_FRACTION,                   //
RUI_TRACK_WEAPON_CLIP_AMMO_FRACTION,                   // Weapon clip ammo as fraction from 0 to 1
RUI_TRACK_WEAPON_REMAINING_AMMO_FRACTION,                   // Weapon remaining ammo as fraction from 0 to 1
RUI_TRACK_WEAPON_CLIP_AMMO_MAX,                   //
RUI_TRACK_WEAPON_STOCKPILE_AMMO_MAX,                   //
RUI_TRACK_WEAPON_LIFETIME_SHOTS,                   //
RUI_TRACK_WEAPON_AMMO_REGEN_RATE,                   //
RUI_TRACK_BOOST_METER_FRACTION,                   // Player boost meter as fraction from 0 to 1
RUI_TRACK_GLIDE_METER_FRACTION,                   // Player glide meter as fraction from 0 to 1
RUI_TRACK_SHIELD_FRACTION,                   // Shield health as fraction from 0 to 1
RUI_TRACK_STATUS_EFFECT_SEVERITY,                   // Status effect severity as fraction from 0 to 1; attachmentIndex used as status effect index
RUI_TRACK_SCRIPT_NETWORK_VAR,                   // Value of a script network variable (use GetNetworkedVariableIndex())
RUI_TRACK_SCRIPT_NETWORK_VAR_GLOBAL,                   // Value of a script network variable without an entity (use GetNetworkedVariableIndex())
RUI_TRACK_SCRIPT_NETWORK_VAR_LOCAL_VIEW_PLAYER,                   // Value of a script network variable on the local view player (changes automatically during kill replay) (use GetNetworkedVariableIndex())
RUI_TRACK_FRIENDLY_TEAM_SCORE,                   //
RUI_TRACK_FRIENDLY_TEAM_ROUND_SCORE,                   // The value of score2 for friendlies
RUI_TRACK_ENEMY_TEAM_SCORE,                   //
RUI_TRACK_ENEMY_TEAM_ROUND_SCORE,                   // The value of score2 for enemies
RUI_TRACK_MINIMAP_SCALE,                   //
RUI_TRACK_SOUND_METER,                   // Sound meter as fraction from 0 to 1.

// INT TYPES
RUI_TRACK_MINIMAP_FLAGS,
RUI_TRACK_MINIMAP_CUSTOM_STATE,
RUI_TRACK_TEAM_RELATION_VIEWPLAYER,                   // ENEMY: -1, NEUTRAL: 0, FRIENDLY: 1
RUI_TRACK_TEAM_RELATION_CLIENTPLAYER,                   // ENEMY: -1, NEUTRAL: 0, FRIENDLY: 1
RUI_TRACK_SCRIPT_NETWORK_VAR_INT,                   // Value of a script network variable (use GetNetworkedVariableIndex())
RUI_TRACK_SCRIPT_NETWORK_VAR_GLOBAL_INT,                   // Value of a script network variable without an entity (use GetNetworkedVariableIndex())
RUI_TRACK_SCRIPT_NETWORK_VAR_LOCAL_VIEW_PLAYER_INT,                   // Value of a script network variable on the local view player (changes automatically during kill replay) (use GetNetworkedVariableIndex())

// GAMETIME TYPES
RUI_TRACK_LAST_FIRED_TIME,
RUI_TRACK_MINIMAP_THREAT_SECTOR,

// IMAGE TYPES
RUI_TRACK_WEAPON_MENU_ICON,
RUI_TRACK_WEAPON_HUD_ICON,
  ```

# CreateCockpitRui
//TODO
