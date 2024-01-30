### How to find your player's save

A player is assigned a connection number, the `playeruid`, visible via the command `/ShowPlayers`:

```plaintext
name,      playeruid,  steamid
VeryGames, 2890613232, 76561197970000000
```
This `playeruid` corresponds to the decimal value of the first 8 digits of the save file names, which are actually hexadecimal values.

If you're having trouble understanding, no problem.

By using this tool [here](https://palworld.kriax.ovh/id-finder) and copying the name of the `.sav` file, for example `4BD87C2145BCD3916C05D8B0498854D8.sav`, it will directly provide you with the corresponding playeruid.

<img width="350" alt="image" src="https://github.com/Salvatore-Als/palworld-faq/assets/58212852/a81dd3bf-1f86-4757-8f4e-42c044672b06">

In this example, the **file** is `AC4B41F0000000000000000000000000.sav` and the **playeruid** is `2890613232`, as indicated in the result of the `/ShowPlayers` command.
