# CM 01/02 Women 2025 — downloads paused

Downloads are paused as of 30 October 2026. Windows Defender reported an active
`Behavior:Win32/DefenseEvasion.A!ml` detection naming the user's `cm0102.exe`
during crash-capture troubleshooting. This has not been established as a false
positive. Keep the flagged copy quarantined and leave Defender enabled.

The published game ZIPs have been removed from the current download branch
while the alert is investigated. The original uploads and local build artifacts
are preserved for analysis. No executable or database replacement is released
with this notice.

A static comparison reproduces the v0.1.2 EXE exactly from the user-supplied
no-CD-patched input: 177 differing bytes, all within 143 calendar/title patch
regions and two history-loop patches. Imports, entry point and section headers
are unchanged. This checks patch provenance; it does not establish the safety
of the supplied original or explain the behavioral alert.

The project is also investigating failed England new-game creation. Neither
v0.1 nor v0.1.2 is a gameplay-verified working release.
