# Space Panicco Archive

An archive and documentation project for **Space Panicco** (スペースぱにっこ), a 1994 DOS action game by BUGSOFT.

---

## VMAP Editor

A browser-based map editor for Space Panicco VMAP files (`.DAT`).

**Live tool:** https://gikonekos.github.io/Space-Panicco-Archive/tools/map-editor/

### Features

- **13 × 12 grid editor** — paint cells with mouse drag or touch
- **32 built-in maps** (ROUND 001–032) loaded from original game data
- **ROUND 001–999 support** — navigate with the numeric input field (arrow keys also work)
- **Load / Save** — reads and writes CP932-encoded `.DAT` files with DOS EOF (0x1A)
- **Copy** — duplicate any round to another slot
- **Undo / Redo** — 50-step history (Ctrl+Z / Ctrl+Y)
- **Keyboard shortcuts** — `SPC` `1` `2` `7` `H` `M` `A` `B` `C` `Q` `W` `E`
- **Touch support** — drag to paint on tablet/mobile
- **MAP INFO panel** — live counts for all symbol types

### Save Behaviour

- Saved files are always placed in the **browser's default download folder**. This is a browser security restriction — JavaScript cannot write to arbitrary locations on the filesystem.
- If the map has **no warnings**, the file saves immediately on clicking Save.
- If the map has **warnings**, a confirmation dialog shows the warning details before saving. You can cancel to fix issues first.

### Warnings

The editor checks for map issues in real time (warning banner) and again at Save (confirmation dialog).

| Warning | Condition |
|---|---|
| PANICCO (M) missing | M not placed on the map |
| PANICCO (M) duplicated | More than 1 M on the map |
| Enemy count exceeded | More than 16 enemies total |
| Gap warning | Empty rounds exist before the current round — game displays `not open - VMAPxxx.DAT !!` |
| Freeze risk | Enemy (A/B/C) has no reachable floor below — enemy will freeze on spawn |
| Dead-end freeze | Enemy can land, but the landing row has fewer than 2 consecutive free spaces in either direction — enemy may freeze after landing |

> **Note on Dead-end freeze warnings:** This check has known detection gaps (e.g. stepping-stone floor patterns). If you are confident the placement is correct, the warning can be safely ignored.

### Known Game Behaviour

- An empty map does not crash — the stage is unwinnable but the game continues.
- PANICCO (M) is optional at runtime — she spawns from above even without an `M` tile.
- Normal enemies (A/B/C) require at least one adjacent floor cell. Without one, the enemy freezes immediately.
- **Enemy overflow:** If more than 16 enemies are placed, the game loads only the first 16 and ignores the rest. No crash occurs.
- Skipped round numbers cause the game to display `not open - VMAPxxx.DAT !!` and show an empty stage.

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
| v1.4 | Gap warning, basic freeze warning |
| v1.5 | Dead-end freeze warning (landing row with fewer than 2 free spaces in either direction) |
| v1.5.1 | Fixed false-positive dead-end freeze when enemy row equals landing row; Save confirmation dialog added |
| v1.5.2 | Confirmation dialog shown only when warnings exist; immediate save when map is clean |

---

## Repository

- **SC62015 opcode reference:** https://github.com/gikonekos/sc62015-opcode-reference
- Featured on Hackaday

---

*1994 © BUGSOFT. Archive project for preservation purposes.*
