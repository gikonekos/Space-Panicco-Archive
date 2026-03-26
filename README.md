# Space Panicco Archive

Historical archive of the PC-98 action game  
**Space Panicco (すぺーす ぱにっ娘)**.

Originally released in **1994**.

This repository was created by one of **the original authors**.

This repository preserves the original distributed files, documentation,
disk images, and related execution environments of the game for historical and archival purposes.

---

## Screenshots

| Round 1 | Round 2 |
|--------|--------|
| ![Round 1](screenshots/panicco_round01.png) | ![Round 2](screenshots/panicco_round02.png) |
| Neko Project II x64<br>MS-DOS 3.30 | Neko Project 21/W x64<br>MS-DOS 6.20 |

Screenshots showing the game running on two different PC-98 emulator environments.

## Gameplay video

YouTube:
https://youtu.be/C4Pq5myM1MM?si=tiAHmLRVQ0kYtJf0

---

## About the Game

Space Panicco is a **platform action game inspired by Space Panic**.

The player digs holes, traps enemies, and clears each round while avoiding attacks.
The game was developed for the **NEC PC-9801 series** and runs under **MS-DOS**.

---

## Game Credits

- Planning, graphics, music: **基 建吉**
- Programming: **芸夢 職人**

---

## Third-Party Components

This program uses or was built with the following third-party software.

### Compiler

- **Borland Turbo C**  
  Copyright (c) 1987–1988 Borland International

### BGM Library

- **BGM Library ver1.12**  
  Copyright (c) 1989–1993 Fumitake Yodo / STUDIO FEMY

### Utility Library

- **master.lib Version 0.21**  
  Copyright (c) 1993 Akihiko Koizuka, Kazumi

### Bundled DOS environment

- **FreeDOS(98)-based DOS environment**  
  A bootable DOS environment is included for PC-98 execution and testing purposes.

  The bundled boot environment displays notices for components such as:

  - **FreeDOS(98) kernel**
    - Copyright 1995–2022 Pasquale J. Villani and The FreeDOS Project
    - Copyright 2001–2022 FreeDOS(98) porting project
    - GNU General Public License, version 2 or later
    - Absolutely no warranty

  - **FreeDOS XMS-Driver for 80286**
    - Copyright 1995 Till Gerken
    - Copyright 2001–2005 Martin Stromberg
    - Copyright 2016 sava

  - **FreeCOM ver 0.85a_DBCS (PC-98)**

All rights to third-party components belong to their respective copyright holders.

For details, see:

- [RIGHTS.md](RIGHTS.md)
- [RIGHTS_ja.md](RIGHTS_ja.md)
- [docs/FREEDOS98-LICENSE-NOTES.md](docs/FREEDOS98-LICENSE-NOTES.md)

---

## Distribution History

This game was originally released in **1994** as Japanese freeware for PC-9801 DOS.

The archived materials in this repository preserve that historical release and related documents.

---

## Internet Archive

A preserved copy is also available at:

- [Internet Archive](https://archive.org/details/space-panicco)

---

## Repository Structure

- `original/` — original distributed archive files and disk images
- `extracted/` — extracted contents from the original archives
- `docs/` — documentation, manuals, license notes, and related notes
- `screenshots/` — screenshots of the game
- `environment/` — emulator and execution environment files and notes
- `analysis/` — preservation-oriented analysis and reverse-engineering notes

---

## Original Distribution

The `original/` directory preserves the original distributed files of **Space Panicco**.

These files are kept for historical and archival purposes.

Contents include:

- original archive packages
- disk images

Extracted files are stored separately in the `extracted/` directory.

Any analysis, modifications, or reorganized materials should be stored outside this directory.

---

## System Requirements

- NEC PC-9801 series compatible environment
- MS-DOS or a compatible PC-98 DOS environment
- floppy disk image or extracted files from the original package

---

## Emulator

The game can be played on PC-98 emulators such as:

- Neko Project II
- Neko Project 21/W

---

## Verified Environments

Confirmed working environments include:

- **Neko Project II x64** with **MS-DOS 3.30**
- **Neko Project 21/W x64** with **MS-DOS 6.20**
- **Neko Project II x64** with the bundled **FreeDOS(98)-based boot disk**

---

## Running the Game

1. Prepare a PC-98 emulator environment.
2. Boot either a preserved DOS image or the bundled FreeDOS(98)-based boot disk.
3. Mount the disk image or open the extracted game files.
4. Run the main executable.

For details, see:

- [Running the Game](docs/Running-the-Game.md)
- [Running the Game (Japanese)](docs/Running-the-Game_ja.md)

---

## Disk Image Format

The archived floppy disk image is preserved in its original format for historical purposes.

Additional convenience images may be included to help run the game in modern emulator environments.

---

## Audio System

The game uses the PC-98 internal speaker (BEEP) for sound during normal gameplay.

Third-party libraries are used for music-related functionality in the original software environment.

---

## Stage Data

Stage graphics and gameplay data are preserved as part of the original game resources.

---

## Documentation

Additional documentation is available in the `docs/` directory.

This includes:

- original manual text
- Japanese notes
- English notes
- running instructions
- FreeDOS(98) license notes

---

## Rights

This repository is a historical archive of the 1994 freeware game *Space Panicco*.

The original game and original distributed materials remain copyrighted by their original rightsholders.
Publication on GitHub does not place the original game under an open-source license.

Personal play, preservation, sharing, and non-commercial use are welcome.
Commercial exploitation or repackaging for profit is not the intended purpose of this archive.

This repository may also include analysis and reverse-engineering notes for preservation and research.
Those materials do not change the copyright status of the original game.

See [RIGHTS.md](RIGHTS.md) and [RIGHTS_ja.md](RIGHTS_ja.md) for details.

---

## Contact

For historical information related to this archive, see the repository owner profile and related archive notes.

---

## Disclaimer

This repository is provided for historical and archival purposes.

No guarantee is made regarding compatibility with modern systems, emulators, DOS environments, or bundled convenience boot images.

---

## Acknowledgements

Thanks to everyone who helped preserve and document historical Japanese PC software.
