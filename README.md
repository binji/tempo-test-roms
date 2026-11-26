# Tempo Test ROMs

Freely licensed hardware test ROMs and reference outputs used by [Tempo](https://github.com/binji/tempo), mounted as a git submodule at `tests/roms`.

Each directory keeps its own `LICENSE` file(s) and `README.md` recording the upstream repository, release/commit, and how Tempo runs the suite.

## Suites

### NES

| Directory | Description | License | Upstream |
|---|---|---|---|
| `240p-test-mini/` | Damian Yerrick's NES 240p Test Suite (`240pee.nes`, v0.23) | GPL-2.0+ (source upstream) | https://github.com/pinobatch/240p-test-mini |
| `accuracycoin/` | Chris Siebert's AccuracyCoin NES accuracy suite | MIT | https://github.com/100thCoin/AccuracyCoin |
| `f-ff/` | Pubby's F-FF UxROM racing game (`f-ff_v1.nes`) | MIT | https://github.com/retrobrews/nes-games |
| `holy-mapperel/` | Damian Yerrick's Holy Mapperel mapper tests (v0.02-4) | zlib | https://github.com/pinobatch/holy-mapperel |
| `nova-the-squirrel/` | NovaSquirrel's MMC1 platformer (`nova.nes`, v1.0.6a) | GPL-3.0+ code (source upstream), CC BY-NC-SA 4.0 assets | https://github.com/NovaSquirrel/NovaTheSquirrel |

### Game Boy / Game Boy Color

| Directory | Description | License | Upstream |
|---|---|---|---|
| `age/` | Christoph Sprenger's AGE test ROMs (DMG & CGB) | MIT | https://github.com/c-sp/age-test-roms |
| `cgb-acid2/` | Matt Currie's CGB PPU rendering test (v1.1) | MIT | https://github.com/mattcurrie/cgb-acid2 |
| `cgb-acid-hell/` | Matt Currie's CGB PPU stress test | MIT | https://github.com/mattcurrie/cgb-acid-hell |
| `cpp/` | CasualPokePlayer's MBC3 RTC and RAM gate tests | MIT | https://github.com/CasualPokePlayer/test-roms |
| `daid/` | daid's speed-switch, STOP, and mid-line BGP tests | MIT | https://github.com/gbdev/GBEmulatorShootout |
| `dmg-acid2/` | Matt Currie's DMG/CGB-compat PPU rendering test (v1.0) | MIT | https://github.com/mattcurrie/dmg-acid2 |
| `gbmicrotest/` | Austin Appleby's cycle-level DMG microtests (482 ROMs) | MIT | https://github.com/aappleby/gbmicrotest |
| `hacktix/` | Hacktix's BullyGB, Strikethrough, and Scribbltests | MIT | https://github.com/Ashiepaws/BullyGB (see `README.md`) |
| `mealybug/` | Matt Currie's Mealybug Tearoom mid-mode-3 PPU tests | MIT | https://github.com/mattcurrie/mealybug-tearoom-tests |
| `mooneye/` | Joonas Javanainen's mooneye-test-suite acceptance & CGB misc tests | MIT | https://gekkio.fi/files/mooneye-test-suite/ |
| `samesuite/` | Lior Halphon's SameSuite APU, DMA, PPU, and interrupt tests | X11 | https://github.com/LIJI32/SameSuite |

### Super NES

| Directory | Description | License | Upstream |
|---|---|---|---|
| `snes-object-dropout/` | undisbeliever's SNES object/tile-per-line dropout test | zlib | https://github.com/undisbeliever/snes-test-roms |

### Game Boy Advance

| Directory | Description | License | Upstream |
|---|---|---|---|
| `alyosha-gba-tests/` | alyosha's hardware tests (prefetcher, DMA, bus, IRQ, PPU) | MIT | https://github.com/alyosha-tas/gba-tests |
| `gba-tests/` | Julian Smolka's ARM/Thumb, memory, BIOS, and save tests | MIT | https://github.com/jsmolka/gba-tests |
| `mgba-suite/` | Jeffrey Pfau's mGBA test suite (`suite.gba`) | MIT | https://github.com/mgba-emu/suite |
| `nba-hw-test/` | fleroviux's NanoBoyAdvance bus, DMA, timer, IRQ, and PPU tests | BSD-3-Clause | https://codeberg.org/nba-emu/hw-test |

### Sony PlayStation

| Directory | Description | License | Upstream |
|---|---|---|---|
| `ps1-tests/` | Jakub Czekański's PS1 hardware EXEs and console TTY logs | MIT | https://github.com/JaCzekanski/ps1-tests |

## Playable Demos

Permissively licensed homebrew games bundled into Tempo's browser player (`/play/demos/`). Every entry below has been verified for permissive code and asset licenses (no GPL, no CC-BY-NC, no Kickstart/BIOS requirement).

| Directory | System | Description | License | Upstream |
|---|---|---|---|---|
| `demos/2048-nes/` | NES | 2048 (`2048.nes`) | Unlicense | https://github.com/mmuszkow/2048-nes |
| `demos/adjustris/` | Game Boy | Adjustris (`adjustris.gb`, v1.1) | CC0-1.0 | https://github.com/tbsp/Adjustris |
| `demos/2048-gb/` | Game Boy | 2048 (`2048.gb`, v1.1) | MIT | https://github.com/wyattferguson/2048-gb |
| `demos/labyrinth-of-the-dragon/` | Game Boy Color | Labyrinth of the Dragon (`labyrinth-of-the-dragon.gbc`, v1.0.5a) | MIT | https://github.com/NesHacker/LabyrinthOfTheDragon |
| `demos/gothicvania/` | Super NES | Gothicvania (`gothicvania.sfc`, v1.0.0) | MIT (CC0 art) | https://github.com/donth77/snes-homebrew |
| `demos/miniplanets/` | Genesis | Miniplanets REMIX Ver REV04 (`miniplanets.bin`) | zlib | https://github.com/sikthehedgehog/miniplanets |
| `demos/battle-4tris/` | Genesis | Battle 4Tris (`battle-4tris.bin`, build-9) | MIT | https://github.com/monteslu/retro-homebrew-games |
| `demos/hexes/` | Game Boy Advance | HEXES (`hexes.gba`, v0.1.1-gbajam22) | MIT | https://github.com/EigenlightArts/HEXES |
