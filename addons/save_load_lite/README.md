# SELODEV RPG Starter

A small, finished town-square errand you can press Play on, plus every free
SELODEV Lite system already sitting in the project. No coding required.

Gather the town's lost coins, talk to the shopkeeper, buy the traveler's sword,
and equip it. Movement is the Controller system, the shopkeeper greets you
through the Dialogue system, your gold is the Vendor system's wallet, the
purchase is a real Vendor transaction that drops the sword into your Inventory
satchel, the sword sits in the Equipment system's weapon slot, and equipping it
raises your Attack through the Stats system's modifier math. The checklist is a
Quest. That is eight Lite systems in one small game. All fourteen are in
`addons/`, wired through one event bus.

## Play it (Godot 4.5 or newer)

Open this folder in Godot and press **Play (F5)**.

- **Move:** arrow keys or WASD
- **Gather** the coins that light up around the square
- **Talk:** walk up to the stall and the shopkeeper offers the sword. Pick "Buy"
  and the gold leaves your purse, the blade lands in your satchel, and it equips.
- **Watch the bar:** gold and satchel on the left, Attack on the right
- **Save and Load:** buttons at the top right

## Make it yours

- `content/quests.json` is the errand and `content/dialogue.json` is what the
  shopkeeper says. Change either. No scripts.
- The sword is `game/rpg/items/sword.tres`: id, name, icon, and the slot it
  equips to. The vendor's stock and price sit on the `Vendor` node in the
  Inspector, and the sword lands in the `Satchel` Inventory on purchase.
- Your Attack stat is `game/rpg/attack_stat.tres`. The +5 gear bonus is one
  modifier line in `game/rpg/rpg_player.gd`.
- `game/art/kenney/` is the pixel art, CC0 from Kenney's Tiny Town and Tiny
  Dungeon packs (credits in `CREDITS.md`). Overwrite a PNG with your own and
  the game picks it up. The houses are region sprites cut from
  `town_sheet.png`, so a new region rect is a new building.
- The square is two rects on the `Ground` node: `town` and `plaza`. Resize
  them in the Inspector and the tree line, collision and camera follow.
- Nine more systems ship switched off. Turn one on in Project Settings then
  Plugins when your game wants it.

## Run the checks yourself

```bash
godot --headless --path . tools/rpg/verify.tscn
```

Every other system carries its own suite under `tools/` as well.

## Growing out of the Lite tier

Each Lite system is the free cut of a paid one. The full versions of everything
in this project, plus the Game Kit that wires them together, ship in one
package: **SELODEV Complete** on https://selodev.com/go/complete. One purchase, every
system, already wired into a running game. The full systems install next to the
Lites here without breaking anything, but this project's scripts talk to the
Lites, so moving it over means updating those scripts.

## License

MIT for the kit. The art is CC0, credited in `CREDITS.md`. Make it, rename it,
ship it, sell it. That's the point.


## Part of a family

This is one free tier from the selodev catalog of no-code Godot 4 systems. They share an item contract and a save contract, so they plug into each other, and each one also works fully on its own.

Free systems:

- [Inventory Lite](https://github.com/seloc0des/godot-inventory-lite)
- [Equipment Lite](https://github.com/seloc0des/godot-equipment-lite)
- [Loot Lite](https://github.com/seloc0des/godot-loot-lite)
- [Crafting Lite](https://github.com/seloc0des/godot-crafting-lite)
- [Vendor Lite](https://github.com/seloc0des/godot-vendor-lite)
- [Quests Lite](https://github.com/seloc0des/godot-quests-lite)
- [Stats / Skills Lite](https://github.com/seloc0des/godot-stats-skills-lite)
- [Save / Load Lite](https://github.com/seloc0des/godot-save-load-lite)
- [Dialogue Lite](https://github.com/seloc0des/godot-dialogue-lite)
- [Combat Lite](https://github.com/seloc0des/godot-combat-lite)
- [Controller Lite](https://github.com/seloc0des/godot-controller-lite)
- [Enemy AI Lite](https://github.com/seloc0des/godot-enemy-ai-lite)
- [Scene Flow Lite](https://github.com/seloc0des/godot-scene-flow-lite)
- [Audio Lite](https://github.com/seloc0des/godot-audio-lite)
- [Level Builder Lite](https://github.com/seloc0des/godot-level-builder-lite)
- [Weather System Lite](https://github.com/seloc0des/godot-weather-lite)
- [Settings + Menus](https://github.com/seloc0des/godot-settings-menus) (complete and free, no paid tier)

Free VFX: [Magic Cast](https://github.com/seloc0des/godot-magic-cast-vfx-lite), [Elemental Impact](https://github.com/seloc0des/godot-elemental-impact-vfx-lite), [Explosion](https://github.com/seloc0des/godot-explosion-vfx-lite), [Pickup, Buff & Heal](https://github.com/seloc0des/godot-pickup-buff-vfx-lite).

Free starter projects: [Free Starter](https://github.com/seloc0des/free-starter-godot), [Dungeon](https://github.com/seloc0des/godot-dungeon-starter), [Survival](https://github.com/seloc0des/godot-survival-starter), [RPG](https://github.com/seloc0des/godot-rpg-starter).

The full versions add drop-in UI, editor docks and the cross-system wiring. They're on itch.io: **https://selodev.itch.io**
