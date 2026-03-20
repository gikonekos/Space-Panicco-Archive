# Licensing Investigation: Space Panicco (PC-98, 1994)

This document summarizes the investigation into third-party libraries
used in *Space Panicco* and the clarification of licensing attribution.

---

## Background

During the public release of this archive project, it was pointed out that
the original license attribution in the documentation was insufficient.

This issue was raised by one of the original authors of master.lib:

- Akihiko Koizuka (戀塚昭彦)

This feedback triggered a detailed investigation into the actual components
used in the original executable.

---

## Trigger

[Testimony]

A public comment by Akihiko Koizuka indicated:

> "License attribution is insufficient"

This statement is treated as an important primary testimony from a
direct contributor to the original ecosystem (master.lib author).

---

## Investigation Method

[Confirmed]

The following sources were used:

- Original binary: `PANIC.EXE`
- Data files: `PANIC.BGM`, `PANIC.EFS`
- Documentation: `master.man`, `BGM / EFS manual`
- Related library documentation (`master.lib`, bgmlib)

Analysis included:

- String extraction from binary
- Format comparison with documented specifications
- API structure verification via manuals

---

## Findings

### 1. Compiler

[Confirmed]

Strings found in the executable:

- "Turbo-C - Copyright (c) 1988 Borland Intl."
- "Copyright (c) 1987,1988 Borland International"

Conclusion:

- The program was built using **Borland Turbo C**

---

### 2. BGM Library

[Confirmed]

Strings found in the executable:

- "BGM Library ver1.12 use TIMER interrupt"
- "Copyright(C)1989-93 Fumitake Yodo and studiofemy"

Conclusion:

- The program uses **BGM Library ver1.12**
- Author: Fumitake Yodo / STUDIO FEMY

---

### 3. master.lib

[Confirmed]

Strings found in the executable:

- "MASTERM.LIB Version 0.21"
- "Copyright (c)1993 A.Koizuka,Kazumi"

Documentation confirms:

- master.lib 0.21 (pre-integration version)
- bgmlib was merged into master.lib starting from version 0.22

Conclusion:

- Space Panicco uses **master.lib 0.21 (before integration)**

---

### 4. BGM / EFS System

[Confirmed]

- `PANIC.BGM` matches bgmlib MML subset format
- `PANIC.EFS` matches bgmlib EFS format (frequency sequence, 4ms step)

Documentation match:

- "BGM / EFS manual (based on bgmlib.man)"

Conclusion:

- The sound system is consistent with **bgmlib specification**

---

## Attribution Issue

[Confirmed]

- The original executable contains copyright strings
- However, these were not clearly reflected in modern documentation

[Testimony]

- The insufficiency of license attribution was explicitly pointed out
  by Akihiko Koizuka

---

## Resolution

[Confirmed]

Based on this investigation:

- Third-party components have been identified
- Attribution has been restored in the README

The following components are now explicitly credited:

- Borland Turbo C
- BGM Library ver1.12 (Fumitake Yodo / STUDIO FEMY)
- master.lib 0.21 (Akihiko Koizuka, Kazumi)

---

## Notes on Certainty

- All technical findings are based on binary evidence and documentation
- Testimony is clearly separated and not treated as sole evidence
- No assumptions are made beyond verifiable data

---

## Conclusion

This investigation confirms that Space Panicco depends on multiple
third-party components, and that proper attribution is necessary.

The issue raised by Akihiko Koizuka directly led to the identification
and correction of incomplete licensing documentation.
