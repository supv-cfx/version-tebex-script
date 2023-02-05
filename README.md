# version-tebex-script (changelog)

## supv_faction-builder v0.1.8
- Correction :
    - Error load faction/client.lua file if you don't create blips for faction player got
    - Error font got a nil value when you open menu after register/edit faction if you setting a menu (only if you use RageUI Libs) for faction you created
    - Is now possible edit garages you created in faction-builder
- Edit :
    - Not overrides Thread if faction loaded is already loaded
    - Rewrite all files config
    - Rewrite System of menu (faction part)
    - Some optimization
    - .sql files (add 2 request)

## supv_healing v1.2
- Add StateBag (LocalPlayer.state.supv_healing) to get status of player if he is in healing or not

## supv_simpleGarage v1.2
- Updated for supv_core (modules marker) (wrong files v1.1 xD)

## supv_healing v1.1
- Correction fxmanifest, missing: `config/client.lua` LocalPlayer.state.supv_healing

## supv_simpleGarage v1.1
- Updated for supv_core (modules marker)

## supv_healing v1.0
- Initial release!

## supv_carkey v1.6
- Add command you can config in config.lua to give car key example : 
- - `/givecarkey id` or `/gck id` *give carkey for vehicle playerId is in*

## supv_faction-builder v0.1.7
- Add Notification (look config's) --not finish... implementation started
- Sync blips for every players when setting `show = 'erveryone'`

## supv_societyGarage v1.7
- Some issues are fixed with preview of vehicle if you use RageUI, some optimization
- Re upload because server-side broken with escrow since v1.6

## supv_faction-builder v0.1.6
- Debug: handcuff system fixed
- Correction native : IsPedDeadOrDying

## supv_faction-builder v0.1.5
- Debug? : Remove some condition from config to load event handcuff system

## supv_faction-builder v0.1.4
- Debug? : Add more print to debug handcuff system (server client / target)

## supv_faction-builder v0.1.3
- Correction : Faction part, handcuff system event + add print to debug it

## supv_faction-builder v0.1.2
- Correction :
- - Builder: 
- - - Blips scale
- - - Option checkbox
- - Faction: 
- - - System handcuff

## supv_faction-builder v0.1.1
- Correction : Some error with encryption escrow to edit menu (rageui) in builder
- Remove : Button to edit marker because this features isn't finish yet