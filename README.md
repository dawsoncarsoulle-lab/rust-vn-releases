<div align="center">

# rust-VN Editor

### Vos histoires prennent forme.

Un éditeur visuel pour créer des visual novels, composer leur interface et préparer leur distribution.

[![Distributions](https://img.shields.io/badge/distribution-officielle-087EA4?style=flat-square)](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/releases)
[![Statut](https://img.shields.io/badge/statut-premi%C3%A8re%20publication%20en%20pr%C3%A9paration-555555?style=flat-square)](#télécharger)

[Télécharger](#télécharger) · [Installer](#installation) · [Mises à jour](#mises-à-jour) · [Vérifier un fichier](#intégrité-des-téléchargements)

</div>

---

![Éditeur Blueprint de rust-VN : un premier dialogue relié à l’entrée du graphe.](assets/blueprints.png)

<p align="center"><em>Une histoire lisible sous forme de nœuds : point de départ, personnage et dialogue.</em></p>

## Créer, personnaliser, partager

rust-VN Editor réunit la création narrative et la composition d’interface dans un même environnement. Les graphes Blueprint permettent d’organiser les dialogues, les choix et les branches de l’histoire ; l’éditeur visuel d’interface permet de travailler sur les menus et leur présentation.

Le projet s’adresse aussi bien aux auteurs qui préfèrent une approche visuelle qu’aux utilisateurs souhaitant travailler sur des scripts RVN dans leur éditeur de code.

| Espace de création | Usage |
| :--- | :--- |
| **Histoire** | Organiser les graphes et les chapitres, relier les dialogues, les choix et les conditions. |
| **Mise en scène** | Utiliser les personnages, sprites, décors, musiques, sons et transitions du projet. |
| **Interface** | Composer les menus, personnaliser leur apparence et définir leurs interactions. |
| **Vérification** | Compiler les graphes, consulter les diagnostics et lancer le jeu depuis l’éditeur. |
| **Distribution** | Préparer une version du jeu à partager, selon les cibles disponibles dans la version installée. |

> L’application est en développement. Les notes de chaque version précisent les fonctionnalités livrées, les plateformes vérifiées et les limites connues. Elles font référence pour le paquet téléchargé.

## L’éditeur en images

### Un point de départ pour chaque histoire

L’accueil rassemble l’ouverture des projets et la création d’une nouvelle histoire.

![Accueil de rust-VN Editor avec les commandes Nouveau projet, Mes projets et Ouvrir.](assets/accueil.png)

### Une interface à composer visuellement

Le mode Design présente la page du jeu au centre, ses pages à gauche et les propriétés de présentation à droite. Ici, un menu principal simple utilise le thème Science-fiction.

![Mode Design : composition du menu principal et inspecteur des styles.](assets/interface.png)

<sub>Captures réelles de l’application de développement, réalisées sur un projet de test. Le suffixe « remote » identifie l’instance de capture. Les images ne sont pas des maquettes et peuvent différer des prochaines versions.</sub>

## Télécharger

**La première distribution publique est en préparation. Aucun installateur n’est encore disponible dans ce dépôt.**

Les fichiers validés seront publiés exclusivement dans les [Releases GitHub](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/releases).

| Plateforme prévue | Format | Nom du téléchargement |
| :--- | :--- | :--- |
| Linux x86_64 | Application portable | `rust-VN-Editor-x86_64.AppImage` |
| Windows x86_64 | Archive à extraire | `rust-VN-Editor-windows-x86_64.zip` |

Chaque publication indiquera sa configuration minimale et son niveau de validation. Une AppImage ne garantit pas la compatibilité avec toutes les distributions Linux ; un exécutable Windows compilé n’est pas nécessairement validé sur une machine Windows.

**Ne téléchargez pas « Source code (zip) » pour installer l’application.** Les archives de code proposées automatiquement par GitHub contiennent les fichiers de ce dépôt, pas l’éditeur.

## Installation

Les instructions suivantes s’appliqueront lorsque les paquets seront disponibles.

### Linux · AppImage

1. Téléchargez l’AppImage depuis une release et consultez ses prérequis.
2. Placez-la dans un dossier où vous souhaitez conserver l’application.
3. Dans les propriétés du fichier, autorisez son exécution comme programme.
4. Ouvrez le fichier pour lancer l’éditeur.

Vous pouvez également utiliser un terminal depuis le dossier du téléchargement :

```sh
chmod +x rust-VN-Editor-x86_64.AppImage
./rust-VN-Editor-x86_64.AppImage
```

La prise en charge de FUSE ou d’un lancement sans FUSE sera précisée dans les notes de distribution.

### Windows · Archive portable

1. Téléchargez l’archive Windows depuis une release.
2. Extrayez **tout son contenu** dans un dossier dédié.
3. Lancez `rust-vn-editor.exe` depuis ce dossier.

Conservez les ressources et les autres exécutables à côté de l’éditeur : déplacer uniquement le fichier `.exe` peut empêcher le fonctionnement de l’application. La signature éventuelle du paquet et les versions de Windows testées seront indiquées dans les notes de release.

## Mises à jour

Ce dépôt est le canal public prévu pour les mises à jour de rust-VN Editor. Il permet de distribuer l’application sans donner accès aux dépôts de développement et sans demander un compte GitHub aux utilisateurs.

Le mécanisme intégré est en préparation. Il est conçu pour :

- rechercher les nouvelles versions stables publiées ici ;
- proposer un téléchargement correspondant à la plateforme ;
- vérifier l’intégrité du fichier avant son utilisation ;
- laisser l’utilisateur décider du téléchargement et de l’installation.

**L’intégration sera annoncée dans les notes de la première version qui la contient.** En attendant, vous pourrez télécharger les versions manuellement depuis les Releases. Les anciennes publications resteront consultables pour identifier les changements et retrouver les fichiers disponibles.

Gardez vos projets et sauvegardes dans un dossier distinct de celui de l’application. Avant un changement de version, enregistrez votre travail et conservez une copie de vos projets importants.

## Intégrité des téléchargements

Les distributions seront accompagnées d’un fichier `SHA256SUMS`. Il permet de vérifier que le fichier téléchargé correspond à celui de la publication.

### Linux

Depuis le dossier contenant l’AppImage et `SHA256SUMS` :

```sh
sha256sum --ignore-missing --check SHA256SUMS
```

Vérifiez que le nom de votre AppImage apparaît avec le résultat `OK`.

### Windows · PowerShell

```powershell
Get-FileHash .\rust-VN-Editor-windows-x86_64.zip -Algorithm SHA256
```

Comparez l’empreinte affichée avec la ligne correspondante dans `SHA256SUMS`.

Une empreinte vérifie l’intégrité ; elle ne remplace pas une signature d’éditeur. Utilisez toujours les fichiers et les empreintes de la même publication officielle.

## À propos de ce dépôt

Ce dépôt est réservé à la **distribution publique** : documentation d’installation, notes de version et fichiers téléchargeables. Il ne contient ni les projets personnels des utilisateurs, ni leurs sauvegardes, ni les dépôts de développement de l’éditeur et du moteur.

Les fichiers de licence et les mentions des composants tiers seront fournis avec les distributions concernées. La publication d’un téléchargement dans ce dépôt ne place pas automatiquement l’application ou ses ressources sous une licence open source.

---

<div align="center">

**rust-VN Editor** · Documentation et distributions officielles

[Consulter les versions](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/releases)

</div>
