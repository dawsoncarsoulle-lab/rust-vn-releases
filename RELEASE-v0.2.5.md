# rust-VN 0.2.5 — public engine and distribution notices

**Public beta, not a stable release. Windows remains experimental.**

## What's new

- The MIT engine is now public: [rust-vn-engine](https://github.com/dawsoncarsoulle-lab/rust-vn-engine). The current editor source remains private.
- Linux and Windows packages are rebuilt against the cleaned public engine. The CLI starter is now text-only, without the old test sprites/music/backgrounds. The full editor example, **Letters at Dawn / Les lettres de l'aube**, remains included.
- New original editor material has separate proprietary terms; prior MIT grants and third-party licenses remain valid. Games may be distributed or sold without rust-VN royalties, subject to applicable component/media licenses.
- Packages include font and dependency notices. Desktop and Web game exports now retain engine, DejaVu and runtime dependency notices automatically.
- Liberation Mono is updated to an OFL-licensed version. Original MPL dependency sources are supplied as an additional download.
- English README, French overview, bilingual installation instructions, credits and real editor screenshots.

## Install

**Linux x86_64:** download `rust-VN-Editor-x86_64.AppImage`, make it executable and launch it.

**Windows x86_64:** extract all of `rust-VN-Editor-windows-x86_64.zip` into a new folder and launch `rust-vn-editor.exe`. Do not overwrite a running application. Do not disable antivirus protection; these packages are unsigned.

Keep projects outside the application folder and back them up before updating. Re-export existing games to include this runtime and its notices. `MPL-dependency-sources.tar.gz` is dependency source code, not an installer; neither are GitHub's automatic source-code archives.

## Checks and limitations

- 333 engine workspace tests, 93 editor tests and five release-gate unit tests passed. The gate unit tests passing does **not** mean full platform qualification passed.
- Linux/Windows desktop and Web runtime builds completed. Windows archive integrity, required files and executable headers checked on Linux; **no native Windows execution of 0.2.5**.
- Linux package smoke checks: launcher, example creation, graph and menu editor display, clean closure, CLI project creation/check, desktop/Web exports and redistribution notices. The exported French example reached an ending with the automated four-choice route and exited successfully.
- Full native Windows validation, clean Ubuntu LTS installation, exhaustive Firefox/Chrome playthroughs, audio listening, update recovery and external-user testing remain pending. Web export generation is not a browser-playthrough test.
- Reports about typewriter behaviour after loading and translation warnings remain under investigation. Maximize the editor when working with project-creation forms on small windows.
- License inventories and source archives improve redistribution notices; no independent legal audit or blanket clearance of user-imported media is claimed.

[Validation record](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/blob/main/validation/20260924-025/RESULTS.md) · [Installation](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/blob/main/INSTALLATION.md) · [Licensing](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/blob/main/LICENSING.md) · [Report a bug](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/issues/new?template=bug_report.md)

## Provenance

- Editor: `78602240c7913d6cf11afa76c1902cca36e245f5` (private repository).
- Engine/CLI: `e0da44b24c4138ef2b202b5082a7769e20f1a2f0` (public repository).
- Web runtime: same runtime sources; subsequent changes in this engine commit concern CLI notice export only.
- Verify downloads with `SHA256SUMS.txt`. Previous 0.2.4 assets are unchanged.

## Français

Bêta publique Linux et Windows expérimental. Le moteur est désormais public sous MIT ; l'éditeur actuel reste privé avec des conditions distinctes. Les anciens médias de test sont retirés du modèle CLI, mais l'exemple complet de l'éditeur est conservé. Les paquets et exports de jeux incluent les notices nécessaires. Vos jeux peuvent être vendus sans redevance rust-VN, sous réserve des licences des composants et médias.

Windows 0.2.5 n'a pas encore été exécuté sur Windows natif. Les validations complètes Web, Ubuntu propre et mises à jour restent à faire. Sauvegardez vos projets, installez dans un dossier neuf et ne désactivez pas l'antivirus.
