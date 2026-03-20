# File References (initial notes)

## Confirmed files in distribution

- PANIC.EXE
- PANIC.DEF
- PANIC.D32
- MOJI.D16
- PANIC.BGM
- PANIC.EFS
- VMAP001.DAT - VMAP005.DAT

## Likely roles

| File        | Role                          |
|------------|-------------------------------|
| PANIC.EXE  | Main program                  |
| PANIC.DEF  | Configuration                 |
| PANIC.D32  | 32x32 graphics patterns       |
| MOJI.D16   | 16x16 font                    |
| PANIC.BGM  | Background music              |
| PANIC.EFS  | Sound effects                 |
| VMAP*.DAT  | Stage / layout data           |

## Open questions

- Where are these files loaded in the executable?
- Is D32 read sequentially or indexed?
- How is VMAP mapped to graphics?
- Are colors defined in EXE or implicit?
