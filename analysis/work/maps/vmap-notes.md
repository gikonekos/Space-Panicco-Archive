# VMAP notes

## Confirmed
- VMAP001.DAT - VMAP032.DAT exist in the default game data set.
- VMAP files are text files.
- Each file consists of a 13x12 character grid.
- Each line has a trailing semicolon comment with a row number.
- Observed symbols include: `1`, `2`, `7`, `H`, `A`, `B`, `C`, `M`, `ｱ`, `ｲ`, `ｳ`, and space.
- VMAP files define stage layout data used by the game.
- `A`, `B`, and `C` are enemy placement markers.
- `M` is the Panicco player start marker in normal stage data.
- If `M` is missing, the player can still appear at a default position near the upper-left area.
- On an empty map, Panicco does not fall immediately after appearing.
- On an empty map, Panicco begins to fall only after horizontal movement is made.
- `1` and `2` represent different terrain states and are not interchangeable.
- `7` appears to represent a dug / fillable block state rather than normal empty space.
- Enemy placement requires enough horizontal space for movement.
- Enemies can become stuck if they are placed inside a fully enclosed narrow corridor.
- Enemies can also become stuck after falling into a one-tile-wide enclosed space.
- Such stuck states can make a stage impossible to clear.
- Empty maps can still be loaded by the game, but they do not produce a practically valid stage.
- If stage numbers are skipped and the corresponding VMAP data does not exist, the game may repeat the previous stage layout.
- In that case, enemy initialization may not work correctly, which can make the stage impossible to clear.

## Working interpretation
- `1` likely represents diggable terrain.
- `2` likely represents fixed floor / fill terrain.
- `7` likely represents a dug or refillable terrain state.
- `A`, `B`, and `C` likely correspond to different enemy types.
- `ｱ`, `ｲ`, and `ｳ` likely correspond to fallen or alternate enemy states related to `A`, `B`, and `C`.

## Observed edge cases
- A stage can be structurally valid as text data but still become unwinnable in actual gameplay.
- Enemy placement must be evaluated not only at initial position, but also after falling.
- A one-tile-wide enclosed landing space is enough to trap an enemy and break stage progression.
- Missing or nonstandard stage numbering can lead to partially initialized gameplay state rather than a clean failure.

## Open questions
- What does each symbol map to in PANIC.D32?
- What are the exact differences between `A`, `B`, and `C` in behavior and graphics?
- What are the exact meanings of `ｱ`, `ｲ`, and `ｳ` in runtime behavior?
- How is `7` handled internally during gameplay?
- How are VMAP files selected during gameplay?
- How does the program determine the default Panicco start position when `M` is missing?
- Why does Panicco remain suspended on an empty map until movement occurs?
- Which gameplay checks occur only after movement or state transition rather than immediately on spawn?
