#### Je veux importer une sauvegarde depuis un autre serveur dédié ou une co-op.

1. Copiez la sauvegarde de votre ancien serveur dédié vers le nouveau serveur dédié.

2. Dans le fichier `PalServer\Pal\Saved\Config\WindowsorLinuxServer\GameUserSettings.ini` du nouveau serveur, modifiez `DedicatedServerName` pour correspondre au nom du dossier de votre sauvegarde. Par exemple, si le nom du dossier de votre sauvegarde est `2E85FD38BAA792EB1D4C09386F3A3CDA`, le `DedicatedServerName` devient `DedicatedServerName=2E85FD38BAA792EB1D4C09386F3A3CDA`.

  2 bis. **CO-OP :** Supprimer le fichier `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>\WorldOption.sav` pour permettre la modification du fichier `PalWorldSettings.ini`. Les joueurs n'auront plus leur spawn points mais c'est tout.

3. Démarrez le nouveau serveur et demandez à chaque joueur de créer un nouveau personnage. Lorsqu'un joueur crée un nouveau personnage, un nouveau fichier en `.sav` apparaîtra dans `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>\Players`. Le nom de ce nouveau fichier `*.sav` est le GUID du nouveau joueur. Assurez-vous de noter tous les GUID anciens et nouveaux ainsi que leur correspondance avec les joueurs.

4. Arrêtez le serveur, puis copiez l'intégralité de la nouvelle sauvegarde du serveur depuis `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>` (il doit s'agir de la sauvegarde contenant tous les nouveaux personnages !) dans un dossier temporaire sur votre ordinateur.

5. Copier les anciennes sauvegardes dans le dossier `PalServer\Pal\Saved\SaveGames\0\<VOTRE_SAVE_ID>\Players`

6. Faites une sauvegarde de votre sauvegarde ! Ceci executera un script expérimental (https://github.com/xNul/palworld-host-save-fix/blob/main/fix-host-save.py) avec des bugs connus, donc assurez-vous toujours de conserver une copie de sauvegarde.

7. Télécharger `server-to-serv-wrapping.bat` (https://github.com/Salvatore-Als/palworld-faq/releases/download/uesave/server-to-serv-wrapping.bat) dans le dossier où vous avez votre sauvegarde. Vous devez donc avoir :
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

8. Le wrapper télécharge `uesave.exe` et `fix-host-save.py` et vous demandera l'ID de la sauvegarde ainsi que l'ID de l'ancien joueur et celui du nouveau joueur. Attention vous devez avoir installé python.

9. Pour chaque paire correspondante de GUID ancien et GUID nouveau, exécutez le script.

*** Le script est très long, vous saurez que c'est terminé quand vous aurez `Fix has been applied! Have fun!`***
*** Attention, ce tuto ne prend pas en charge l'installation de Python !***

10. Copiez la sauvegarde depuis le dossier temporaire vers le serveur dédié. Déplacez ou renommez la sauvegarde que vous aviez dans le serveur dédié vers un autre emplacement.

11. Redémarrez le serveur et demandez à chaque joueur de rejoindre le serveur avec son personnage corrigé.

12. Si, après 5 minutes de jeu, les Pals d'un joueur ne les attaquent pas ou ne travaillent pas dans leur base, demandez-leur de suivre la solution de contournement [[Pal bug]](https://github.com/xNul/palworld-host-save-fix/blob/main/README.md#pal-bug) pour les corriger.