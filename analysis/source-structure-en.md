# File Structure Analysis: Space Panicco (PC-98, 1994)

This document describes the file-level structure of the Space Panicco
distribution based on analysis of the original archive contents.

---

## Overview

[Confirmed]

The program consists of an executable and multiple external data files.

Observed files:

- PANIC.EXE
- PANIC.BGM
- PANIC.EFS
- PANIC.D32
- PANIC.DEF

---

## Executable

### PANIC.EXE

[Confirmed]

The main executable file.

Contains:

- Program logic
- References to external data files
- Embedded copyright strings

Observed strings include:

- "panic.bgm"
- "panic.efs"
- "panic.d32"
- "panic.def"

---

## Music Data

### PANIC.BGM

[Confirmed]

Text-based music data file.

Characteristics:

- MML-like notation
- Multiple tracks
- Track separator "*"
- Comment lines using ";"

---

## Sound Effect Data

### PANIC.EFS

[Confirmed]

Text-based sound effect data file.

Characteristics:

- Numeric sequences
- Each effect terminated by 0
- Labeled as "effect 1" through "effect 5"

---

## Graphics Data

### PANIC.D32

[Confirmed]

Referenced by the executable.

[Unknown]

- Internal format
- Encoding method
- Resolution or structure

---

## Configuration Data

### PANIC.DEF

[Confirmed]

Referenced by the executable.

[Unknown]

- Exact contents
- Whether it contains configuration, tables, or metadata

---

## File Loading Model

[Confirmed]

The executable references external files by name:

- panic.bgm
- panic.efs
- panic.d32
- panic.def

This indicates a runtime loading model rather than embedded resources.

---

## Error Handling

[Confirmed]

The executable contains error messages:

- "not open = panic.D32 !!"
- "not open = panic.def !!"

This confirms:

- File existence is checked at runtime
- Missing files produce explicit errors

---

## Separation of Concerns

[Confirmed]

The program separates functionality into distinct files:

| Component | File |
|----------|------|
| Program logic | PANIC.EXE |
| Music | PANIC.BGM |
| Sound effects | PANIC.EFS |
| Graphics | PANIC.D32 |
| Configuration | PANIC.DEF |

---

## Conclusion

[Confirmed]

Space Panicco uses a modular file structure in which:

- The executable handles logic and playback control
- External files provide music, sound effects, and other resources
- Resources are loaded at runtime using file-based access
