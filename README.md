# version-tebex-script (changelog)

## supv_faction-builder v0.2.1 (This update need supv_core >= v0.7.4.1)
- __Correction-Blips:__ Modification du scale:ballot_box_with_check
- __Correction-BossAction:__ Correction de la function exporter `supv_esx:SetAdvanced(...)`
- __Correction-Garage:__ Parfois les les points pour rentrer un véhicule ne charger pas (car la place occupée dans le véhicule n'était pas bien retourner)

## supv_esx v0.3 (This update need supv_core >= v0.7.4.1)
- Correction mineur ainsi que le clear des prints

## supv_faction-builder v0.2.0 (This update need supv_core >= v0.7.4)
- __Blips:__  Correction de la preview blip si vous avez pas le minimum de paramètre recommandé pour lancé cette preview
- __Blips:__ Correction de l'affichage dans le RightLabel du `scale` quand vous faites un blip pour qu'il s'actualise au changement du `float`
- __Garage:__ Possibilité de créer plusieurs types de garages différents `(faction, personnel, libre)`
- __Menu faction:__ Possibilité au joueur de quitter sa faction (configurable)
- __Boss Actions:__ Possibilité d'ajouter une zone pour que les boss gèrent les membres (en ligne / hors ligne [configurable])
- __Coffre:__ Possibilité d'ajouter plusieurs zones de coffre pour une faction
- __Général:__ Liaison des fonctionnalités doublejob via **supv_esx**
- __Options:__ Personnalisation des markers (simple)

__**Nouvelle installation SQL**__
```sql
ALTER TABLE `supv_faction_builder`
ADD `bossAction` longtext DEFAULT '[]';
```
__**Information types de garage :**__
- __1__ : Véhicule qui appartient a la faction (table sql doit correspondre: owned_vehicles `faction`)
- __2__ : Véhicule qui appartient a la faction et au joueur (table sql doit correspondre: owned_vehicles `faction` ET `owner`)
- __3__ : Véhicule qui appartient a la faction ou au joueur (table sql doit correspondre: owned_vehicles `faction` OU `owner`)
- __4__ : Tout les véhicules possibles (Si le véhicule est dans la table sql `owned_vehicles` alors il sera stocker avec la data actualiser en db, si c'est une véhicule voler il sera enregistrer dans le fichier `garage.json`

## supv_esx v0.2 (This update need supv_core >= v0.7.4)
- Retravaille complet sur l'ensemble des exports
- Ajout de 2 exports pour reset la faction & job par défaut
- Changement de l'export `GetMembers` sur le mod: offline, avant tout était retourner dans 1 table avec un paramètre in game ou non sur les joueurs retournées, maintenant vous avez 2 tables retourner (online, offline)
- Ajout d'un exports pour retourner la configuration du fichier qui du coups pour s'adapter a l'ensemble de mes script (exemple si le faction-builder vous avez un es_extended sous job2 et non faction, tout les fonctions seront basé a comment vous aurez configurez le script supv_esx donc le faction-builder pourra fonctionnée sous job2 aussi
- Ajout d'option optionnel de filtrage sur l'export `GetMembers`

## supv_faction-builder v0.1.9
- Reupload : Because 1 error by escrow
- Correction : Index font menu editor (RageUI Libs) default
- Remove : fx_oal in fxmanifest

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