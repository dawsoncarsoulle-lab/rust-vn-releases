# Installation / Installation

## English

### Linux x86_64

The AppImage requires glibc 2.39 and a working desktop graphics/audio environment. Not every distribution has been tested.

1. Download the AppImage from the official release.
2. Allow execution in file properties, or run `chmod +x rust-VN-Editor-x86_64.AppImage`.
3. Launch `./rust-VN-Editor-x86_64.AppImage`.
4. Without FUSE, use `./rust-VN-Editor-x86_64.AppImage --appimage-extract-and-run`.

The CLI is available with `./rust-VN-Editor-x86_64.AppImage --appimage-extract-and-run --cli --help`. Rust/Cargo is not required to use the packaged editor.

### Windows x86_64 — experimental

Extract the **entire** ZIP into a new directory and run `rust-vn-editor.exe`. Keep the CLI, runtime and resources beside it. Do not run from inside the ZIP.

Windows 10/11 x86_64 is the intended target, not a claim that both have been tested. Check the release notes for actual validation. Packages are unsigned. Never disable antivirus protection; report any blocking warning instead.

### Updates and backups

Keep projects and saves outside the application folder. Save and back up before updating. Downloads from the Updates button require user action; startup checks are optional.

The AppImage installer retains a `.previous` copy. Close the editor before restarting or rolling back. On Windows, extract each update into a **new folder**, never over running executables. Re-export games to include an updated engine.

### Verify downloads

Download `SHA256SUMS.txt` from the **same release**. It lists both packages.

Linux:
```sh
sha256sum --ignore-missing --check SHA256SUMS.txt
```
Your downloaded file must report `OK`.

Windows PowerShell:
```powershell
Get-FileHash .\rust-VN-Editor-windows-x86_64.zip -Algorithm SHA256
```
Compare with the Windows line in `SHA256SUMS.txt`. Hashes verify integrity, not publisher identity.

### Problems

[Report a bug](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/issues/new?template=bug_report.md). Include the version, system, steps and expected/actual result. The editor's CLI log panel shows the preview log path. Windows packages include `windows-diagnostic.ps1`. Review logs for private information before sharing.

## Français

### Linux x86_64

L'AppImage nécessite glibc 2.39 et un environnement graphique/audio fonctionnel. Toutes les distributions ne sont pas validées. Téléchargez le fichier, autorisez son exécution dans les propriétés, puis lancez-le. En terminal :
```sh
chmod +x rust-VN-Editor-x86_64.AppImage
./rust-VN-Editor-x86_64.AppImage
```
Sans FUSE, ajoutez `--appimage-extract-and-run`. Rust/Cargo n'est pas requis pour l'éditeur distribué.

### Windows x86_64 — expérimental

Extrayez **toute** l'archive dans un nouveau dossier puis lancez `rust-vn-editor.exe`. Gardez tous les exécutables et ressources ensemble. Ne lancez pas depuis le ZIP. Windows 10/11 est la cible prévue, pas une affirmation de validation des deux systèmes. Consultez les notes de version. Ne désactivez jamais l'antivirus.

### Mises à jour et vérification

Enregistrez et sauvegardez vos projets, conservés hors du dossier du logiciel. Sous Windows, utilisez un nouveau dossier. L'installateur AppImage garde une copie `.previous` ; fermez l'éditeur avant relance ou retour arrière.

`SHA256SUMS.txt` contient les empreintes **Linux et Windows**. Utilisez les commandes ci-dessus et les fichiers de la même release.

### Aide

[Signalez un problème](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/issues/new?template=bug_report.md) avec version, système, étapes et résultats. Le panneau Journal CLI indique le chemin du journal de l'aperçu. Retirez les informations personnelles avant partage.
