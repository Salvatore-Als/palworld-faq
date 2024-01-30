### How to install a mod on your VeryGames server ?

#### # First and Foremost, Understand Some Key Points:

- Modding is not yet official!

- Model/skin type mods are not usable on a server, known as client-side only.
- Mods installed on a server must also be installed on each player's game.
- Client-side mods serve a visual purpose.
- Server-side mods serve functionality and configuration purposes.

- Mods can corrupt your save file, so keep this in mind! Don't hesitate to back it up.
- A client-compatible mod may not necessarily be compatible server-side! Currently, we have no way of knowing unless the creator has provided this information in their documentation.

- Installing some mods requires a GAME without players and without a world; otherwise, the mods will have no effect mid-game.

- Modding is currently limited to Windows. If you're using a Linux server, you'll need to create a new installation via the GAMES tab.
  
#### # Example with the `vuxWeightIncrease` mod, which allows increasing the maximum weight for characters

All players must install it. 

Then, if players configure the mod to `500` and the server to `800`, the value will be `800` since **the server acts as the configuration**.

If a client doesn't have the mod, they won't see the change. The modification will normally be in place, *but it's not certain* (feedback is needed on this).

*Therefore, share all mods with your friends; it's crucial*

#### # Installing a Mod on Your Game

***Skip this step if you've already installed UE4SS.***

To install a client-side mod, you need to download [this tool](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/v2.5.2) and install it in `/{Gameroot}/Pal/Binaries/Win64/`.
`Gameroot` is where your game is installed (Steam, external hard drive, etc).

Mods should be placed in the folder `/{Gameroot}/Pal/Binaries/Win64/Mods`.
Then, if the mod contains `Enabled.txt`, it will be automatically launched.

Otherwise, in the file `/palworld_windows - verygames/Pal/Binaries/Win64/Mods/mods.txt`, you can specify:
````
ModName : 1 (enabled)
ModName : 0 (disabled)
``````

*`ModName` is the folder name*

If a mod is in `Enabled.txt` and you specify `0` in the `mods.txt` file, it will be deactivated.

Delete the `CACHE` folder as well as the files `imgui.ini` and `UE4SS.log` located in `/palworld_windows - verygames/Pal/Binaries/Win64/`

#### # Installing a Mod on Your VeryGames Server

If the mod is set for auto-installation in the plugin tab, simply install it :)

If the mod doesn't have auto-installation, it's best to follow its documentation.

If there's no documentation, assume its installation is basic, so simply place it in the folder `/palworld_windows - verygames/Pal/Binaries/Win64/Mods/`.

Then, if the mod contains `Enabled.txt`, it will be automatically launched.

Otherwise, in the file `/palworld_windows - verygames/Pal/Binaries/Win64/Mods/mods.txt`, you can specify:

````
ModName : 1 (enabled)
ModName : 0 (disabled)
``````

*`ModName` is the folder name*

Delete the `CACHE` folder as well as the files `imgui.ini` and `UE4SS.log` located in `/palworld_windows - verygames/Pal/Binaries/Win64/`.

If you don't observe any changes, it means that your mod cannot be used in the ongoing game session; you will need to use it in a new game.