# rust-VN Editor 0.2.1 — Linux x86_64

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
- Aucun paquet Windows n’est livré dans cette release. Le code de téléchargement Windows ne constitue pas une validation native Windows.
- Les projets et sauvegardes doivent rester dans un dossier distinct de l’application. Ne les placez pas dans le contenu extrait de l’AppImage.
- Depuis une installation locale antérieure non-AppImage, téléchargez puis lancez cette AppImage séparément. Les mises à jour suivantes pourront remplacer cette AppImage directement.
- Aucune signature de l’éditeur n’est fournie. Vérifiez `SHA256SUMS` et utilisez uniquement ce dépôt officiel.

## Vérifications

58 tests automatisés réussis, dont rejet des téléchargements incomplets, des empreintes incorrectes, des liens symboliques et de la modification d’un paquet après téléchargement. Ouverture de l’AppImage, des graphes et du CLI vérifiée sans dépendre du répertoire de développement.

Cette publication n’est pas une certification de toutes les fonctions du moteur ni de toutes les distributions Linux.
