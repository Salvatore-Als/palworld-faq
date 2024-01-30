### Récupération d'une Sauvegarde Antérieure

Dans le répertoire `/backups`, vous pouvez accéder aux sauvegardes des 48 dernières heures de votre serveur. Chaque sauvegarde est réalisée toutes les 30 minutes.

#### Instructions :

1. **Arrêtez votre Serveur :**
   Assurez-vous d'arrêter votre serveur et attendez qu'il soit hors ligne.

2. **Renommez le Dossier :**
   Dans votre dossier `/palworld - verygames/Pal/Saved/SaveGames/0`, localisez le dossier avec un ID (par exemple, `F55CA874D1754520AF7DD397F9A4CC0E`). Renommez ce dossier en ajoutant un préfixe (par exemple, `__F55CA874D1754520AF7DD397F9A4CC0E`) pour qu'il ne soit plus pris en compte.

3. **Sélectionnez une Sauvegarde :**
   Accédez au dossier `/palworld - verygames/Pal/Saved/SaveGames/backups`. Les sauvegardes sont nommées en fonction de la date et de l'heure. Choisissez la sauvegarde la plus récente.

4. **Téléchargez la Sauvegarde :**
   Téléchargez le dossier correspondant à votre sauvegarde (utilisez Filezilla, par exemple). Assurez-vous qu'il porte le même ID que votre sauvegarde principale (dans notre exemple, `F55CA874D1754520AF7DD397F9A4CC0E`).

5. **Restaurez la Sauvegarde :**
   Retournez dans le dossier `/palworld - verygames/Pal/Saved/SaveGames/0` et téléversez le dossier de votre sauvegarde.

6. **Redémarrez le Serveur :**
   Redémarrez votre serveur et connectez-vous.

#### Résultats Attendus :

- Si la sauvegarde est valide, vous devriez retrouver votre inventaire et vos personnages. Vous aurez simplement perdu le temps de jeu entre la corruption de la sauvegarde et l'heure de votre backup. Vous pouvez alors supprimer l'ancienne sauvegarde préfixée (dans notre exemple, `__F55CA874D1754520AF7DD397F9A4CC0E`).

- Si la sauvegarde n'est pas valide, essayez une autre sauvegarde en la téléversant dans le dossier `/palworld - verygames/Pal/Saved/SaveGames/0`. Répétez ces étapes jusqu'à trouver une sauvegarde valide.
