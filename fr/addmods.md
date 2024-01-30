### Comment installer un mod sur mon serveur VeryGames ?

#### # Avant tout, il faut comprendre quelques points :

- Le modding n'est pas encore officiel !

- Les mods de type model/skin ne sont pas utilisables sur un serveur, c'est ce qu'on appelle du client side only.
- Les mods installés sur un serveur doivent être installés sur le jeu de chaque joueur.
- Les mods côté client ont un but "visuel".
- Les mods côté serveur ont un but de fonctionnalité et de configuration.

- Les mods peuvent corrompre votre sauvegarde, gardez ceci à l'esprit ! N'hésitez pas à sauvegarder celle-ci.
- Un mod compatible côté client n'est pas nécessairement compatible côté serveur ! Pour le moment, nous n'avons aucun moyen de le savoir, sauf si son créateur a ajouté l'information dans sa documentation.

- L'installation de certains mods se fait sur une partie VIERGE sans joueurs et sans monde, le mods n'aurais aucun effet en cours de partie.

- Le modding est actuellement limité à Windows. Si vous utilisez un serveur Linux, vous devrez créer une nouvelle installation via l'onglet JEUX.
  
#### # Exemple avec le mod `vuxWeightIncrease` qui permet d'augmenter le poids maximum pour les personnages

Tous les joueurs doivent l'installer. 

Ensuite, si les joueurs configurent le mod sur `500` et le serveur sur `800`, la valeur sera de `800  étant donné que **c'est le serveur qui fait office de configuration**.

Si un client n'a pas le mod, il ne verra pas le changement. La modification sera normalement en place *mais ce n'est pas certain* (j'ai besoin de retour d'information sur ceci).

*Partagez donc tous les mods avec vos amis, c'est très important*

#### # Installer un mod sur votre jeu

***Sauter cette étape si vous avez déjà installé UE4SS.***

Pour installer un mod côté client, vous devez télécharger [cet outil](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/v2.5.2) et l'installer dans `/{Gameroot}/Pal/Binaries/Win64/`.
`Gameroot` étant où est installé votre jeu (Steam, disque dur externe, etc).

Les mods doivent se mettre dans le dossier `/{Gameroot}/Pal/Binaries/Win64/Mods`.
Ensuite, si le mod contient `Enabled.txt`, celui-ci sera automatiquement lancé.

Sinon, dans le fichier `/palworld_windows - verygames/Pal/Binaries/Win64/Mods/mods.txt`, vous pouvez y mettre :
```plaintext
NomDuMod : 1 (pour activer)
NomDuMod : 0 (pour désactiver)
````
*`NomDuMod` étant le nom du dossier*

Si un mod est en `Enabled.txt` et que vous indiquez `0` dans le fichier `mods.txt`, celui-ci sera désactivé.

Supprimer le dossier `CACHE` ainsi que les fichiers `imgui.ini` et `UE4SS.log` qui se trouve dans `/palworld_windows - verygames/Pal/Binaries/Win64/`

#### # Installer un mod sur votre serveur VeryGames

Si le mod est en auto installation dans l'onglet plugin, il suffit simplement de l'installer :)

Si le mod n'est pas en auto installation, le mieux est de suivre les indications de sa documentation.

S'il n'y a pas de documentation, partons du principe que son installation est basique, donc il faut simplement le mettre dans le dossier `/palworld_windows - verygames/Pal/Binaries/Win64/Mods/`.

Ensuite, si le mod contient `Enabled.txt`, celui-ci sera automatiquement lancé.

Sinon, dans le fichier `/palworld_windows - verygames/Pal/Binaries/Win64/Mods/mods.txt`, vous pouvez y mettre :
```plaintext
NomDuMod : 1 (pour activer)
NomDuMod : 0 (pour désactiver)
````
*`NomDuMod` étant le nom du dossier*

Supprimer le dossier `CACHE` ainsi que les fichiers `imgui.ini` et `UE4SS.log` qui se trouve dans `/palworld_windows - verygames/Pal/Binaries/Win64/`

Si vous n'observez aucun changement, cela signifie que votre mod ne peut pas être utilisé dans une partie en cours ; vous devrez l'utiliser lors d'une nouvelle partie.