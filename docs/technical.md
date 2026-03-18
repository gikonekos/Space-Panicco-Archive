## Technical Overview

Space Panicco is a PC-98 action game developed in 1994 using a C-based game library environment typical of Japanese hobbyist game development of the early 1990s.

The game architecture separates the executable program from most game resources, allowing data such as maps, graphics, music, and configuration to be modified independently.

### Program Structure

The distributed files form a simple **engine + data architecture**:

PANIC.EXE      Game engine  
PANIC.DEF      Configuration file  
VMAPxxx.DAT    Stage data  
PANIC.D32      Character sprite graphics (32×32)  
MOJI.D16       Font graphics (16×16)  
PANIC.BGM      Background music data  
PANIC.EFS      Sound effect data  

This modular design was relatively uncommon in many small PC-98 hobbyist games of the period, which often embedded stage data directly in the executable.

### Graphics

The game runs in the **PC-98 640×400 16-color graphics mode**.

PC-98 graphics hardware uses a **four-plane VRAM architecture**.  
Space Panicco takes advantage of this structure to manage background graphics and sprites efficiently.

Although the display mode supports 16 colors, the actual visual design uses fewer colors:

- Character sprites use **up to 7 colors plus transparency**
- Background tiles typically use **two colors**

This design improves visibility during fast gameplay while reducing rendering complexity.

Character graphics are stored in:

PANIC.D32

This file contains **32×32 pixel character sprites** used for the player and enemies.

Font graphics and UI characters are stored in:

MOJI.D16

This file contains **16×16 pixel characters** used for text and interface elements.

### Stage Data

Stage layouts are stored in external text-based files:

VMAP001.DAT – VMAP999.DAT

Each stage is defined as a **13 × 12 tile map** using ASCII characters.

Example elements include:

A : SLIMER enemy  
B : EBYRINS enemy  
C : ZAUROID enemy  
M : Player start position  

1 : Diggable block  
2 : Solid (non-diggable) block  
7 : Hole  
H : Ladder  
(space) : Empty path  

Although the distributed game includes **32 stages**, the engine supports up to **99 stages**, configurable through the file `PANIC.DEF`.

### Audio System

Space Panicco uses the **PC-98 internal BEEP speaker** for music and sound effects.

Music data is stored in:

PANIC.BGM

The data is written in an **MML-style format with multiple parts**.  
Since the PC-98 BEEP can only play a single tone at a time, the music driver rapidly alternates between note sequences to simulate **three simultaneous voices using high-speed arpeggiation**.

The main BGM, **"Bottakuri Shouten"**, was originally composed by Motoi Kenkichi on **1994-05-11** using the **PLAY3 three-voice buzzer music driver** on the **SHARP PC-E500 pocket computer**.

This music was later adapted and reused as the main background track in Space Panicco.

Sound effects are stored separately in:

PANIC.EFS

### Gameplay System

Space Panicco follows the lineage of early trap-based arcade games.

Influences include:

- Space Panic (1980) – defeating enemies by dropping them from sufficient height
- Lode Runner (1983) – terrain manipulation through digging

However, the digging mechanics follow the **Space Panic style**, where both digging and filling holes require time.

The game introduces additional mechanics such as:

- Chain Drop – dropping enemies onto other enemies
- Collision Kill – enemies defeating each other on impact
- Bury Kill – filling a hole while an enemy is inside

These mechanics increase the action pace and create additional tactical possibilities.

### Enemy Design

The game features three enemy types:

SLIMER – slime-like creature (1-level fall required)  
EBYRINS – shrimp-like alien (2-level fall required)  
ZAUROID – dinosaur-like android (3-level fall required)

Enemy names and character designs were created by **Motoi Kenkichi**.
