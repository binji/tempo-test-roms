# dmg-acid2

dmg-acid2 by Matt Currie (MIT, see `LICENSE`), a test of the Game Boy PPU's rendering:
`dmg-acid2.gb` from release v1.0 of https://github.com/mattcurrie/dmg-acid2, and its reference
image `img/reference-dmg.png`. `reference-dmg.txt` is that image as 144 lines of 160 shades
(0 lightest, 3 darkest), which `tests/test_gb.cpp` compares the PPU's frame against.

`reference-cgb.png` is the picture on a CGB, in compatibility mode with the boot ROM's default
palettes (c-sp's game-boy-test-roms v7.0, `dmg-acid2-cgb.png`); `reference-cgb.txt` is it as
RGB555 colors (`tools/png_rgb555.py`), for test_gbc.
