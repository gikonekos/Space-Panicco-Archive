## Running the Game

Space Panicco was originally designed for **NEC PC-9801 series computers running MS-DOS**.

Today the game can be run easily using a **PC-98 emulator**.

### Recommended Emulator

The game has been tested with the following PC-98 emulators:

- Neko Project II
- Neko Project 21/W

These emulators accurately reproduce the PC-98 hardware environment.

---

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

---

### Method 2 — FreeDOS Boot Disk

A bootable floppy disk image using **FreeDOS(98)** is also provided:

```
fd98_2hd_p24.img
```

This disk image automatically starts **Space Panicco** after boot.

FreeDOS(98) information:

https://bauxite.sakura.ne.jp/software/dos/freedos.htm

Example emulator setup:

https://simk98.github.io/np21w/freedos98.html

---

### Controls

Movement

```
8 : Up
2 : Down
4 : Left
6 : Right
```

Actions

```
X : Dig a hole
Z : Fill a hole
ESC : Pause / Config menu
```

The numeric keypad keys **2,4,6,8** correspond to the cursor keys.

---

### Notes

- The game uses the **PC-98 internal BEEP speaker**.
- A joystick is supported but not required.
- Game parameters can be modified using the configuration file:

```
PANIC.DEF
```

---

### Compatibility

Tested environments:

```
Neko Project II x64   + MS-DOS 3.30
Neko Project 21/W x64 + MS-DOS 6.20
```

The game also runs using **FreeDOS(98)** with the provided boot disk image.
