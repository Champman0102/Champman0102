# CM 01/02 Women 2025 — crash investigation

**v0.1 is known to crash when the user starts an England game. Do not use the old installation ZIP.**

[Download v0.1.2 HISTORY TEST](https://github.com/Champman0102/Champman0102/raw/refs/heads/first-edition-download/delivery/women-v012-history-test.zip)

This is a diagnostic candidate; **Windows new-game success is unverified**.
The reported crash offset `0x126c95` identifies a history-table loop. Native x86
tests reproduce a fault at that instruction when the table is empty/NULL.
This build guards that loop and an adjacent staff-history loop, replacing
31 bytes of setup in place. The user's register state was not captured.

It also corrects the DAT reputation units and adds 20,326 clearly documented
synthetic non-playing staff. These are placeholder female-derived name pairs
and generic attributes, not a real 2025 coaching export. The 45,824 player
identities, CA/PA, birthdays and playing attributes are preserved.

31 tests pass, including the original fault, both empty-table representations
and unchanged populated traversal. A full Windows game test has not run here.
Read README-FIRST.txt and test on a separate complete installation.

Merge Data; do not delete the original Data folder or lose language/game assets.
If the crash persists, the ZIP includes Get-Crash-Log.cmd to collect recent game
error events and basic file checks locally. Send its cm0102-crash.txt for diagnosis.

The old v0.1 file remains in Git history for reproduction. It is not a working release.
