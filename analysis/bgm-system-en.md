# BGM System Analysis: Space Panicco (PC-98, 1994)

This document describes the sound system used in *Space Panicco* based on
binary analysis and documentation comparison.

---

## Overview

[Confirmed]

The sound system of Space Panicco is based on a PC speaker software driver.

The executable contains the following string:

- "BGM Library ver1.12 use TIMER interrupt"

This indicates the use of a timer-driven BGM system.

---

## Components

[Confirmed]

The following components are involved:

- BGM Library ver1.12
- master.lib Version 0.21

Documentation confirms that bgmlib was merged into master.lib starting
from version 0.22. Therefore, version 0.21 represents a pre-integration state.

---

## BGM Data Format

[Confirmed]

The file `PANIC.BGM` is a text-based music data file.

It matches the MML subset described in the bgmlib documentation.

Observed characteristics:

- Musical notes: A–G
- Length specification: numeric (e.g., 4, 8, 16)
- Tempo command: T
- Octave control: O, <, >
- Rest: R
- Part separation: ","
- Multiple tracks (up to 3 parts)
- Track separator: "*"

---

## Sound Effect Format

[Confirmed]

The file `PANIC.EFS` is a text-based sound effect data file.

Observed characteristics:

- Numeric sequences
- Terminated by 0
- Labeled as "effect 1" to "effect 5"

Documentation states:

- Each value represents output frequency
- Data is processed at 4 ms intervals

---

## Playback Model

[Confirmed]

Based on documentation and binary strings:

- Playback is driven by a timer interrupt
- BGM and sound effects share the same output device (PC speaker)
- BGM is defined using MML-like notation
- Sound effects are defined as frequency sequences

---

## API Structure

[Confirmed]

The following API functions are documented in master.man:

- bgm_init
- bgm_read_data
- bgm_read_sdata
- bgm_start_play
- bgm_select_music
- bgm_sound
- bgm_stop_play
- bgm_finish

---

## Data Loading

[Confirmed]

The executable contains references to:

- "panic.bgm"
- "panic.efs"

This indicates external loading of BGM and sound effect data.

---

## Conclusion

[Confirmed]

The sound system of Space Panicco:

- Uses BGM Library ver1.12
- Is integrated with master.lib 0.21
- Uses text-based MML for music
- Uses frequency sequences for sound effects
- Operates via timer interrupt on the PC speaker
