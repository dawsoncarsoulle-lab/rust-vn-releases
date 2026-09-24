# rust-VN Editor

Create visual novels with visual story graphs and customizable game menus.

**Public beta — not a stable release.**

[Download](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/releases/latest) · [Installation](INSTALLATION.md) · [Français](README.fr.md) · [Report a bug](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/issues/new?template=bug_report.md) · [Support](https://ko-fi.com/rustvn)

## Create, preview, export

- Organize dialogue, choices, conditions and scenes in visual graphs.
- Add characters, backgrounds, music and sound effects.
- Design game menus and their interactions.
- Compile, inspect diagnostics and preview your story.
- Export desktop games and Web builds.

**Les lettres de l'aube / Letters at Dawn** is an included French/English example with three endings and custom menus. Choose **Example project** to explore it. **Empty project** stays empty.

## Screenshots

![Story graph editor](assets/blueprints.png)
![Project launcher](assets/accueil.png)
![Menu designer](assets/interface.png)

Real Linux captures taken on 24 September 2026 with the 0.2.5 development build, not concept art. The graph is a simplified demonstration assembled from the example; the menu is the included French example with the editor UI set to English. The `remote` suffix identifies the isolated capture instance. Version 0.2.5 is still in preparation; these images are not a claim that it has been published.

## Downloads and validation

Linux x86_64 AppImage and experimental Windows x86_64 portable ZIP are available from [Releases](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/releases). Do not download GitHub's automatic **Source code** archives to install the editor: they contain this documentation repository.

The **Latest** label identifies the distributed version, not a guarantee of stability. Read the exact release's notes before installing.

Known gaps include native Windows retesting of the latest package, a separate clean Ubuntu LTS installation, complete Firefox/Web coverage, current-version update recovery and external-user testing. Typewriter behaviour after loading and translation warnings reported on Windows remain under investigation. No complete listening check of all audio is claimed.

**Save regularly. Keep projects outside the application directory and back up important projects before updating.** Existing exported games keep their runtime until you export again. Packages are unsigned: never disable antivirus protection to run them.

## Licensing

The engine and the editor have different licenses. See [licensing and game distribution](LICENSING.md). Example media retain their own licenses and attribution requirements. You retain ownership of your original stories and assets.

## Feedback

[Open an issue](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/issues/new?template=bug_report.md) with the version, OS, reproduction steps and expected/actual results. Include your browser for Web problems. Remove personal information from screenshots and logs; only share projects you have permission to disclose. A GitHub account is required.

## Support

[Ko-fi](https://ko-fi.com/rustvn) contributions are optional support for development, not payment for a promised feature, delivery date or unlimited support. Reproducible bug reports and usability feedback also help.
