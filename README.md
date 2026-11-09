# Accio for RuneScape: Dragonwilds

A spell mod for RuneScape: Dragonwilds: summon items to you. It runs on the
[Spell Framework](https://github.com/MichaelRyan2319/RSDragonwilds-SpellFramework).

Accio is one entry in the Spellbook. Casting it opens a wheel with two variants:

| Variant | What it does | Runes | Cooldown |
| --- | --- | --- | --- |
| **Accio** | Type an item's name (it autocompletes) and it flies from nearby storage into your bag. Linked chests within 30 m count. Add an amount, e.g. `20 clay`. Runes are only used when something arrives. | 1 Law, 1 Air | 2 s |
| **Accio Everything** | Every item lying on the ground within 25 m flies to you. | 1 Law, 3 Air | 10 s |

- Works in your own world (single player, or as the host).
- Your saves stay valid with or without the mod. See the Spell Framework's
  README for how.
- Doesn't change any world settings, so achievements keep working.

## Requirements

- [UE4SS for RuneScape: Dragonwilds](https://github.com/MichaelRyan2319/RSDragonwilds-UE4SS)
- [Spell Framework](https://github.com/MichaelRyan2319/RSDragonwilds-SpellFramework)

## Install with Mod Loader

[Mod Loader](https://github.com/MichaelRyan2319/ModLoader) installs the mod and
keeps it up to date.

1. **Add game** and pick RuneScape: Dragonwilds. Mod Loader 1.0.1 or later sets
   the mods folder to the game's inner `RSDragonwilds` folder (the one with
   `Binaries` and `Content` in it).
2. **Add mod** `MichaelRyan2319/RSDragonwilds-AccioSpell`. Mod Loader 1.1.0 or
   later offers to add UE4SS and the Spell Framework as well; click **Yes**. With
   an older Mod Loader, add `MichaelRyan2319/RSDragonwilds-UE4SS` and
   `MichaelRyan2319/RSDragonwilds-SpellFramework` yourself first.
3. Start the game and load your world.

## Install by hand

1. Install UE4SS and the Spell Framework (see Requirements).
2. Download `AccioSpell.zip` from the [Releases](../../releases) page and
   extract it into the game's `RSDragonwilds` folder (the one with `Binaries` and
   `Content` in it). In Steam, right-click RuneScape: Dragonwilds > Manage >
   Browse local files to find it. The spell ends up in
   `Binaries\Win64\ue4ss\Mods\SpellFramework\Spells\Accio.lua`.
3. Start the game and load your world.

## Using it

1. Press **P** to open the Spellbook, open **Custom Spells** and drag Accio into
   a slot of the spell radial.
2. Press **Q** to open the spell radial and cast Accio, then pick a variant from the wheel.
3. For **Accio**, type part of the item's name, choose a suggestion with Up/Down
   (Tab completes it) and press Enter. The cast animation plays and the items
   arrive. Esc cancels without using runes.

The ranges (`STORAGE_RANGE`, `GROUND_RANGE`) are at the top of `Accio.lua`. An
update replaces that file, so change them again after an update.

## Uninstall

Remove it in Mod Loader, or delete
`Win64\ue4ss\Mods\SpellFramework\Spells\Accio.lua`. Radial slots that held
Accio show Siphon Runes.
