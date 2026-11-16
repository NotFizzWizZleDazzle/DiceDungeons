# Dice Dungeons

A side-scrolling dungeon crawler made with Drift. Roll through an endless dungeon as a spinning top and fight living dice with spells.

```sh
drift run .
```

## Controls

- A / D: move
- W or Space: jump
- Left click: cast spell
- Right click: shield
- 1-5, Q, E: switch spell

Defeated dice drop upgrade cards.

## Enemies

A die's face is its health. d6s charge you up close; d4s shoot from range. Both warn you before they attack.

Set `difficulty` under `[enemy_ai]` in `drift.toml` to make them easier or harder.
