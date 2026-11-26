# mealybug-tearoom-tests

Mealybug Tearoom Tests by Matt Currie (MIT, see `LICENSE`): tests of the Game Boy PPU's
behavior when its registers change during mode 3, judged by the picture on screen when the
test executes `ld b,b` (at its 10th VBlank).

From https://github.com/mattcurrie/mealybug-tearoom-tests at commit
70e88fb90b59d19dfbb9c3ac36c64105202bb1f4 (2020-12-20): the 24 tests with a DMG expected image.
`<name>.gb` is from the repository's `mealybug-tearoom-tests.zip`; `<name>.txt` is
`expected/DMG-blob/<name>.png` as 144 lines of 160 shades (0 lightest, 3 darkest), made with
`tools/png_shades.py`. `tests/test_gb.cpp` compares the PPU's frame against it. The tests
for the CGB only (the `*2` variants) and `win_without_bg` (no expected image) aren't included.

`<name>-cgbD.txt` is the same test's picture on a CGB-D (in compatibility mode: these are DMG
cartridges), from c-sp's game-boy-test-roms v7.0 (`<name>_cgb_d.png`), as RGB555 colors made with
`tools/png_rgb555.py`; test_gbc compares against it (there are no CGB-E pictures).
