## Running the Game

Space Panicco was originally designed for **NEC PC-9801 series computers running MS-DOS**.

Today the game can be run using a **PC-98 emulator** with either the preserved original disk image or the bundled FreeDOS(98)-based boot disk.

### Recommended emulators

The game has been tested with the following PC-98 emulators:

- Neko Project II
- Neko Project 21/W

### Verified environments

Tested environments include:

- **Neko Project II x64** + **MS-DOS 3.30**
- **Neko Project 21/W x64** + **MS-DOS 6.20**
- **Neko Project II x64** + bundled **FreeDOS(98)-based boot disk**

---

### Method 1 — Original floppy disk image

Use the preserved floppy disk image included in this archive:

```text
original/panic24.hdm
```

Mount the disk image in the emulator and start the game from DOS.

Executable file:

```text
PANIC.EXE
```

---

### Method 2 — Bundled FreeDOS(98)-based boot disk

A bootable floppy disk image using a **FreeDOS(98)-based DOS environment** is also provided:

```text
environment/fd98_2hd_p24.img
```

This disk image is intended to help run the game more easily on modern PC-98 emulators.

The boot environment displays notices for components such as:

- FreeDOS(98) kernel
- FreeDOS XMS-Driver for 80286
- FreeCOM ver 0.85a_DBCS (PC-98)

For license-related notes on the bundled environment, see:

- [FREEDOS98-LICENSE-NOTES.md](FREEDOS98-LICENSE-NOTES.md)

---

### Controls

Movement

```text
8 : Up
2 : Down
4 : Left
6 : Right
```

Actions

```text
X   : Dig a hole
Z   : Fill a hole
ESC : Pause / Config menu
```

The numeric keypad keys **2, 4, 6, 8** correspond to the cursor keys.

---

### Notes

- The game uses the **PC-98 internal BEEP speaker**.
- A joystick is supported but not required.
- Game parameters can be modified using:

```text
PANIC.DEF
```

- For local testing, the bundled boot environment may be adjusted to show a message after `PANIC.EXE` exits. Such convenience edits are not part of the original game itself.

---

### Disclaimer

This repository is published for preservation and research purposes.
No guarantee is made regarding compatibility with every emulator or DOS environment.
