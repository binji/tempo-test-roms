# mooneye-test-suite

The acceptance tests from mooneye-test-suite by Joonas Javanainen (MIT, see `LICENSE`), as
prebuilt ROMs: release `mts-20260714-0944-31510e1`, from
https://gekkio.fi/files/mooneye-test-suite/. Only `acceptance/` is kept, without the `.sym`
files. `tests/test_gb.cpp` runs them on `examples/gb.tempo`.

`misc/` keeps the tests for a CGB (`boot_regs-cgb`, `boot_hwio-C`, `boot_div-cgbABCDE`,
`bits/unused_hwio-C`, `ppu/vblank_stat_intr-C`), from the same release as c-sp's
game-boy-test-roms v7.0 packs it: DMG cartridges, which test_gbc runs in the CGB's
compatibility mode.
