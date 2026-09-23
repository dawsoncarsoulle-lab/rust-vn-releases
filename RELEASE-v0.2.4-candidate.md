# rust-VN 0.2.4 — correctif Linux et Windows du 23 septembre 2026

## Paquets actuels — Linux et Windows corrigés

Les deux paquets embarquent maintenant le moteur corrigé
`98d6a1c9497acfebddd52bd38d23bb5e2946147c`, y compris le moteur Web.
Éditeur : `98135295e9e3da0364c21888c92aa752bc914ff2`.

- Linux AppImage : `739c71a4781c4d2751738a164b046512adcd10e5d72e7f8a19ac0b652d01046c`.
- Windows ZIP : `cb1ec801fabd0fb1a2cb0d2a366c5a9d81c9e7b115e3774de4b0d61240149e21`.

Les indications ci-dessous sur une AppImage non corrigée sont historiques.
La release reste en brouillon ; les validations restantes ne sont pas levées.

AppImage exacte vérifiée sur Pop!_OS : accueil, CLI et fermeture de l'éditeur ;
fermeture du moteur embarqué pendant dialogue et choix sous XWayland, sans
panic et avec sortie 0. Voir [résultats et captures](validation/20260923-linux/RESULTATS.md).

## Historique de la mise à jour Windows

## Mise à jour du 23 septembre — à lire en priorité

Le ZIP Windows a été remplacé après le rapport de validation Windows natif
fourni par Dawson. Le moteur desktop et Web inclus contient le correctif de
fermeture : le rendu ne suppose plus que la fenêtre existe au dernier cycle.
Deux tests exécutant les vrais systèmes de rendu après destruction de fenêtre
passent ; les suites rvn_bevy, rvn_core et rvn_ui et les constructions Linux,
Windows et Web passent. Le nouveau paquet reste à retester sur Windows natif.

- Éditeur inchangé : `98135295e9e3da0364c21888c92aa752bc914ff2`.
- Moteur du nouveau ZIP : `98d6a1c9497acfebddd52bd38d23bb5e2946147c`.
- SHA-256 Windows : `cb1ec801fabd0fb1a2cb0d2a366c5a9d81c9e7b115e3774de4b0d61240149e21`.
- **L'AppImage Linux ci-dessous reste celle du 22 septembre, sans ce correctif.**

Extraire le nouveau ZIP dans un dossier neuf. Tester la croix et Alt+F4 pendant
un dialogue et un choix, dans l'aperçu puis dans un **nouvel export desktop**.
Les anciens jeux exportés ne sont pas mis à jour automatiquement.
Le rapport Windows confirme des essais partiels sur l'ancien paquet ; cela
ne certifie pas ce nouveau paquet. Les autres anomalies et validations restent
ouvertes, notamment l'écriture progressive après chargement et les traductions.
La release reste en brouillon et la version publique reste 0.2.3.

## Historique de la candidate du 22 septembre (empreintes anciennes)

**Brouillon de validation, non publié.** Les nouveaux paquets Linux et Windows
remplacent ceux du 21 septembre. Les validations liées aux anciennes empreintes
ne valent pas pour ces fichiers. La dernière version publique reste 0.2.3.

## Corrections incluses

- Fermeture par la croix rétablie ; protection des graphes non enregistrés conservée.
- Labels nouvellement créés disponibles dans les sélecteurs, même avant sauvegarde.
- Personnages du projet disponibles depuis les différents graphes.
- Libellés de pins dans les diagnostics et l’inspecteur accordés à la langue de l’éditeur.
- `Return` reprend après le véritable `Call`, y compris depuis un choix ou une condition.
- Nœud Référence de label redessiné : champ déroulant, chevron, survol, recherche,
  sélection clavier et ouverture au-dessus lorsque la place manque en dessous.
- Inclut aussi les améliorations précédentes de l’accueil, des pictogrammes,
  des vignettes de projet et du lancement dans le navigateur.

## Sources et intégrité

- Éditeur : `98135295e9e3da0364c21888c92aa752bc914ff2`.
- Moteur/CLI : `5a22461cc5e2d507751f41fe8db08bc2a62b38a6`.
- `rust-VN-Editor-x86_64.AppImage` :
  `549238da8a8d40191c2f1257941c25c04a7d6cedb138505c90e23c9a1b85b005`.
- `rust-VN-Editor-windows-x86_64.zip` :
  `09c3f06274b006f8855541e7a83d38174c4df2fef787a2f615cb13879c47dce6`.

## Vérifications effectuées

- 93 tests éditeur et 5 tests du contrôle de publication réussis.
- Suites release `rvn_core`, `rvn_graph`, `rvn_ui`, `rvn_cli` et `rvn_bevy` réussies.
- Compilation Linux et cross-compilation Windows réussies ; archive ZIP contrôlée par CRC.
- AppImage exacte lancée depuis `/tmp` avec PATH limité, accueil inspecté,
  fermeture par sa croix réussie et CLI embarqué lancé.
- Sur le binaire éditeur identique à celui du paquet : modification d’un graphe
  temporaire, premier clic de fermeture bloqué avec récupération conservée,
  second clic de confirmation fermant correctement le processus.

Ces contrôles Linux ont été réalisés sur le poste de développement Pop!_OS,
sous GNOME/Wayland. Ils ne remplacent pas un test sur machine vierge.

## Avant publication commune

Restent à valider sur les paquets exacts : Windows natif, Ubuntu LTS distinct,
installation propre, exports desktop, parcours complets FR/EN et trois fins,
Chrome et Firefox, mises à jour depuis l’ancienne version, audit complet des
licences et retours des testeurs extérieurs. Aucun résultat Windows natif n’est
revendiqué. Aucun changement du canal public de mise à jour.

Windows : télécharger le ZIP du brouillon avec le compte propriétaire, extraire
entièrement dans un dossier neuf, puis suivre `WINDOWS-TEST.md` inclus.
Ne pas désactiver l’antivirus. Conserver les projets hors du dossier de l’app.
Ubuntu : suivre `UBUNTU-TEST.md` joint au brouillon.

## English summary

Updated **draft testing candidate**, not a validated public release. Includes
window-close handling, project-wide character/label references, translated pin
diagnostics, correct return-from-branch behavior and the redesigned label selector.
Linux package startup and close were checked; Windows was cross-compiled and its
ZIP checked, but native Windows and full release qualification are still pending.
Public version and updater remain at 0.2.3. Extract Windows into a new directory;
keep projects elsewhere and do not disable antivirus protection.
