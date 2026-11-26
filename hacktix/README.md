# Hacktix's Game Boy tests

By Hacktix (Optix, now Ashiepaws), MIT (see `LICENSE-*`), the prebuilt ROMs as c-sp's
game-boy-test-roms v7.0 packs them:

- BullyGB, https://github.com/Ashiepaws/BullyGB at e24fe6f: `bully.gb`
- Strikethrough, https://github.com/Ashiepaws/strikethrough.gb at 7cd01bf: `strikethrough.gb`
- Scribbltests, https://github.com/Ashiepaws/scribbltests at 96dd2f1: `lycscx.gb`, `lycscy.gb`,
  `palettely.gb`, `scxly.gb`, `statcount-auto.gb` (fairylake and winpos have no picture)

`tests/test_gb.cpp` judges each by its picture after a set time (c-sp's howtos: 30 frames,
10 for the scribbltests, 270 for statcount-auto): `<name>-dmg.txt` (shades, tools/png_shades.py)
and `<name>-cgb.txt` (RGB555, tools/png_rgb555.py; compatibility mode), from c-sp's PNGs.
scxly's CGB picture uses a palette that isn't RGB555, so it isn't here. Bully runs with work
RAM as noise (it checks that power-on RAM isn't zeroed).
