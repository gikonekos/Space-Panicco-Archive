# Space Panicco V2.4
(Action Game Version)

Program ............ Geimu Shokunin  
Music & Graphics ... Moto Kenkichi  

1994-09-20

---

# 1. Overview

Space Panicco is a **three-dimensional alien trap action game**.

Control the heroine **Panicco**, dig holes, and bury the aliens to defeat them all.

Advanced techniques such as **chain drops** can also be used.

---

# 2. File Contents

```
PANIC.EXE      Game executable
PANIC.D32      Character data (32×32 sprites)
MOJI.D16       Character data (16×16 sprites)
PANIC.DEF      Configuration file
VMAP***.DAT    Map data (001–999)
PANIC.BGM      Background music data
PANIC.EFS      Sound effect data
PANIC.DOC      This manual
```

---

# 3. How to Run

Place all files in the same directory.

Start the game by typing:

```
PANIC
```

Press **Z** or the **joystick Trigger B** at the title screen to begin the game.

---

# 4. How to Play

Control Panicco and defeat all aliens.

## How to Defeat Aliens

Drop enemies into holes and make them fall.

Each enemy requires a minimum falling height to be defeated.

```
SLIMER      ... 1 level or more
EBYRINS     ... 2 levels or more
ZAUROID     ... 3 levels or more
```

However, if a falling enemy collides with another enemy below it,
both enemies are defeated regardless of the height.

If Panicco is caught by an alien or the **OXYGEN** gauge runs out,
one life is lost.

---

# Advanced Techniques

## Chain Drop

Dropping an enemy onto another enemy below can trigger a chain fall.
All enemies involved will be defeated regardless of the falling height.

## Collision

Drop an enemy so that it collides with another enemy.
Both will be destroyed regardless of the falling height.

## Bury Kill

If the ground below is blocked,
you can bury the enemy directly in the hole.

The enemy will be defeated instantly,
regardless of the falling height.

---

# 5. Controls

## During Gameplay

```
Movement

8 : Up
2 : Down
4 : Left
6 : Right
```

```
X / Trigger A : Dig a hole
Z / Trigger B : Fill a hole
```

Joystick control is also supported.

The numeric keypad keys **2,4,6,8** correspond to cursor keys.

---

## Pause Menu

Press **ESC** during the game  
(or press joystick buttons A+B simultaneously).

This opens the **CONFIG menu**.

Use **2 / 8** (or joystick up/down) to select options.  
Press **Z** (or joystick B button) to confirm.

### Menu Options

```
RETURN   : Resume game
DEAD     : Force Panicco to lose one life
QUIT     : Exit to DOS
```

```
SPEED    : Game speed (0–99)
           Lower values make the game faster
           Default: 10
```

```
SOUND    : Enable / Disable sound
```

```
ROUND    : Stage select (001–999)
           Currently only 32 stages exist
```

---

# 6. Scoring

```
SLIMER     : 100 × number of floors fallen
EBYRINS    : 200 × number of floors fallen
ZAUROID    : 300 × number of floors fallen
```

```
BONUS      : Remaining oxygen × 100 points
1UP        : Every 20000 points
```

---

# 7. Configuration File (PANIC.DEF)

Game parameters can be modified by editing this file.

```
(1) Panicco lives        01–09   default: 03
(2) Speed                00–99   default: 10
(3) Starting round       001–099 default: 001
(4) Invincibility        00–01   default: 00
(5) BEEP sound           00–01   default: 01
(6) Maximum round        001–099 default: 032
```

Use half-width characters when editing.

---

# 8. Map Files

```
VMAP001.DAT – VMAP999.DAT
```

These files define stage layouts.

Map size is fixed at:

```
13 × 12 blocks
```

Map characters:

```
A : SLIMER
B : EBYRINS
C : ZAUROID

M : Panicco (player)

1 : Breakable block
2 : Floor (not diggable)
7 : Hole
H : Ladder
Space : Empty path
```

Enemy limit:

```
0 – 16 enemies per stage
```

---

# 9. Copyright

This software is released as **free software**.

Copyright belongs to:

```
Geimu Shokunin
Moto Kenkichi
```

If you redistribute this software on other networks,
please contact one of the authors.

---

# 10. Contact

Comments and feedback are welcome.

Program / Game Design

```
Geimu Shokunin
NIF                HCA01243
Tokyo BBS          FUKU
Pocket Communication Ver.3   #2357
```

Game Design / Graphics / Sound

```
BUGSOFT (Moto Kenkichi)
Tokyo BBS          BUGSOFT
CAT-NET            CAT23779
C&C-NET            BASELUCK
Pocket Communication Ver.3   #2400
```

---

# 11. Final Notes

Our philosophy is:

"A game must be fun to have value."

We carefully refined the gameplay and controls,
so climbing, digging, and filling holes should feel smooth even for beginners.

This version improves the **action gameplay**
and incorporates feedback received from many players.
