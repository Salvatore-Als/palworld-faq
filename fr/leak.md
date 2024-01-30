### Memory Leak

Il y a quelques événements qui se produisent dans le jeu et sont supposés causer des fuites de mémoire.

Actuellement, il existe une façon de lutter contre cela.

Définissez `bEnableInvaderEnemy=False` dans votre fichier `PalWorldSettings.ini` 

Les Événements supposés causer un problème :

- Rejoindre les donjons de manière répétée.
- Événements de raid.
- Les Pals de groupe travaillant sur la base ont été vus "déplacer" des objets, mais sortent des limites et les laissent tomber de manière répétée. Cela conduit à une grande accumulation de ressources sur le chemin des Pals.