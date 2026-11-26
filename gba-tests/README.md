# GBA Tests

Julian Smolka's gba-tests, the assembled ROMs, from https://github.com/jsmolka/gba-tests
(MIT, see `LICENSE`; the sources, FASMARM assembly, are in that repository). Each ROM runs
many tests and ends with the number of the first that failed in r12 (0: none), drawn on the
screen in mode 4 ("All tests passed").

- `arm.gba`, `thumb.gba`: the instruction sets
- `memory.gba`: the memory map's mirrors, and 8-bit stores to VRAM, the palette and OAM
- `bios.gba`: what the official BIOS leaves on its read-protected bus (needs the user's BIOS)
- `nes.gba`: the code an NES emulator on the GBA runs
- `hello.gba`, `shades.gba`, `stripes.gba`: pictures, checked by eye
- `none.gba`, `sram.gba`, `flash64.gba`, `flash128.gba`: save memory (stage 6)
- `unsafe.gba`: behaviour games shouldn't rely on

`tests/test_gba.cpp` runs arm, thumb, memory, nes and (with TEMPO_GBA_BIOS) bios.
