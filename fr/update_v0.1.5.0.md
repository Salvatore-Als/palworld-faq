
### Fix mise à jour v0.1.5.0

#### Création d'une nouvelle installation

Dans le panel, dan l'onglet `Jeux` créez une nouvelle installation de Palworld. (Vos données actuelles seronts conservées)
Modifiez l'installation active pour la nouvelle installation et redémarrez une première fois le serveur.

#### Récupération de la sauvegarde de l'ancienne installation

Éteignez le serveur. 

Dans l'accès FTP, copiez le _contenu_ du dossier de sauvegarde de l'ancienne installation et collez le dans de dossier de de sauvegarde de la nouvelle installation.
Ne copiez PAS le dossier en lui-même.

Si le dossier de l'ancienne sauvegarde est
> 42679FFB7E0B4775A46948D3E6238455
Et que le dossier de la nouvelle installation est
> A308DA0E450C4734BF7224FAA288A9E3

Vous devez copiers les fichiers 
 - 42679FFB7E0B4775A46948D3E6238455/Players
 - 42679FFB7E0B4775A46948D3E6238455/Level.sav
 - 42679FFB7E0B4775A46948D3E6238455/LevelMeta.save
dans le dossier `SaveGames/0/A308DA0E450C4734BF7224FAA288A9E3`

Lorsque la copie est terminée vous pouvez relancer le serveur.

#### Récupération de la progression (doit être fait par chaque joueur)

Les données de progression (tutoriel, découverte de la carte) sont enregistrées coté client (sur l'ordinateur des joueurs). Chaque joueur devra faire la manipulation suivante s'il souhaite conserver sa progression.

Connectez-vous une première fois au serveur pour que le jeu crée le dossier avec la progression sur la nouvelle installation de jeu du serveur. Puis fermez le jeu.

Ouvez le dossier `C:\Users\{User}\AppData\Local\Pal\Saved\SaveGames\{Palworld-user-ID}` dans lequel `{User}` correspond au nom de la session windows utilisé et {Palworld-user-ID} à votre id Palworld.
Dans ce dossier vous trouverez un dossier pour chaque installation de serveur auquel vous vous êtes connecté.

Pour retrouver à quoi correspond quel fichier il faut comparer les dates de modification.
Si vous ne vous êtes pas connecté à d'autre serveurs entre-temps :

 1 Le dossier le plus récemment modifié correspond aux données de la nouvelle installation sur le serveur. Renommez le en y ajoutant un préfixe ou un suffixe reconaissable (tiret bas, la date ou autre).
 2 Le second dossier le plus récemment modifié correspond aux données de l'ancienne installation sur le serveur. Copiez-le et renommez la copier avec le nom du nouveau dossier.

![Manipulation coté client expliquée en image](../img/Update_0.1.5.0_clientside.png?raw=true)
