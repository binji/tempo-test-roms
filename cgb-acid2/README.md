# cgb-acid2

cgb-acid2 by Matt Currie (MIT, see `LICENSE`), a test of the Game Boy Color PPU's rendering:
`cgb-acid2.gbc` from release v1.1 of https://github.com/mattcurrie/cgb-acid2, and its reference
image `img/reference.png`. `reference.txt` is that image as RGB555 colors (a `palette` line, then
144 lines of 160 indexes into it), made by `tools/png_rgb555.py`; `tests/test_gb.cpp` (test_gbc)
compares the PPU's frame against it when the test executes `LD B,B`.
