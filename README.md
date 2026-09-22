# Qapacity
Simple QuakeC mod that adds ammo and health upgrades similar to the Dawn Of The Machine episode, albeit applied to vanilla Quake entities.

It also works in multiplayer!

## Requirements
A vanilla Quake installation (either the original game or LibreQuake). I've tested both in QSS-M and Ironclaw.

## Installation
Put the `qapacity` folder in your Quake root folder (same directory as your id1 folder).

To activate the mod you can either
- Use a shortcut with the `-game "qapacity"` parameter
- Run `game "qapacity"` from the game's console
- Select `qapacity` from your source port's mod menu (if available)

You might be able to use Qapacity with mappacks, as long as they don't have their own progs.dat for custom behavior. Copy the progs.dat from the `qapacity` folder into the mappack's folder and run that mod instead.

## How does it work?
Upon starting a new game, the player has a base capacity of

| Health | Shells | Nails | Rockets | Cells |
|--------|--------|-------|---------|-------|
|   50   |   20   |   20  |    5    |  20   |

Picking up weapons or megahealth changes the corresponding capacity by

| Health | Shells | Nails | Rockets | Cells |
|--------|--------|-------|---------|-------|
|  +10   |  +10   |  +20  |   +5    |  +10  |

Megahealth will also add your new maximum health's worth of points to your current health.

In practice, you'll always start one ammo upgrade higher than the base once you pick up a weapon that can actually use the ammo, so 40 for nails, 10 for rockets, etc., with the only exception being the shotgun since you start with it.

The net result is that the game is going to be harder. Seeking out secrets will give you an edge, even beyond the vanilla game's standard limits.

## Future ideas
I want to add different starting points and upgrade sizes for different difficulties, I'm also looking into Clientside QuakeC to add a HUD element showing your current caps. I might try to implement more features.

## Credits / Special Thanks
- id Software for making Quake and the original source code
- LibreQuake for the source files I used to make this (and LibreQuake is cool, you should try it)
- The Quake community (especially The Quake Wiki) for providing a lot of material for digesting QuakeC