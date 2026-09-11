# rust-VN Editor 0.2.2 — Correctifs Blueprint

## Corrections

- Les sorties Texte des nœuds SET peuvent alimenter directement un Dialogue.
- Les conversions Nombre → Texte sont acceptées dans les dialogues.
- Les images et sons utilisent le bon chemin de ressources au lancement et à l’export : suppression du doublon `assets/assets`.
- Les noms longs des ressources sont raccourcis visuellement pour ne plus recouvrir les pins.
- Ajouter ou modifier un nœud ne compile plus automatiquement le graphe. Les diagnostics sont produits par Compiler, Valider ou la compilation préalable au lancement et à l’export. Les derniers diagnostics sont conservés jusqu’à une nouvelle vérification.

## Téléchargements

- **Linux x86_64** : `rust-VN-Editor-x86_64.AppImage`. Rendez le fichier exécutable puis lancez-le. Sans FUSE, utilisez `--appimage-extract-and-run`.
- **Windows x86_64 — expérimental** : `rust-VN-Editor-windows-x86_64.zip`. Extrayez tout le dossier puis lancez `rust-vn-editor.exe`.
- Les deux paquets incluent le CLI, le moteur et les ressources d’export web.
- Les empreintes des deux fichiers figurent dans `SHA256SUMS`.

Le bouton **Mises à jour** permet de télécharger cette version depuis la 0.2.1. Enregistrez votre travail avant de remplacer ou relancer l’application. Gardez vos projets hors du dossier de l’application.

## Vérifications et compatibilité

Tests automatisés de l’éditeur et des graphes réussis. Compilation visuelle et rendu du dialogue vérifiés sous Linux sur une copie du projet de reproduction.

Linux : glibc 2.39 ou ultérieure et bibliothèques système de bureau nécessaires ; vérifié sur Pop!_OS / COSMIC Wayland, pas sur toutes les distributions.

Windows : cible Windows 10/11 x86_64 avec Direct3D 11. Version cross-compilée sous Linux ; archive vérifiée, mais aucun essai natif Windows. Application non signée. Ne désactivez pas votre antivirus.

## English

This patch fixes SET text outputs and number-to-text conversions feeding dialogue, duplicated asset paths, long asset titles overlapping pins, and unwanted automatic compilation while editing. Use Compile, Validate, Play or Export to check the graph explicitly.

Linux AppImage and experimental Windows ZIP include the CLI, engine and web export resources. Save your work before updating. Windows binaries are cross-compiled and not tested on native Windows.

Support the project: https://ko-fi.com/rustvn
