# alyosha's GBA tests

alyosha's hardware tests for GBAHawk, from https://github.com/alyosha-tas/gba-tests at
66f5f1d (2026-07-04): a fork of jsmolka's gba-tests (MIT, see `LICENSE`; `README.orig.md` is its
README), with about 120 more tests of what alyosha measured on a console. Only the assembled ROMs
and the folders' readmes are here; the sources (FASMARM) are in that repository, and `unsafe/`
(tests that can lock a console up) is left out.

Each ROM leaves the number of its first failed test in r12, 0 when all passed, and draws it (or
"All tests passed") in mode 4. A few draw a picture to look at instead (`ppu/Sprite_Disable_*`,
`hello`, `shades`, `stripes`). The folders:

- `prefetcher/`: the prefetch buffer when full, at a 0x20000 boundary, and on short branches
- `DMA/`, `Bus/`, `fifo_dma/`, `Interactions/`: DMA timing and what the CPU sees around it, the
  sound FIFOs' DMA, interrupts landing during DMA and internal cycles
- `irq/`, `timer/`, `Serial/`, `timing/`: interrupt latency, IF/IE, HALT's return PC, the timers,
  the serial port's timing, the prefetcher's enable
- `LDM/`, `thumb/`, `arm/`, `psr/`, `memory/`, `ppu/`, `save/`, `bios/`, `nes/`: instructions,
  memory, the PPU's start-up, saves (jsmolka's and alyosha's)

tests/test_gba.cpp runs them as a ratchet (tests/gba_alyosha_expected.txt).
