# NBA hw-test

fleroviux's hardware tests for NanoBoyAdvance, the assembled ROMs of those that
measure bus, DMA, timer, IRQ and HALTCNT timing, from https://codeberg.org/nba-emu/hw-test
(BSD-3-Clause, see `LICENSE`; the sources, C and assembly built with devkitARM, are in that
repository). Each prints its cases with libgba's console, `NAME: PASS value` or
`NAME: FAIL value` and what was expected.

- `128kb-boundary.gba`: a sequential cartridge access across a 128 KB page is non-sequential
- `burst-into-tears.gba`, `force-nseq-access.gba`, `latch.gba`, `start-delay.gba`: DMA
- `haltcnt.gba`: HALTCNT, directly and through the BIOS's calls
- `irq-delay.gba`: the cycles from an interrupt to its handler
- `reload.gba`, `start-stop.gba`, `tick-before-reload.gba`: the timers
- `ppu/`, the PPU's: `status-irq-dma.gba` (DISPSTAT's flags, VCOUNT, the PPU's interrupts and
  DMA starts, to the cycle; a menu of four) and `vram-mirror.gba` print their cases;
  `bgpd.gba`, `bgx.gba` (when the affine registers are latched), `dispcnt-latch.gba` (DISPCNT's
  enables a line at a time), `greenswap.gba` and `sprite-hmosaic.gba` draw a picture, which the
  repository has photographed from a GBA (`expected.png`, not kept here);
  `ram-access-timing.gba` shows, as a bitmap, the cycles of a line in which a CPU access to
  VRAM, the palette or OAM waits for the PPU (a research tool: no expected values)

`tests/test_gba.cpp` reads the cases from the screen (`screen_text`) and keeps those that
pass in `tests/gba_expected.txt`, a ratchet; and the pictures' hashes, checked by eye against
the photographs, in `tests/gba_pictures.txt`.
