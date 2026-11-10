# WizeStream development APK — quiet progressive refresh

Debug build 1.39.0 (1039000), application ID `org.wisso.newpipematerial.debug`,
Android 6.0+ (API 23), target API 35. Built from current upstream pipe plus the
quiet progressive-feed correction for issue #1211.

Videos continue arriving progressively, with a single completion banner when
visible new items are available. Repeated row rebinds and refresh-time list
animations have been removed. No thumbnail dimensions or layout preferences changed.

Source: https://github.com/antoninocanta/WizeStream/tree/eb321548afef0945707f9aa9ca176984723a851d
Technical assessment and verification:
https://github.com/antoninocanta/WizeStream/blob/eb321548afef0945707f9aa9ca176984723a851d/doc/silent-progressive-feed.md
License and build instructions are available in the source linked above.

Cloud checks: assembleDebug, lintDebug and all 2,088 JVM tests passed, including
84 feed tests. APK signature, ZIP alignment and 64-bit ELF 16 KB checks passed.
Real-device smoothness, playback and resource use were not measured.

This uses development signing and separate data from the official application.
Its signing certificate matches the previously delivered 1.36.0 debug APK, so it
can update that build while retaining its settings. Allow APK installation from
your browser/file manager. No release was created; this branch hosts the requested
APK only. No new upstream pull request was submitted.

See SHA256SUMS for the artifact digest.
