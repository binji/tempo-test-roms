# AGE test roms

From Christoph Sprenger's AGE test roms (MIT, see `LICENSE`):
https://github.com/c-sp/age-test-roms at 1f5bc10, prebuilt as in the game-boy-test-roms v7.0
release (https://github.com/c-sp/game-boy-test-roms). The tests for a CGB-E in CGB mode (names
with `cgbE`, `cgbBCE`), for one in compatibility mode (`ncmE`, `ncmBCE`: DMG cartridges) and
for a DMG (`dmgC`) are here: `tests/test_gb.cpp` runs each until it executes `LD B,B`, test_gbc those for the CGB,
test_gb those for the DMG, and passes it if B, C, D, E, H, L = 3, 5, 8, 13, 21, 34. A screenshot
test (no model in its name) is judged by the picture then: `<name>-cgbBCE.txt` (RGB555 colors,
`tools/png_rgb555.py`; for a DMG cartridge `-ncmBCE.txt` or `-ncmE.txt`, compatibility mode's)
or `<name>-dmgC.txt` (shades, `tools/png_shades.py`), from the release's
PNGs.
`caution/` ends the halt after the switch early with an interrupt, which Nintendo's manual
warns against (`WARNING.md`).
