# Dice Dungeons

A side-scrolling dungeon crawler made with Drift and Candela. You are a three-pronged top rolling through an endless dungeon, casting spells at living dice.

## Play

```sh
drift run .
drift build --web .
```

- A and D roll left and right; W or Space jumps.
- Left click casts the selected spell at the mouse; right click raises a shield that blocks one hit.
- 1 to 5, Q and E pick a spell once you have more than one.
- Kills drop cards. Walk over one and pick an upgrade: new spells, more speed, health or mana.

## Enemies

Every enemy is a die whose face is its health; each hit rolls it down a face.

- d6s fight up close. Before a lunge they stop and show a shrinking red ring.
- d4s keep their distance and shoot. Before a shot they show an aim line, which stops following you just before they fire.

They patrol until they see you, hear a spell fly past, get hit or hear another die raise the alarm. They jump onto crates to reach you, go round you when one side is crowded, take turns to attack, and search where they last saw you. A die on its last faces backs off while your selected spell could finish it, and comes back when you are out of mana.

## Tuning

`[enemy_ai]` in `drift.toml` sets how hard the dice fight. `difficulty` scales reaction time, telegraph length, aim, dodging and how many attack at once; 0.5 is gentle and 1.5 is hard. The other keys are listed in `EnemyAiSettings` in `src/enemy_ai.cdl`. Set `show_states = true` to see what each die is doing, and `log_states = true` to log every change.
