### Retrieving a previous backup

In the `/backups` directory, you can access backups of your server from the last 48 hours. Each backup is made every 30 minutes.

#### Instructions:

1. **Stop Your Server:**
   Make sure to stop your server and wait for it to be offline.

2. **Rename the Folder:**
   In your `/palworld - verygames/Pal/Saved/SaveGames/0` directory, locate the folder with an ID (for example, `F55CA874D1754520AF7DD397F9A4CC0E`). Rename this folder by adding a prefix (for example, `__F55CA874D1754520AF7DD397F9A4CC0E`) so it won't be recognized anymore.

3. **Select a Backup:**
   Go to the `/palworld - verygames/Pal/Saved/SaveGames/backups` directory. Backups are named based on date and time. Choose the most recent backup.

4. **Download the Backup:**
   Download the folder corresponding to your backup (use Filezilla, for example). Make sure it has the same ID as your main save (in our example, `F55CA874D1754520AF7DD397F9A4CC0E`).

5. **Restore the Backup:**
   Go back to the `/palworld - verygames/Pal/Saved/SaveGames/0` directory and upload the folder of your backup.

6. **Restart the Server:**
   Restart your server and log in.

#### Expected Results:

- If the backup is valid, you should retrieve your inventory and characters. You will have simply lost the gameplay time between the corruption of the save and the time of your backup. You can then delete the prefixed old save (in our example, `__F55CA874D1754520AF7DD397F9A4CC0E`).

- If the backup is not valid, try another backup by uploading it to the `/palworld - verygames/Pal/Saved/SaveGames/0` directory. Repeat these steps until you find a valid backup.
