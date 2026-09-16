# rust-VN Editor 0.2.3 — Les lettres de l'aube

## Nouvel exemple complet, français et anglais

Le modèle **Projet exemple** inclut désormais *Les lettres de l'aube / Letters at Dawn* : une histoire d'environ 10–15 minutes, quatre décisions, trois dénouements, deux personnages, trois décors, une musique et une galerie. Les menus personnalisés et les graphes sont modifiables. Toutes les ressources sont incluses, avec leurs crédits et licences ; aucun téléchargement supplémentaire n'est nécessaire pour créer l'exemple.

**Projet vide** reste vide. Les projets existants ne sont pas remplacés : créez un nouvel exemple pour découvrir ce contenu.

## Corrections

- Export desktop : cible Windows correctement affichée et exécutable exporté avec son extension `.exe`.
- Éditeur d'interactions des menus : sélection multiple, déplacement, duplication avec conservation des liens internes et navigation améliorés.
- Sauvegardes : nettoyage des anciens sprites avant restauration et arrêt de la musique lorsque la sauvegarde n'en contient pas.
- Personnages : adaptation proportionnelle à la taille de la fenêtre.
- Traduction : dialogues, choix et historique cohérents avec la langue courante après chargement.
- Menus : navigation depuis la galerie, retour au titre et affichage des dialogues corrigés ; galerie native traduite.
- La préférence d'écriture progressive est conservée après rechargement.
- Export Web : correction de la capture de miniature ; crédits et licences conservés dans les exports Web et desktop.
- Fin de récit : traitement des dernières commandes et suppression d'un saut inutile après un saut explicite.

## Installation et mises à jour

- **Linux x86_64** : `rust-VN-Editor-x86_64.AppImage`. Rendez le fichier exécutable. Sans FUSE, lancez-le avec `--appimage-extract-and-run`.
- **Windows x86_64 — expérimental** : `rust-VN-Editor-windows-x86_64.zip`. Extrayez tout le dossier puis ouvrez `rust-vn-editor.exe`.
- Les deux paquets incluent le CLI, le moteur et le runtime d'export Web. Les empreintes figurent dans `SHA256SUMS`.

Le bouton **Mises à jour** des versions précédentes permet de télécharger cette version. Enregistrez votre travail avant de remplacer ou relancer l'application. Conservez vos projets hors de son dossier. Sur Windows, extrayez la nouvelle version dans un nouveau dossier ; ne remplacez pas les exécutables en cours d'utilisation. Une mise à jour AppImage conserve la copie `.previous` pour revenir à la version antérieure.

## Vérifications et limites

Tests automatisés en mode release de l'éditeur et du moteur, dont les 24 parcours de l'exemple dans les deux langues. Des essais visuels et interactifs ont été effectués sous Linux et Chromium/Chrome : fins, langues, sauvegarde/rechargement, galerie, préférences et plusieurs tailles d'écran. Cela ne signifie pas que toutes les branches ont été parcourues manuellement dans chaque navigateur. Firefox n'a pas été validé.

Linux : glibc 2.39 ou ultérieure et bibliothèques système de bureau nécessaires ; pas de garantie pour toutes les distributions.

Windows : cible Windows 10/11 x86_64 avec Direct3D 11. Exécutables cross-compilés et archive contrôlée sous Linux, **pas d'essai natif Windows**. Application non signée ; ne désactivez pas votre antivirus. Les éditions Windows N peuvent nécessiter le Media Feature Pack.

## English

This release adds *Letters at Dawn*, a complete editable French/English example with custom menus, licensed assets and three endings. Empty projects remain empty; existing projects are never overwritten.

Fixes include Windows export naming, menu graph interactions, restored sprites and music, responsive character placement, localized saved dialogue/history, gallery navigation and persistent typewriter settings. Both packages include the CLI, engine and Web runtime.

Automated release tests and Linux/Chromium/Chrome checks were performed. Firefox and native Windows have not been validated; the Windows package remains experimental.

Support the project: https://ko-fi.com/rustvn
