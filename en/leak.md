### Memory Leak

There are a few events that occur in the game and are supposed to cause memory leaks.

Currently, there is a way to mitigate this.

Set `bEnableInvaderEnemy=False` in your `PalWorldSettings.ini` file.

Events known to cause an issue:

- Repeatedly joining dungeons.
- Raid events.
- Group Pals working on the base have been seen "moving" objects but go out of bounds and drop them repeatedly. This leads to a large accumulation of resources in the path of the Pals.