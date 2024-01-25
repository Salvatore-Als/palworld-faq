# Palworld FAQ
N'hésitez pas à soumettre une Pull Request si vous souhaitez ajouter des informations :)

***Spécialement conçue pour la communauté VeryGames :)***

### J'ai importé ma sauvegarde, mais mon fichier de configuration ne semble pas fonctionner
Il est possible que la configuration ne soit pas prise en compte. Vous devrez **supprimer** ou **renommer** le fichier `Pal/Saved/SaveGames/0/{VOTRE_SAUVEGARDE}/WorldOption.sav`

### Je ne suis pas certain que ma configuration soit correcte
Nous avons mis en place un outil pour vérifier si votre configuration comporte un souci. Il est disponible [ici](https://palworld.kriax.ovh/configuration-validator).

### Je veux importer une sauvegarde depuis un autre serveur dédié ou une co-op.

1. Copiez la sauvegarde de votre ancien serveur dédié vers le nouveau serveur dédié.

2. Dans le fichier `PalServer\Pal\Saved\Config\WindowsorLinuxServer\GameUserSettings.ini` du nouveau serveur, modifiez `DedicatedServerName` pour correspondre au nom du dossier de votre sauvegarde. Par exemple, si le nom du dossier de votre sauvegarde est `2E85FD38BAA792EB1D4C09386F3A3CDA`, le `DedicatedServerName` devient `DedicatedServerName=2E85FD38BAA792EB1D4C09386F3A3CDA`.

  2 bis. **CO-OP :** Supprimer le fichier `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>\WorldOption.sav` pour permettre la modification du fichier `PalWorldSettings.ini`. Les joueurs n'aurons plus leur spawn points mais c'est tout.

3. Démarrez le nouveau serveur et demandez à chaque joueur de créer un nouveau personnage. Lorsqu'un joueur crée un nouveau personnage, un nouveau fichier .sav apparaîtra dans `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>\Players`. Le nom de ce nouveau fichier .sav est le GUID du nouveau joueur. Assurez-vous de noter tous les GUID anciens et nouveaux ainsi que leur correspondance avec les joueurs.

4. Arrêtez le serveur, puis copiez l'intégralité de la nouvelle sauvegarde du serveur depuis `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>` (il doit s'agir de la sauvegarde contenant tous les nouveaux personnages !) dans un dossier temporaire sur votre ordinateur.

5. Copier les anciennes sauvegardes dans le dossier `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>\Players`

6. Faites une sauvegarde de votre sauvegarde ! Ceci executera un script expérimental (https://github.com/xNul/palworld-host-save-fix/blob/main/fix-host-save.py) avec des bugs connus, donc assurez-vous toujours de conserver une copie de sauvegarde.

7. Télécharger `server-to-serv-wrapping.bat` (https://github.com/Salvatore-Als/palworld-faq/releases/download/uesave/server-to-serv-wrapping.bat) dans le dossier ou vous avez votre sauvegarde, vous devez donc avoir
```plaintext
- votre_dossier
-- {VOTRE_SAVE_ID}
--- Level.sav
--- LevelMeta.sav
---- Players
------ {PLAYER_SAV_ID}.sav
------ {PLAYER_SAV_ID}.sav
------ {PLAYER_SAV_ID}.sav
```

8. Le wrapper télécharge `uesave.exe` et `fix-host-save.py` et vous demandera l'id la sauvegarde ainsi que l'id de l'ancien joueur et celui du nouveau joueur. Attention vous devez avoir installer python.

9. Pour chaque paire correspondante de GUID ancien et GUID nouveau, exécutez le script

*** Le script est très long, vous saurez que c'est terminé quand vous aurez Fix has been applied! Have fun!** 
*** Attention, ce tuto ne prend pas en charge l'installation de Python !***

10. Copiez la sauvegarde depuis le dossier temporaire vers le serveur dédié. Déplacez ou renommez la sauvegarde que vous aviez dans le serveur dédié vers un autre emplacement.

11. Redémarrez le serveur et demandez à chaque joueur de rejoindre le serveur avec son personnage corrigé.

12. Si, après 5 minutes de jeu, les Pals d'un joueur ne les attaquent pas ou ne travaillent pas dans leur base, demandez-leur de suivre la solution de contournement [[Pal bug]](https://github.com/xNul/palworld-host-save-fix/blob/main/README.md#pal-bug) pour les corriger.

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
