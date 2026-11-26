# GBMicrotest

Austin Appleby's GBMicrotest (MIT, see `LICENSE`): https://github.com/aappleby/gbmicrotest at
463eb6b (2024-04-26), the prebuilt ROMs from its `bin/`. Each test reads one register or address
at one cycle after boot, checked on a DMG (DMG-CPU-08), and leaves its verdict in HRAM: $FF80
what it read, $FF81 what it expected, $FF82 $01 for a pass or $FF for a failure.
`tests/test_gb.cpp` runs them on test_gb only.

Kept: the 482 whose source ends in one of its `test_finish_*`, `test_pass` or `test_fail`
macros. Left out, with no verdict of their own (demos, testbenches, pictures to look at):
000-oam_lock, 000-write_to_x8000, 001-vram_unlocked, 002-vram_locked, 004-tima_boot_phase,
004-tima_cycle_timer, 007-lcd_on_stat, 400-dma, 500-scx-timing, 800-ppu-latch-scx,
801-ppu-latch-scy, 802-ppu-latch-tileselect, 803-ppu-latch-bgdisplay, audio_testbench,
cpu_bus_1, dma_basic, flood_vram, lcdon_write_timing, ly_while_lcd_off, minimal,
mode2_stat_int_to_oam_unlock, oam_sprite_trashing, poweron, ppu_scx_vs_bgp,
ppu_sprite_testbench, ppu_spritex_vs_scx, ppu_win_vs_wx, ppu_wx_early, temp, toggle_lcdc,
wave_write_to_0xC003.
