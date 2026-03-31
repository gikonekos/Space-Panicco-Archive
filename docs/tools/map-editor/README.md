# Space Panicco Archive

An archive and documentation project for **Space Panicco** (スペースぱにっこ), a 1994 DOS action game by BUGSOFT.

---

## VMAP Editor

A browser-based map editor for Space Panicco VMAP files (`.DAT`).

**Live tool:** https://gikonekos.github.io/Space-Panicco-Archive/tools/map-editor/

### Features

- **13 × 12 grid editor** — paint cells with mouse drag or touch
- **32 built-in maps** (ROUND 001–032) loaded from original game data
- **ROUND 001–999 support** — navigate with the numeric input field
- **Load / Save** — reads and writes CP932-encoded `.DAT` files with DOS EOF (0x1A)
- **Copy** — duplicate any round to another slot
- **Undo / Redo** — 50-step history (Ctrl+Z / Ctrl+Y)
- **Keyboard shortcuts** — `SPC` `1` `2` `7` `H` `M` `A` `B` `C` `Q` `W` `E`
- **Touch support** — drag to paint on tablet/mobile
- **MAP INFO panel** — live counts for all symbol types

### Warnings

The editor automatically checks for common map issues and displays a warning banner:

| Warning | Condition |
|---|---|
| PANICCO (M) missing | M not placed on the map |
| PANICCO (M) duplicated | More than 1 M on the map |
| Enemy count exceeded | More than 16 enemies total |
| Gap warning | Empty rounds exist before the current round — game displays `not open - VMAPxxx.DAT !!` |
| Freeze risk | Enemy (A/B/C) has no reachable floor below — enemy will freeze on spawn |
| Dead-end freeze *(v1.5)* | Enemy can land, but the landing row has fewer than 2 consecutive free spaces in either direction — enemy may freeze after landing |

### Symbol Reference

| Symbol | Key | Description |
|---|---|---|
| (SP) | Space | Road — open space enemies walk on |
| `1` | 1 | Block — solid wall |
| `2` | 2 | Floor — platform |
| `7` | 7 | Hole |
| `H` | H | Ladder |
| `M` | M | PANICCO (player start) |
| `A` | A | SLIMER (enemy) |
| `B` | B | EBYRINS (enemy) |
| `C` | C | ZAUROID (enemy) |
| `ｱ` | Q | SLIMER — fall spawn |
| `ｲ` | W | EBYRINS — fall spawn |
| `ｳ` | E | ZAUROID — fall spawn |

### Known Game Behaviour

- An empty map does not crash — the stage is unwinnable but the game continues.
- PANICCO (M) is optional at runtime — she spawns from above even without an `M` tile.
- Normal enemies (A/B/C) require at least one adjacent floor cell. Without one, the enemy freezes immediately.
- **Dead-end freeze (v1.5):** Even when an enemy successfully lands, it may freeze if the landing row offers fewer than 2 consecutive free spaces in either direction. The editor warns about this pattern.
- Skipped round numbers cause the game to display `not open - VMAPxxx.DAT !!` and show an empty stage.

### File Format

Each `.DAT` file is a 12-line CP932 text file:

```
<13 map characters><optional extra><comment>\r\n
...
\x1a  (DOS EOF)
```

Half-width katakana (`ｱ` `ｲ` `ｳ`) are written as raw CP932 bytes (0xB1 / 0xB2 / 0xB3).

---

## Version History

| Version | Changes |
|---|---|
| v1.1 | 32 built-in maps, round selector |
| v1.2 | English UI, warning banner moved below toolbar |
| v1.3 | ROUND 001–999 numeric input, Undo/Redo (50 steps), touch support, keyboard shortcuts |
| v1.4 | Gap warning (`checkGapWarnings`), basic freeze warning (`checkEnemyPlacement`) |
| v1.5 | Dead-end freeze warning — detects landing rows with fewer than 2 consecutive free spaces in either direction |

---

## Repository

- **SC62015 opcode reference:** https://github.com/gikonekos/sc62015-opcode-reference
- Featured on Hackaday

---

*1994 © BUGSOFT. Archive project for preservation purposes.*
