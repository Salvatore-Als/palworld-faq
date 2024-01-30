### Comment trouver la sauvegarde de mon personnage

Un joueur se voit attribuer un numéro de connexion, le `playeruid`, visible via la commande `/ShowPlayers` :

```plaintext
name,      playeruid,  steamid
VeryGames, 2890613232, 76561197970000000
```

Ce `playeruid` correspond à la valeur décimale des 8 premiers chiffres du nom des fichiers de sauvegarde, qui sont en réalité une valeur hexadécimale.

Si vous avez du mal à comprendre, pas de problème. 

En utilisant cet outil [ici](https://palworld.kriax.ovh/id-finder) et en copiant le nom du fichier `.sav`, par exemple `4BD87C2145BCD3916C05D8B0498854D8.sav`, il vous fournira directement le playeruid correspondant.

<img width="350" alt="image" src="https://github.com/Salvatore-Als/palworld-faq/assets/58212852/a81dd3bf-1f86-4757-8f4e-42c044672b06">

Dans cet exemple, le **fichier** est `AC4B41F0000000000000000000000000.sav` et la **playeruid** est `2890613232`, comme indiqué dans le résultat de la commande `/ShowPlayers`.