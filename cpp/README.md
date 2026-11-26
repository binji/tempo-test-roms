# CasualPokePlayer's test ROMs

From https://github.com/CasualPokePlayer/test-roms (MIT, see `LICENSE`; at 4a04706), as
GBEmulatorShootout (38b926b) builds them in `testroms/cpp`: MBC3's clock and RAM gate
(`latch-rtc-test.gb`, `rtc-invalid-banks-test.gb`, `ramg-mbc3-test.gb`). `tests/test_gb.cpp`
judges each by its picture after 30 frames: `<name>-dmg.txt` (shades, tools/png_shades.py)
and `<name>-cgb.txt` (RGB555, tools/png_rgb555.py; compatibility mode), from GBEmulatorShootout's
PNGs. The SGB test isn't here.
