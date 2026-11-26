# SameSuite

Lior Halphon's SameSuite (X11 license, see `LICENSE`): https://github.com/LIJI32/SameSuite,
prebuilt as in the game-boy-test-roms v7.0 release (https://github.com/c-sp/game-boy-test-roms):
its APU, DMA, PPU and interrupt tests (not the SGB ones). Each ends in `LD B,B` with B, C, D,
E, H, L = 3, 5, 8, 13, 21, 34 for a pass. `tests/test_gb.cpp` runs those made for a CGB
(header $143 bit 7) as test_gbc, and the rest as test_gb. They are written for a CGB-E.
