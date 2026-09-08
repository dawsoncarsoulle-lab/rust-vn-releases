# rust-VN Editor 0.2.1 — Linux et Windows x86_64

Première distribution publique de l’éditeur, encore en développement.

## Dans cette version

- Éditeur Blueprint et éditeur visuel des menus.
- Interface de l’éditeur en français et en anglais.
- Moteur, CLI `rvn` et ressources d’export web inclus dans l’AppImage.
- Bouton **Mises à jour** : recherche des versions publiques, téléchargement HTTPS et vérification SHA-256. Vérification au démarrage facultative, désactivée initialement.
- Installation sur confirmation pour les AppImages ; l’ancienne application est conservée à côté avec le suffixe `.previous`. Enregistrez votre travail puis relancez l’application.
- Lien facultatif **Soutenir le projet** vers https://ko-fi.com/rustvn.

## Installation

Téléchargez `rust-VN-Editor-x86_64.AppImage`, rendez-le exécutable puis ouvrez-le.

```sh
chmod +x rust-VN-Editor-x86_64.AppImage
./rust-VN-Editor-x86_64.AppImage
```

Sans FUSE :

```sh
./rust-VN-Editor-x86_64.AppImage --appimage-extract-and-run
```

Le CLI inclus est accessible sans installer Rust :

```sh
./rust-VN-Editor-x86_64.AppImage --appimage-extract-and-run --cli --help
```

## Compatibilité et précautions

- Paquet **Linux x86_64**, construit avec **glibc 2.39**. Vérifié sur Pop!_OS / COSMIC en session Wayland. Ce paquet ne vise pas toutes les distributions Linux.
- Les bibliothèques système de bureau restent nécessaires, notamment OpenSSL 3, X11, Wayland, xkbcommon, ALSA/PulseAudio et les pilotes graphiques. La glibc et les pilotes ne sont pas embarqués.
- **Windows expérimental** : `rust-VN-Editor-windows-x86_64.zip`. Extrayez tout le dossier puis lancez `rust-vn-editor.exe`. Le CLI `rvn.exe`, le moteur `rvn_bevy.exe` et les ressources doivent rester à côté. Cible prévue Windows 10/11 x86_64, Direct3D 11. Exécutables non signés, compilés depuis Linux et non testés nativement sur Windows. Ne désactivez pas votre antivirus. Empreinte séparée dans `SHA256SUMS-windows` ; l’AppImage Linux n’a pas été remplacée.
- Les projets et sauvegardes doivent rester dans un dossier distinct de l’application. Ne les placez pas dans le contenu extrait de l’AppImage.
- Depuis une installation locale antérieure non-AppImage, téléchargez puis lancez cette AppImage séparément. Les mises à jour suivantes pourront remplacer cette AppImage directement.
- Aucune signature de l’éditeur n’est fournie. Vérifiez `SHA256SUMS` et utilisez uniquement ce dépôt officiel.

## Vérifications

58 tests automatisés réussis sous Linux, dont rejet des téléchargements incomplets, des empreintes incorrectes, des liens symboliques et de la modification d’un paquet après téléchargement. Ouverture de l’AppImage, des graphes et du CLI vérifiée sans dépendre du répertoire de développement. Pour Windows : compilation des trois exécutables, inspection de leurs imports DLL et contrôle CRC de toutes les entrées du ZIP. Ces contrôles ne remplacent pas un essai sur Windows.

Cette publication n’est pas une certification de toutes les fonctions du moteur ni de toutes les distributions Linux.
