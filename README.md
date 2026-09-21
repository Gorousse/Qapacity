# qapacity
Simple progs.dat-based mod that adds ammo and health upgrades similar to the Dawn Of The Machine episode, albeit applied to vanilla Quake entities. It also works in multiplayer!

## Requirements
A vanilla Quake installation (either the original game or LibreQuake). I've tested both in QSS-M and Ironclaw.

Mappacks might work if they don't have their own progs.dat for custom behavior.

## Installation
Put the `qapacity` folder in your Quake root folder (same directory as your id1 folder).

To activate the mod you can either
- Use a shortcut with the `-game "qapacity"` parameter
- Run `game "qapacity"` from the game's console
- Select `qapacity` from your source port's mod menu (if available)

## How does it work?
Upon starting a new game, the player has a base capacity of

|  Stat   | Capacity |
|---------|-----|
| Health  | 50  |
| Shells  | 20  |
| Nails   | 20  |
| Rockets | 5   |
| Cells   | 20  |

Picking up Megahealth will increase your max_health by 10 as well as adding 100 to your current health like always.

Picking up weapons increases the corresponding ammo's capacity by:

|  Ammo   | Capacity |
|---------|-----|
| Shells  | 10  |
| Nails   | 20  |
| Rockets | 5   |
| Cells   | 10  |

In practice, you'll always start one "step" higher than the base once you pick up a weapon that can actually use the ammo, so 40 for nails, 10 for rockets, etc., except for the shotguns obviously.

## Future plans
I didn't think I'd have this running in a single afternoon, let alone in multiplayer but here we are. I want to add different starting points and capacity upgrades for different difficulties