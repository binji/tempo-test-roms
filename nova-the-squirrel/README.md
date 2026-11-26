# Nova the Squirrel

`nova.nes`: NovaSquirrel's platformer, release v1.0.6a, from
https://github.com/NovaSquirrel/NovaTheSquirrel/releases (the source is in that
repository). MMC1 (mapper 1), 256 KB PRG ROM, 8 KB CHR RAM.

Licenses, from the project's README:
- **Code:** GPL version 3 or later (`LICENSE`).
- **Assets** (graphics, levels, etc.): Creative Commons
  Attribution-NonCommercial-ShareAlike 4.0 International. So the game may not be
  sold without permission. Permission is not granted to use the character and
  design of Nova in anything else.

The header asks for 32 KB of battery-backed work RAM (SXROM), but only the
optional level editor uses more than the first 8 KB. It checks for SXROM and
won't run without it.

`tests/test_mappers.cpp` presses Start, A, A, Down, A, which goes through the title,
the main menu, the level select and the pre-level screen ("Start!") into level
1.
