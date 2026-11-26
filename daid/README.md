# daid's Game Boy tests

From GBEmulatorShootout (https://github.com/gbdev/GBEmulatorShootout at 38b926b, MIT, see
`LICENSE`), `testroms/daid`, prebuilt: the CGB's speed switch against DIV, LY and STAT
(`speed_switch_timing_*.gbc`), STOP (`stop_instr.gb`, `stop_instr_gbc_mode3.gb`) and mid-line
BGP writes (`ppu_scanline_bgp.gb`). `tests/test_gb.cpp` judges each by its picture after 30
frames: `<name>-dmg.txt` (shades, tools/png_shades.py) or `<name>-cgb.txt` (RGB555,
tools/png_rgb555.py), from the repository's PNGs. ppu_scanline_bgp on a DMG has three
acceptable pictures (consoles differ), so only its CGB one is here; rom_and_ram has none.
