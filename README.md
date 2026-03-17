# Space Panicco Archive

Historical archive of the PC-98 action game  
**Space Panicco (すぺーす ぱにっ娘)**.

Originally released in **1994**.

This repository preserves the original distributed files, documentation, and disk images of the game for historical and archival purposes.

---

## Screenshots

| Round 1 | Round 2 |
|--------|--------|
| ![Round 1](screenshots/panicco_round01.png) | ![Round 2](screenshots/panicco_round02.png) |
| Neko Project II x64<br>MS-DOS 3.30 | Neko Project 21/W x64<br>MS-DOS 6.20 |

Screenshots showing the game running on two different PC-98 emulator environments.

---

## About the Game

Space Panicco is a **platform action game inspired by Space Panic**.

The player controls the heroine **Panicco**, digs holes in platforms, and defeats aliens by dropping or burying them.

Unlike the original *Space Panic*, this game introduces additional mechanics:

- enemies require different falling heights to defeat
- unbreakable floors allow **bury-kill strategies**
- chain drops and enemy collisions
- editable stage maps
- configurable gameplay parameters

These features make Space Panicco a more strategic evolution of the classic digging-platform formula.

---

## Game Credits

Program  
**Geimu Shokunin (芸夢職人)**

Music & Graphics  
**Motoi Kenkichi (基 建吉)**

Released  
**1994-09-20**

The game was developed under the name **BUGSOFT**, which served both as a circle name and as Motoi Kenkichi's personal handle at the time.

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

## Original Distribution

The original distribution of **Space Panicco v2.4** was archived from:

Vector software library

https://www.vector.co.jp/soft/dos/game/se023653.html

The files included in this repository preserve the original
distribution archive and floppy disk image for historical purposes.

---

## System Requirements

The game was originally developed for the **NEC PC-9800 series** personal computers.

### Original Hardware

- NEC PC-9801 / PC-9821 series
- MS-DOS
- Internal PC speaker (BEEP)
- Floppy disk drive

FM sound hardware is **not required**, as the game uses the internal speaker.

### Emulator

The game can be played on PC-98 emulators such as:

- Neko Project II
- Neko Project 21/W
- T98-Next
- Anex86

Use the included disk image:

```
panic24.hdm
```

### Verified Environments

The following environments were tested for this archive:

| Emulator | DOS Version |
|--------|--------|
| Neko Project II x64 | MS-DOS 3.30 |
| Neko Project 21/W x64 | MS-DOS 6.20 |

### Disk Image Format

The primary floppy disk image preserved in this archive is:

panic24.hdm

D88 format was also tested, but the available converted image showed
compatibility problems in some emulators and mounting tools.

For reliability, the HDM image is therefore used as the preserved
disk image for this archive.

---

## Audio System

The game uses the **PC-98 internal speaker (BEEP)** for music.

Music playback uses a C library developed by **BIO_100%**, which produces pseudo-polyphonic sound using rapid arpeggios on the single-channel PC speaker.

Music data is stored in:

```
PANIC.BGM
```

Main BGM is "Bottakuri Shouten" (ボッタクリショウテン)
composed by Kenkichi Motoi on 1994-05-11.
 
The main BGM **"Bottakuri Shouten"** was originally written using
the **PLAY3 buzzer music driver** for the **SHARP PC-E500** series Pocket computer.
https://github.com/gikonekos/PLAY3-Archive

---

## Stage Data

Stage layouts are stored as text-based map files:

```
VMAP001.DAT – VMAP032.DAT
```

Map size:

```
13 × 12 blocks
```

This design allows stages to be edited manually.

---

## Running the Game

Use the included floppy disk image:

```
panic24.hdm
```

Run the game from DOS:

```
PANIC
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

Motoi Kenkichi  
https://x.com/qptn/

Geimu Shokunin  
https://x.com/k2PSyIqxDKciBXA

You may also open an **Issue** in this repository.

---

## Acknowledgements

Some documentation editing and English text polishing
were assisted by ChatGPT during the archive preparation.

---

## Preservation Note

This repository was created by one of the original authors to preserve the game and its materials for historical purposes.

All original files are kept in their original form whenever possible.
