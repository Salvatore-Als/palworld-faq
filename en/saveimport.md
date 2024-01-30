#### Importing a backup from Another Dedicated Server or Co-op

1. Copy the backup from your old dedicated server to the new dedicated server.

2. In the `PalServer\Pal\Saved\Config\WindowsorLinuxServer\GameUserSettings.ini` file of the new server, modify `DedicatedServerName` to match the name of your backup folder. For example, if the folder name of your backup is `2E85FD38BAA792EB1D4C09386F3A3CDA`, then `DedicatedServerName` becomes `DedicatedServerName=2E85FD38BAA792EB1D4C09386F3A3CDA`.

    2. **CO-OP:** Delete the file `PalServer\Pal\Saved\SaveGames\0\<YOUR_SAVE_ID>\WorldOption.sav` to allow modification of the `PalWorldSettings.ini` file. Players will no longer have their spawn points but that's it.

3. Start the new server and ask each player to create a new character. When a player creates a new character, a new `.sav` file will appear in `PalServer\Pal\Saved\SaveGames\0\<YOUR_SAVE_ID>\Players`. The name of this new `*.sav` file is the GUID of the new player. Make sure to note down all old and new GUIDs and their correspondence with players.

4. Stop the server, then copy the entirety of the new server's backup from `PalServer\Pal\Saved\SaveGames\0\<YOUR_SAVE_ID>` (this should be the backup containing all the new characters!) into a temporary folder on your computer.

5. Copy the old backups into the folder `PalServer\Pal\Saved\SaveGames\0\<YOUR_SAVE_ID>\Players`.

6. Make a backup of your backup! This will execute an experimental script (https://github.com/xNul/palworld-host-save-fix/blob/main/fix-host-save.py) with known bugs, so always make sure to keep a backup copy.

7. Download `server-to-serv-wrapping.bat` (https://github.com/Salvatore-Als/palworld-faq/releases/download/uesave/server-to-serv-wrapping.bat) into the folder where you have your backup. So you should have:
```
- your_folder
-- {YOUR_SAVE_ID}
--- Level.sav
--- LevelMeta.sav
---- Players
------ {PLAYER_SAV_ID}.sav
------ {PLAYER_SAV_ID}.sav
------ {PLAYER_SAV_ID}.sav
```

8. The wrapper will download `uesave.exe` and `fix-host-save.py` and ask you for the ID of the backup as well as the old player's ID and the new player's ID. Note that you must have Python installed.

9. Run the script for each corresponding pair of old GUID and new GUID.

   **The script takes a long time; you'll know it's finished when you see `Fix has been applied! Have fun!`.**
   **Note that this guide does not cover Python installation!**

10. Copy the backup from the temporary folder back to the dedicated server. Move or rename the backup you had in the dedicated server to a different location.

11. Restart the server and ask each player to join the server with their corrected character.

12. If, after 5 minutes of gameplay, a player's Pals are not attacking them or not working in their base, ask them to follow the workaround solution [[Pal bug]](https://github.com/xNul/palworld-host-save-fix/blob/main/README.md#pal-bug) to fix it.
