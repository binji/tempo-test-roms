# Object dropout test

undisbeliever's (Marcus Rowe's) SNES hardware test of the objects a line can show (zlib
license, see `LICENSE`), from https://github.com/undisbeliever/snes-test-roms at commit ac6ef80,
`src/hardware-tests/object-dropout-test.asm` (v3, as at d57faf2). `object-dropout-test.sfc` is
that source built with the repository's bass-untech and `tools/write-sfc-checksum.py --lorom`
(sha1 d51c8949...).

It shows one screen of objects, five tests from top to bottom; the results on a Super Famicom
are in the author's post, https://forums.nesdev.org/viewtopic.php?p=292526:

1. 36 objects on a line: past 32, the highest-numbered ones are dropped.
2. Twelve 32 x 32 objects, 48 tiles a line: past 34 tiles, the lowest-numbered objects lose
   theirs first, then the next one its rightmost tiles.
3. The same, flipped: the rightmost tiles on screen are still the ones dropped.
4. 8 objects at X = 256 before 32 on screen: they count toward the 32, so the last 8 drop.
5. 8 large objects on screen and 4 at X = 256 after them: every tile of an object at X = 256
   counts toward the 34 (8 tiles dropped where small and large ones overlap, 6 below).

`test_snes` runs it (the `snes_objects` test, `tests/snes_objects_expected.txt`).
