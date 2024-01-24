# Palworld FAQ
N'hésitez pas à soumettre une Pull Request si vous souhaitez ajouter des informations :)

***Spécialement conçue pour la communauté VeryGames :)***

### J'ai importé ma sauvegarde, mais mon fichier de configuration ne semble pas fonctionner
Il est possible que la configuration ne soit pas prise en compte. Vous devrez **supprimer** ou **renommer** le fichier `Pal/Saved/SaveGames/0/{VOTRE_SAUVEGARDE}/WorldOption.sav`

### Je ne suis pas certain que ma configuration soit correcte
Nous avons mis en place un outil pour vérifier si votre configuration comporte un souci. Il est disponible [ici](https://palworld.kriax.ovh/configuration-validator).

### Je veux importer une sauvegarde depuis un autre serveur dédié

Sur l'ancien serveur :

- Récupérez le dossier situé dans `Pal/Saved/SaveGames/0/VOTREIDENTIFIANTDESAVE` ainsi que tout son contenu, puis sauvegardez-le localement.
- Copiez l'identifiant de la sauvegarde comme précédemment (pour cet exemple : **VOTREIDENTIFIANTDESAVE**)

-> Arrêtez le nouveau serveur

Sur le nouveau serveur :

- Collez le dossier précédemment sauvegardé au même emplacement `Pal/Saved/SaveGames/0/VOTREIDENTIFIANTDESAVE`
- Recherchez le fichier `Pal/Saved/Config/LinuxServer/GameUserSettings.ini` et éditez-le
- Remplacez la valeur de DedicatedServerName par l'identifiant de sauvegarde précédemment copié (pour cet exemple : **VOTREIDENTIFIANTDESAVE**)

-> Relancez le nouveau serveur

- Connectez-vous à votre serveur via le jeu. Si le jeu vous invite à créer un nouveau personnage, utilisez le nom que vous aviez sur l'ancienne sauvegarde.
- Si le jeu ne vous invite pas à créer un nouveau personnage, vous devriez vous reconnecter avec votre personnage existant.

### Ma sauvegarde est réinitialisée quand je relance mon serveur

La configuration doit être effectuée lorsque le serveur est éteint. 

Si elle est réalisée avec le serveur allumé, elle sera écrasée lors du redémarrage, en raison de la sauvegarde effectuée lors de la mise hors ligne du serveur.

### Wipe de mon personnage

Ce problème vient du jeu lui-même. Malheureusement, il faut attendre une correction de la part des développeurs.

### Problème de connexion : Écran noir avec du son

Il semble que la sauvegarde de votre joueur soit corrompue (voir "Wipe de mon personnage").

Pour résoudre cela, vous devez supprimer la sauvegarde de votre personnage qui se trouve dans `/Pal/Saved/SaveGames/0/4BD87C2145BCD3916C05D8B0498854D8/Players/`.

### Comment trouver la sauvegarde de mon personnage

Un joueur se voit attribuer un numéro de connexion, le `playeruid`, visible via la commande `/ShowPlayers` :

```plaintext
name, playeruid, steamid
VeryGames, 2890613232, 76561197970000000
```

Ce playeruid correspond à la valeur décimale des 8 premiers chiffres du nom des fichiers de sauvegarde, qui sont en réalité une valeur hexadécimale.

Si vous avez du mal à comprendre, pas de problème. 

En utilisant cet outil [ici](https://palworld.kriax.ovh/id-finder) et en copiant le nom du fichier `.sav`, par exemple `4BD87C2145BCD3916C05D8B0498854D8.sav`, il vous fournira directement le playeruid correspondant.

<img width="350" alt="image" src="https://github.com/Salvatore-Als/palworld-faq/assets/58212852/a81dd3bf-1f86-4757-8f4e-42c044672b06">

Dans cet exemple, le **fichier** est `AC4B41F0000000000000000000000000.sav` et la **playeruid** est `2890613232`, comme indiqué dans le résultat de la commande `/ShowPlayers`.

### Memory Leak

Il y a quelques événements qui se produisent dans le jeu et sont supposés causer des fuites de mémoire.

Actuellement, il existe une façon de lutter contre cela.

Définissez `bEnableInvaderEnemy=False` dans votre fichier `PalWorldSettings.ini` 

Les Événements supposés causer un problème :

- Rejoindre les donjons de manière répétée
- Événements de raid
- Les Pals de groupe travaillant sur la base ont été vus "déplacer" des objets, mais sortent des limites et les laissent tomber de manière répétée. Cela conduit à une grande accumulation de ressources sur le chemin des Pals.
