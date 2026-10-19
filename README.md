# Valheim Block Planner

See which enemy attacks you can block or parry in Valheim, using your own character.

**Live page:** [https://talhatayob.github.io/Valheim_Block_Calculator/](https://talhatayob.github.io/Valheim_Block_Calculator/)

Drop your character file on the page. It reads your shield, armour, Blocking skill and max health, then shows every enemy attack in the game with what happens when you take it unblocked, blocked or parried.

## Features

- **Block & parry:** every enemy attack from the Meadows to the Deep North (Valheim 1.0). Each one shows:
  - whether your block holds, you get staggered, or your guard breaks
  - how much health you lose
  - the max health you'd need to take it cleanly
- **Planner:** try other shields, armour, Blocking skill levels, max health, meads and boss powers before you craft or grind anything. Filter the gear lists by the biome the gear comes from, or search them by name.
- **Conditions:** combat difficulty (Very easy to Very hard), enemy stars, and multiplayer scaling for players nearby.
- **Character overview:** skills, inventory, stats, discoveries, and what your file records about cheats and achievement tracking.

## How to use it

1. Open the page.
2. Drop your `.fch` character file on it, or click to choose it. On Windows, local saves are in:
   ```
   %USERPROFILE%\AppData\LocalLow\IronGate\Valheim\characters_local
   ```
   Steam Cloud saves are in `<Steam folder>\userdata\<your Steam ID>\892970\remote\characters`. You can open those directly, or move the character to local in the game first.
3. Open the **Block & parry** tab.

You don't need a save to use it: the page opens with an example character, and the Planner works on its own.

## Privacy

Everything runs in your browser. Your file is never uploaded, and the page never changes it.

## How the numbers are worked out

- **Enemy damage** is scaled by combat difficulty, enemy stars and players nearby. A few hits, like death explosions and shockwaves, don't scale with stars.
- **Block power** is your shield's block armour at its level, plus 0.5% per Blocking skill point. A parry multiplies it by the shield's parry bonus.
- **Blocking reduces a hit the same way armour does.** Blunt, slash, pierce and lightning damage that gets through fills your stagger bar, which holds 40% of your max health.
- **What gets through** then goes through your resistances and body armour.
- **Gear biomes** come from the materials in each item's recipe. Troll leather counts as Black Forest, for example, and Wolf gear as Mountains.

The page's "How this is worked out" section has the details.

**Limits:**
- Each result assumes an empty stagger bar.
- Stamina isn't modelled.
- Damage shown is the strongest roll of each hit.
- Numbers match Valheim 1.0 (patch 1.0.20) and may drift after future patches.
- The Deep North Greydwarf variants and Fader's summoned helpers couldn't be checked against the wiki.

Spotted a wrong number? Open an issue with the enemy, the attack and where you saw the correct value.

## Sources and credits

- **Game data:** enemy attacks, shields, armour and recipes come from [kirilloid/valheim](https://github.com/kirilloid/valheim) by kirilloid, the data behind [valheim.kirilloid.ru](https://valheim.kirilloid.ru/). Many thanks.
- **Enemy attack corrections:** every enemy was checked against the [Valheim Wiki](https://valheim.weirdgloop.org/) in October 2026. Where they differed, the wiki's values are used. That covers 15 enemies, including Stone Golem, Fader, Kall Fimbulbringer and Krigen.
- **Blocking, parry and stagger rules:** the [Valheim Wiki](https://valheim.weirdgloop.org/w/Blocking) and [valheim.tools](https://www.valheim.tools/guides/combat), checked against the order of operations in the [Stagger Scaler](https://github.com/Babrushka/Stagger-Scaler) mod.

## Legal

This is a fan-made, non-commercial tool. It is not affiliated with or endorsed by Iron Gate AB or Coffee Stain Publishing.

Valheim and all related names, game data and content are the property of [Iron Gate](https://irongatestudio.se/) and [Coffee Stain](https://www.coffeestainstudios.com/). Game content is used for this free companion tool in line with the game's EULA on the [Valheim website](https://www.valheimgame.com/), the same terms the kirilloid project points to. If you reuse anything here, check that EULA too.

The page only reads character files that players choose to open themselves. It does not modify game files, and it is provided as is, without any warranty.
