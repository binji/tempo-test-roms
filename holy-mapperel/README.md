# Holy Mapperel

Damian Yerrick's cartridge board test (zlib license, see `LICENSE`), from
https://github.com/pinobatch/holy-mapperel at commit 4e48b59 ("v0.02-4").

It probes the mapper, then checks that every PRG and CHR bank is reachable
and that CHR RAM holds a pattern, and leaves its findings in zero page.
`tests/test_mappers.cpp` runs these builds:

| File | Board |
|---|---|
| `M0_P32K_C8K_V.nes` | NROM, 8 KB CHR ROM, vertical mirroring |
| `M0_P32K_CR8K_H.nes` | NROM, 8 KB CHR RAM, horizontal |
| `M2_P64K_CR8K_H.nes` | UxROM, 64 KB PRG, horizontal |
| `M2_P128K_CR8K_V.nes` | UxROM, 128 KB PRG, vertical |
| `M2_P256K_CR8K_H.nes` | UxROM (UOROM), 256 KB PRG, horizontal |
| `M3_P32K_C16K_V.nes` | CNROM, 16 KB CHR ROM, vertical |
| `M3_P32K_C32K_H.nes` | CNROM, 32 KB CHR ROM, horizontal |
| `M1_P128K_C128K.nes` | MMC1, 128 KB CHR ROM, no work RAM |
| `M1_P128K_C32K_W8K.nes` | MMC1, 32 KB CHR ROM, 8 KB work RAM |
| `M1_P128K_CR8K.nes` | MMC1 SGROM: CHR RAM, no work RAM |
| `M1_P256K_CR8K_S8K.nes` | MMC1 SNROM: 256 KB PRG, CHR RAM, battery work RAM |
| `M1_P512K_CR8K_S8K.nes` | MMC1 SUROM: 512 KB PRG, CHR RAM, battery work RAM |
| `M4_P32K_C32K.nes` | MMC3, 32 KB PRG, 32 KB CHR ROM, no work RAM |
| `M4_P64K_C64K_S8K.nes` | MMC3, 64 KB PRG, 64 KB CHR ROM, battery work RAM |
| `M4_P128K_CR8K_W8K.nes` | MMC3 TGROM-like: 128 KB PRG, CHR RAM, work RAM |
| `M4_P256K_C256K.nes` | MMC3 TLROM: 256 KB PRG and CHR ROM |
| `M4_P512K_C256K_W8K.nes` | MMC3 TKROM-like: 512 KB PRG, 256 KB CHR ROM, work RAM |
| `M7_P128K_CR8K.nes` | AxROM (ANROM-like): 128 KB PRG, CHR RAM |
| `M7_P256K_CR8K.nes` | AxROM (AOROM): 256 KB PRG, CHR RAM |

Built with cc65 2.19 and Python 3 with Pillow:
`tools/cvt8x5.py` and `tools/pilbmp2nes.py` convert the font, `ca65` assembles
each of `src/*.s`, `ld65 -C nrom256.x` links `mapperel-primary.nes`, and
`make_roms.py`'s `handle_single_rom` makes each board's image from it (the
primary PRG with bank tags in every 4 KB, the header for the board).

The MMC3 and AxROM images were made later, from the program in `M0_P32K_C8K_V.nes`
rather than a rebuild (a cc65 2.19 build from this commit today lays out zero
page differently, and `tests/test_mappers.cpp` reads results at fixed addresses):
its 32 KB of PRG and 8 KB of CHR as `make_roms.py`'s `primary_prgrom` and
`primary_chrrom`, and `handle_single_rom` on each spec in `romspecs_all`.
Each byte of the program that `handle_single_rom` changed in that image, it
overwrites again for every board, so this is exact: made that way, every image
above comes out byte for byte the same.
