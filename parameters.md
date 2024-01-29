# Modifications des paramètres du jeu Palworld

Dans ce documment je vais vous expliquer les paramètres que vous pouvez modifier pour rendre votre aventure Palworld à votre goûts.

#Slazes

### Tous ces paramètres ce trouve dans le fichier .ini que vous avez depuis la gestion du serveur depuis l'onglet configuration

#### La modification se fait le serveur éteint !

`Difficulty=None` --> Change la difficulté du jeu, 
- None est pour la configuration par défaut 
- 1 est pour avoir un jeu facile, 
- 2 pour une difficulté normal et 
- 3 pour une difficulté difficile.

`DayTimeSpeedRate=1.000000` --> Modifier ce paramètre fera en sorte que les jours passeront plus ou moins vite

`NightTimeSpeedRate=1.000000` --> Modifie la durée de la nuit

`ExpRate=1.000000` --> Modifie l'xp gagnée

`PalCaptureRate=1.000000` --> Modifie la chance de capture des pals

`PalSpawnNumRate=1.000000` --> Modifie la fréquence de spawn des pals

`PalDamageRateAttack=1.000000` --> Modifie les dégats de tous les pals
`PalDamageRateDefense=1.000000` --> Modifie la défence de tous les pals

`PlayerDamageRateAttack=1.000000` --> Modifie les dégats du joueur

`PlayerDamageRateDefense=1.000000` --> Modifie la défence du joueur

`PlayerStomachDecreaceRate=1.000000` --> Modifie la durée nécessaire au joueur pour avoir faim

`PlayerStaminaDecreaceRate=1.000000` --> Modifie la perte d'endurance lors des actions

`PlayerAutoHPRegeneRate=1.000000` --> Modifie la régénération de vie du joueur

`PlayerAutoHpRegeneRateInSleep=1.000000` --> Modifie la régénération de vie du joueur en dormant

`PalStomachDecreaceRate=1.000000` --> Modifie la faim des pals

`PalStaminaDecreaceRate=1.000000` --> Modifie l'endurence des pals

`PalAutoHPRegeneRate=1.000000` --> Modifie la régénération de vie des pals

`PalAutoHpRegeneRateInSleep=1.000000` --> Modifie la régénération de vie des pals 
lorsque qu'ils dorment

`BuildObjectDamageRate=1.000000` -->  Ajuste le taux auquel les objets construits subissent des dégâts.

`BuildObjectDeteriorationDamageRate=1.00000` --> Ajuste le taux auquel les objets construits se détériorent.

`CollectionDropRate=1.000000` --> Ajuste le taux de largage des objets collectés.

`CollectionObjectHpRate=1.000000` --> Ajuste la santé des objets collectés.

`CollectionObjectRespawnSpeedRate=1.000000` -->Ajuste la vitesse de réapparition des objets collectés. 

`EnemyDropItemRate=1.000000` --> Modifie la quantité de drop des ennemis tués
 
`DeathPenalty=2` 
- ALL, vous perdez vos Pal + équipement (par défaut)
- 0 si vous souhaitez ne rien perdre  , mettez ce paramètre sur 0
- 1 si vous souhaitez perdre qu'un partie de l'équipement et garder vos pals
- 2 si vous souhaitez perdre tout l'équipement en gardant vos Pals

`bEnablePlayerToPlayerDamage=False` --> Activer ou désactiver le PvP

`bEnableFriendlyFire=False` --> Activer les tirs aliés

`bEnableInvaderEnemy=True` --> Activer / désactivés les invasions

`bActiveUNKO=False` --> Active ou désactive UNKO (Nocturne Non Identifié Knock-off).

`bEnableAimAssistPad=True` --> Aide à la visée sur manette

`bEnableAimAssistKeyboard=False` --> Aide à la visée clavier souris

`DropItemMaxNum=3000` --> Nombre max d'item pouvant être au sol

`DropItemMaxNum_UNKO=100` --> Définit le nombre maximal d'objets UNKO largués dans le jeu.

`BaseCampMaxNum=128` --> Nombre maximum de base

`BaseCampWorkerMaxNum=15` --> Nombre maximum de pal dans une base (vous ne pouvez pas modifier cette options sur des serveurs dédiés)

`DropItemAliveMaxHours=1.000000` --> Définit le temps maximal pendant lequel les objets restent en vie après avoir été largués.

`bAutoResetGuildNoOnlinePlayers=False` --> Réinitialise automatiquement les guildes sans joueurs en ligne.

`AutoResetGuildTimeNoOnlinePlayers=72.000000` --> Remise à 0 d'une guilde si aucun joueur s'est connecté depuis X temps

`GuildPlayerMaxNum=20` --> Nombre max de joueur dans une guilde

`PalEggDefaultHatchingTime=72.000000` --> Temps d'incubations des oeufs ( à baisser pour diminuer le temps d'incubation) 

`WorkSpeedRate=1.000000` --> Rapidité de travail

`bIsMultiplay=False` --> Active ou désactive le mode multijoueur.

`bIsPvP=False` --> Active ou désactive le mode joueur contre joueur (PvP).

`bCanPickupOtherGuildDeathPenaltyDrop=False` --> Prendre ou non les items d'une personne morte , peu importe la guilde

`bEnableNonLoginPenalty=True` -->  Active ou désactive les pénalités en cas de non-connexion.

`bEnableFastTravel=True` --> Activer les déplacements instantanés

`bIsStartLocationSelectByMap=True` --> Activer le choix de spawn

`bExistPlayerAfterLogout=False` --> Activer / désactiver la persistance d'un joueur lorsqu'il se déconnecte (son corps restera dans le jeux)

`bEnableDefenseOtherGuildPlayer=False` -->  Active ou désactive la défense des joueurs d'autres guildes.

`CoopPlayerMaxNum=4` --> Nombre max de joueur en coop

`ServerPlayerMaxNum=8` --> Configuration du nombre de slots par l'hebergeur

`ServerName=""` --> Nom du serveur

`ServerDescription=""` --> Description du serveur

`AdminPassword=""` --> Mot de passe admin à renseigner pour les commandes admins

`ServerPassword=""` --> Mot de passe du serveur, à renseigné ou non

`PublicPort=20014` --> Port de connexion

`PublicIP=""` --> Modifier l'ip public

`RCONEnabled=True` --> Activation du RCON (permet de voir les joueurs connecter ou de faire des commandes admins à distances)

`RCONPort=30011` --> Port pour le RCON

`Region=""` --> Région du serveur

`bUseAuth=True` --> Active ou désactive l'authentification du serveur.

`BanListURL="https://api.palworldgame.com/api/banlist.txt"` --> Liste des bans du serveur
