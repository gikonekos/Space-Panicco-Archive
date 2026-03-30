# Space Panicco — VMAP Editor

A browser-based map editor for **Space Panicco / すぺーす ぱにっ娘** (1994, NEC PC-9801 DOS).

---

## Overview

A self-contained editor that runs from a single `index.html` file.  
No installation or server required — just open it in a browser.

- All 32 original maps (ROUND 001–032) are built in; ROUND 033–999 are available as blank maps
- 13×12 grid with color-coded symbol display and editing
- Saves as VMAP\*\*\*.DAT (DOS EOF appended, CP932-compatible output)
- Undo / Redo (up to 50 steps)
- Keyboard shortcuts for symbol selection
- Touch input supported (iPad / smartphone)

---

## Files

| File | Description |
|---|---|
| `index.html` | The editor — everything in one file |

---

## Requirements

- **Modern desktop browser (Chrome / Edge / Firefox) — verified working**
- Open the file locally; no server needed
- Touch input (iPad / smartphones) is supported

---

## How to Use

### Launch

Open `index.html` in your browser (double-click is fine).

All 32 built-in maps load immediately. ROUND 033–999 start as empty maps.

---

### Switching Rounds

Type a round number (1–999) into the **ROUND** input field in the toolbar.

- Press **Enter** or click away to switch
- Edits are kept in memory while browsing other rounds
- Unsaved changes are lost when the browser is closed

---

### Editing

1. Click a symbol in the **SYMBOL PALETTE** to select it
2. Click or drag on the grid to place it

Selecting **Road (SP)** acts as an eraser.

#### Symbols

| Symbol | Meaning | Color |
|---|---|---|
| (SP) | Road | Dark blue |
| `1` | Block | Blue + yellow crosshatch |
| `2` | Floor | Blue-purple |
| `7` | Hole | Black + red border |
| `H` | Ladder | Black + yellow stripes |
| `M` | PANICCO (player) | Purple |
| `A` | SLIMER | Blue-purple |
| `B` | EBYRINS | Red-brown |
| `C` | ZAUROID | Green |
| `ｱ` | SLIMER (fall placement) | Deep blue-purple |
| `ｲ` | EBYRINS (fall placement) | Deep red-brown |
| `ｳ` | ZAUROID (fall placement) | Deep green |

**Fall placement** means the enemy starts in mid-air and falls at the beginning of the round.

---

### Keyboard Shortcuts

| Key | Action |
|---|---|
| `Space` | Select Road (eraser) |
| `1` | Select Block |
| `2` | Select Floor |
| `7` | Select Hole |
| `H` | Select Ladder |
| `M` | Select PANICCO |
| `A` | Select SLIMER |
| `B` | Select EBYRINS |
| `C` | Select ZAUROID |
| `Q` | Select SLIMER (fall) — ｱ |
| `W` | Select EBYRINS (fall) — ｲ |
| `E` | Select ZAUROID (fall) — ｳ |
| `Ctrl+Z` | Undo |
| `Ctrl+Y` | Redo |

> Shortcuts are inactive when the cursor is in a text input field.  
> Key hints are shown on the right side of each palette button.

---

### Copying a Round

Use the **📋 Copy to** button and the input field next to it.

1. Navigate to the round you want to copy
2. Enter the destination round number (1–999) in the field next to the button
3. Click **📋 Copy to**
4. A dialog asks whether to move to the destination round

> **Typical use:** Copy an existing map to ROUND 033 or higher, then edit it as a new level.

---

### Loading a File

Click **📂 Load** to load a VMAP\*\*\*.DAT file from disk into the currently selected round.

- Reads CP932 (Shift-JIS) encoding correctly
- Half-width katakana (ｱ / ｲ / ｳ) supported
- The loaded filename is shown in the toolbar

---

### Saving

Click **💾 Save** to download the current round as a VMAP\*\*\*.DAT file.

- Filename is set automatically based on the round number: `VMAP001.DAT` – `VMAP999.DAT`
- If you loaded a file, its original filename is used
- DOS EOF (`0x1A`) is appended to the file
- Line endings are CR+LF (DOS format)

> The file is saved to your browser's download folder.  
> Copy it to your game directory to replace the original.

---

### Clear

Click **🗑 Clear** to reset the current round to all Road (empty) cells.  
A confirmation dialog appears. Row comments are preserved.

---

### Undo / Redo

Click **↺ Undo** / **↻ Redo** in the toolbar, or use `Ctrl+Z` / `Ctrl+Y`.

- Up to **50 steps** of history are kept per session
- History is shared across all rounds
- Undo/Redo history is cleared when the browser is closed
- The Undo button is grayed out when no history is available

---

### Validation Warnings

Warnings appear in a banner directly below the toolbar.  
Saving proceeds even if warnings are present.

| Condition | Warning |
|---|---|
| No `M` on the map | PANICCO is not placed |
| More than one `M` | Multiple PANICCO instances |
| Enemies (A/B/C/ｱ/ｲ/ｳ) total > 16 | Enemy count exceeds the limit of 16 |

---

## Game Reference

### VMAP File Format

```
Rows    : 12 (fixed)
Columns : 13 characters (fixed)
Format  : [13-char map body] [space]; [row number] CR LF
EOF     : DOS EOF byte (0x1A)
Encoding: CP932 (Shift-JIS compatible)
```

### Example Rows

```
 H   M   H  ; 10
2222222222222 ; 11
```

### How to Defeat Enemies

| Enemy | Minimum fall floors |
|---|---|
| SLIMER (A / ｱ) | 1 or more |
| EBYRINS (B / ｲ) | 2 or more |
| ZAUROID (C / ｳ) | 3 or more |

Chain falls, collisions, and burial kills work regardless of fall distance.

### Scoring

| Enemy | Score |
|---|---|
| SLIMER | 100 × floors fallen pts |
| EBYRINS | 200 × floors fallen pts |
| ZAUROID | 300 × floors fallen pts |

---

## Known Limitations

- **Files are saved to the browser's download folder** — direct overwrite is not possible due to browser security
- CP932 characters other than ｱ / ｲ / ｳ (e.g. full-width characters) cannot be saved (not used in the game)
- Edits are lost when the browser is closed — save before closing
- The game reads up to 32 rounds by default. Edit `scene max` in `PANIC.DEF` to enable more

---

## Notes from File Analysis

- VMAP008.DAT row 5 and VMAP013.DAT row 0 contain 14-character body lines (typos in the originals). The editor uses the first 13 characters.
- Half-width katakana used in: VMAP002, 006, 014, 017, 025, 031

---

## Copyright

The game itself is copyright **芸夢 職人 & 基 建吉 (BUGSOFT)**.  
This editor was created for archival and preservation purposes.
