# 0.2.5 validation — 24 September 2026

Host: Pop!_OS Linux, existing development machine, graphical XWayland session. Not a clean installation.

| Check | Result | Evidence/scope |
| --- | --- | --- |
| Engine workspace release tests | PASS | 333 tests; final CLI notice change additionally rechecked with 30 CLI tests |
| Editor release tests | PASS | 93 tests |
| Packaging gate unit tests | PASS | 5 tests; no claim that release qualification gate is satisfied |
| Linux/Windows/Web compilation | PASS | Release builds from sources identified in release notes |
| Linux launcher and example creation | PASS | Packaged UI, isolated config/recents; example created outside source tree |
| Graph and menu designer display | PASS | Real screenshots in this directory |
| Editor closure | PASS | Own test process exited 0; final remote grab timed out while quitting, earlier captures succeeded |
| CLI starter | PASS | New project, zero check errors/warnings; no test images/audio |
| Desktop/Web generation | PASS | Both starter and editor example exported using packaged CLI |
| Runtime notices in exports | PASS | MIT, prior Apache, DejaVu and dependency notices present |
| Example native playthrough | PASS, limited | Automated French route 0,0,0,0 reached FIN and TitleScreen; process exit 0 |
| Windows ZIP | PASS, static only | CRC, required files, PE executable headers, no personal saves |
| Native Windows | NOT RUN | Requires Windows machine |
| Browsers and clean Ubuntu | NOT RUN | Export generation does not validate browser execution |
| Update rollback/external testers | NOT RUN | No qualification claim |

The final repack changes only CLI source formatting from the UI-tested candidate; editor, resources and native/Web runtimes are unchanged. Final archive checks and CLI export checks are repeated before publication.

SHA-256:

```text
2d7fce8d0c396d3afe9307f45110f37346204039956d2cd40c13b098361cdc4c  rust-VN-Editor-x86_64.AppImage
3d95ceb8cd7fdf82c1bf0851d481d9b84c56fb11834767169991cf8c89f80124  rust-VN-Editor-windows-x86_64.zip
80853e118a07f04b8e230e7b667695fc631d2f3a1b1f29dc98a71632b9ab6d56  MPL-dependency-sources.tar.gz
```
