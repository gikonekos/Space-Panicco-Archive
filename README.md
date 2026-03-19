# Space Panicco Archive

Historical archive of the PC-98 action game  
**Space Panicco (すぺーす ぱにっ娘)**.

Originally released in **1994**.

This repository was created by one of **the original authors**.

This repository preserves the original distributed files, documentation,
and disk images of the game for historical and archival purposes.

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

The title is a play on the arcade game *Space Panic*.  
The heroine of the game is named **Panicco (ぱにっ娘)**.

The player controls the heroine **Panicco**, digs holes in platforms,
and defeats aliens by dropping or burying them.

Unlike the original *Space Panic*, this game introduces additional mechanics:

- enemies require different falling heights to defeat
- unbreakable floors allow **bury-kill strategies**
- chain drops and enemy collisions
- editable stage maps
- configurable gameplay parameters

These features make Space Panicco a more strategic evolution of
the classic digging-platform formula.

---

## Game Credits

Program  
**Geimu Shokunin (芸夢職人)**

Music & Graphics  
**Motoi Kenkichi (基 建吉)**

Released  
**1994-09-20**

The game was developed by the Japanese doujin software circle  
**BUGSOFT**.

---

## Distribution History

Space Panicco was originally distributed in **1994** through Japanese
hobbyist software channels.

The game was first distributed on floppy disks at events such as
**Comiket (Comic Market)**, packaged with a printed instruction sheet.

Later versions were distributed online through the **Vector software
library**, a major Japanese freeware and shareware distribution site.

Vector also produced CD-ROM compilations of its software archive,
which were distributed to registered authors at the time.

Today the game is preserved here on **GitHub (2026)** as part of a
historical archive project documenting PC-98 software and Japanese
doujin game culture.

---

## Repository Structure

```
Space-Panicco-Archive

original/
    panic24.zip          Original distribution archive
    panic24.hdm          Floppy disk image
    fd98_2hd_p24.img     Bootable FreeDOS(98) floppy image

extracted/
    Extracted original files from the archive

docs/
    original_manual.md   Original Japanese documentation
    manual_en.md         English translation of the manual

screenshots/
    Emulator screenshots
```

---

## Original Distribution

The original distribution of **Space Panicco v2.4** was archived from:

Vector software library

https://www.vector.co.jp/soft/dos/game/se023653.html

The files included in this repository preserve the original
distribution archive and floppy disk image for historical purposes.

Additional disk images may be provided for convenience to help run the
software in modern emulator environments.

---

## System Requirements

The game was originally developed for the **NEC PC-9800 series**
personal computers.

### Original Hardware

- NEC PC-9801 / PC-9821 series
- MS-DOS
- Internal PC speaker (BEEP)
- Floppy disk drive

FM sound hardware is **not required**, as the game uses the internal
speaker.

---

## Running the Game

Space Panicco was originally designed for **NEC PC-9801 series computers running MS-DOS**.

Today the game can be run on modern systems using **PC-98 emulators**.

### Emulator

The game works with common PC-98 emulators such as:

- Neko Project II
- Neko Project 21/W
- T98-Next
- Anex86

### Method 1 — Floppy Disk Image

Use the preserved floppy disk image included in this archive:

```
panic24.hdm
```

Mount the disk image in the emulator and start the game from DOS:

```
PANIC
```

Executable file:

```
PANIC.EXE
```

### Method 2 — FreeDOS Boot Disk

A bootable floppy disk image using **FreeDOS(98)** is also provided:

```
fd98_2hd_p24.img
```

This disk image automatically starts **Space Panicco** after boot,
so no DOS setup is required.

FreeDOS(98) information:

https://bauxite.sakura.ne.jp/software/dos/freedos.htm

Example emulator setup:

https://simk98.github.io/np21w/freedos98.html

---

## Verified Environments

The following environments were tested for this archive:

| Emulator | DOS Version |
|--------|--------|
| Neko Project II x64 | MS-DOS 3.30 |
| Neko Project 21/W x64 | MS-DOS 6.20 |

---

## Controls

Movement

```
8 : Up
2 : Down
4 : Left
6 : Right
```

Actions

```
X   : Dig a hole
Z   : Fill a hole
ESC : Pause / Config menu
```

The numeric keypad keys **2,4,6,8** correspond to the cursor keys.

---

## Notes

- The game uses the **PC-98 internal BEEP speaker**.
- A joystick is supported but not required.
- Game parameters can be modified using the configuration file:

```
PANIC.DEF
```

---

## Disk Image Format

The primary floppy disk image preserved in this archive is:

```
panic24.hdm
```

D88 format was also tested, but the available converted image showed
compatibility problems in some emulators and mounting tools.

For reliability, the HDM image is therefore used as the preserved
disk image for this archive.

---

## Audio System

The game uses the **PC-98 internal speaker (BEEP)** for music.

Music playback uses a C library developed by **BIO_100%**, which
produces pseudo-polyphonic sound using rapid arpeggios on the
single-channel PC speaker.

Music data is stored in:

```
PANIC.BGM
```

The main BGM **"Bottakuri Shouten" (ボッタクリショウテン)**  
was composed by Kenkichi Motoi on **1994-05-11**.

This music was originally written using the **PLAY3 buzzer music
driver** for the **SHARP PC-E500** pocket computer.

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

This repository was created by one of the original authors
to preserve the game and its materials for historical purposes.

All original files are kept in their original form whenever possible.

---

## Disclaimer

This repository is provided for **historical and archival purposes**.

The software is preserved as originally distributed whenever possible.

No guarantee is made regarding compatibility with modern systems,
emulators, or DOS environments.
