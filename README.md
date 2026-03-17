# Space Panicco Archive

Historical archive of the PC-98 action game  
**Space Panicco (すぺーす ぱにっ娘)**.

Originally released in **1994**.

This repository preserves the original distributed files,
documentation, and disk images of the game for historical
and archival purposes.

---
## Screenshots

| Round 1 | Round 2 |
|--------|--------|
| ![Round 1](screenshots/panicco_round01.png) | ![Round 2](screenshots/panicco_round02.png) |
| Neko Project II x64<br>MS-DOS 3.30 | Neko Project 21/W x64<br>MS-DOS 6.20 |

Screenshots showing the game running on two different PC-98 emulator environments.

## About the Game

Space Panicco is a **platform action game inspired by Space Panic**.

The player controls **Panicco**, digs holes in platforms, and defeats
aliens by dropping or burying them.

Unlike the original Space Panic, the game introduces additional mechanics:

- enemies require different falling heights to defeat
- unbreakable floors allow **bury-kill strategies**
- chain drops and enemy collisions
- editable stage maps
- configurable gameplay parameters

These features make Space Panicco a more strategic evolution
of the classic digging-platform formula.

---

## Game Credits

Program  
**Geimu Shokunin (芸夢職人)**

Music & Graphics  
**Moto Kenkichi (基 健吉)**

Released  
**1994-09-20**

---

## Repository Structure

```
Space-Panicco-Archive

original/
    panic24.zip      Original distribution archive
    panic24.hdm      Floppy disk image

extracted/
    Extracted original files from the archive

docs/
    original_manual.md   Original Japanese documentation
    manual_en.md         English translation of the manual
```

---

## Audio System

The game uses the **PC-98 internal speaker (BEEP)** for music.

Music playback uses a C library developed by **BIO_100%**,
which produces pseudo-polyphonic sound using rapid arpeggios
on the single-channel PC speaker.

Music data is stored in:

```
PANIC.BGM
```

---

## Stage Data

Stage layouts are stored as text-based map files:

```
VMAP001.DAT – VMAPxxx.DAT
```

Map size:

```
13 × 12 blocks
```

This design allows stages to be edited manually.

---

## Running the Game

The game runs on **NEC PC-9801 / PC-9821** compatible systems.

You can play it using PC-98 emulators such as:

- Neko Project II
- T98-Next
- Anex86

Use the provided floppy disk image:

```
panic24.hdm
```

---

## Documentation

Original documentation and translation are available in:

```
docs/original_manual.md
docs/manual_en.md
```

---

## Contact

For questions or historical information about the game:

Moto Kenkichi  
https://x.com/qptn/

Geimu Shokunin  
https://x.com/k2PSyIqxDKciBXA

You may also open an **Issue** in this repository.

---

## Preservation Note

This repository was created by one of the original authors
to preserve the game and its materials for historical purposes.

All original files are kept in their original form whenever possible.
