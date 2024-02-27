
### Fix mise à jour v0.1.5.0

#### Création d'une nouvelle installation

- Dans le panel, dan l'onglet `Jeux` créez une nouvelle installation de Palworld. (Vos données actuelles seronts conservées)
- Modifiez l'installation active pour la nouvelle installation et redémarrez une première fois le serveur.

#### Récupération de la sauvegarde de l'ancienne installation

- Éteignez le serveur. 

- Dans l'accès FTP, copiez le _contenu_ du dossier de sauvegarde de l'ancienne installation et collez le dans de dossier de de sauvegarde de la nouvelle installation.
**Ne copiez PAS le dossier en lui-même.**

Si le dossier de l'ancienne sauvegarde est `42679FFB7E0B4775A46948D3E6238455`
Et que le dossier de la nouvelle installation est `A308DA0E450C4734BF7224FAA288A9E3`

Vous devez copiers les fichiers 
 - `42679FFB7E0B4775A46948D3E6238455/Players`
 - `42679FFB7E0B4775A46948D3E6238455/Level.sav`
 - `42679FFB7E0B4775A46948D3E6238455/LevelMeta.save`
dans le dossier `SaveGames/0/A308DA0E450C4734BF7224FAA288A9E3`

Lorsque la copie est terminée vous pouvez relancer le serveur.

#### Configuration

Reconfigurer votre nouvelle installation, une simple copie du fichier de config de l'ancienne installation est suffisante.

#### Récupération de la progression (doit être fait par chaque joueur)

Les données de progression (tutoriel, découverte de la carte) sont enregistrées coté client (sur l'ordinateur des joueurs). 
Chaque joueur devra faire la manipulation suivante s'il souhaite conserver sa progression.

- Connectez-vous une première fois au serveur pour que le jeu crée le dossier avec la progression sur la nouvelle installation de jeu du serveur. Puis fermez le jeu.

- Ouvez le dossier `C:\Users\{User}\AppData\Local\Pal\Saved\SaveGames\{STEAMID64}` dans lequel `{User}` correspond au nom de la session windows utilisé et {STEAMID64} à votre SteamID64.
-> Dans ce dossier vous trouverez un dossier pour chaque installation de serveur auquel vous vous êtes connecté.

- Localiser le dossier de l'ancienne sauvegarde, ici ce sera `42679FFB7E0B4775A46948D3E6238455`
- Localiser le dossier de la nouvelle sauvegarde, ici ce sera `A308DA0E450C4734BF7224FAA288A9E3`.

- Dans le dossier de la nouvelle sauvegarde, renommer le fichier `LocalData.sav` en `_LocalData.sav`
- Copier le fichier `LocalData.sav` qui se trouve dans l'ancienne sauvegarde, dans le dossier de la nouvelle sauvegarde.

- ***Connectez-vous et profiter :)***
