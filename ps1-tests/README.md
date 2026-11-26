ps1-tests by Jakub Czekański (MIT, see LICENSE): https://github.com/JaCzekanski/ps1-tests

The EXEs are from release build-158; each psx.log is the real console's TTY output
from the repository at f727802f (2023-03-05). The console's vram.png pictures are
not copied: tests/psx_pictures.txt holds their hashes (tools/png_hash555.py).

Left out: mdec/movie (1.8 MB each), spu/toolbox (interactive), timer-dump (needs a
console with TCLK0 rewired), mdec/step-by-step-log (its psx.log came from another
build and prints its buffer addresses), and tools/diffvram.
test_psx --suites runs them through the user's BIOS (TEMPO_PSX_BIOS).
