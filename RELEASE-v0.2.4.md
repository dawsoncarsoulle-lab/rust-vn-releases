# rust-VN 0.2.4 — bêta publique Linux et Windows

Release principale (« Latest ») à la demande de Dawson, le 23 septembre 2026.
Cette bêta est téléchargeable publiquement et proposée par le canal de mise à
jour. Ce statut n'est pas une validation complète Linux/Windows ; les limites
ci-dessous restent applicables.

## Corrections

- Fermeture de l'éditeur par la croix rétablie, protection des graphes conservée.
- Correction du plantage du jeu à la fermeture pendant un dialogue ou un choix.
- Nouveaux labels disponibles avant sauvegarde et personnages accessibles entre graphes.
- Diagnostics de pins accordés à la langue de l'éditeur.
- Retour au véritable Call depuis les choix et conditions.
- Sélecteur de label redessiné, recherche et navigation clavier.
- Améliorations de l'accueil, des vignettes, pictogrammes et aperçu navigateur.

## Téléchargements et installation

Linux : `rust-VN-Editor-x86_64.AppImage` (rendre exécutable puis lancer).
Windows : extraire entièrement `rust-VN-Editor-windows-x86_64.zip` dans un
dossier neuf et lancer `rust-vn-editor.exe`. Conserver les projets ailleurs.
Ne pas désactiver l'antivirus. Les paquets ne sont pas signés ; les restrictions
de sécurité Windows peuvent empêcher leur exécution.

Recréer les exports de jeu pour bénéficier du moteur corrigé : les anciens
exports ne sont pas mis à jour automatiquement.

## Vérification et limites connues

Tests automatisés réussis et compilations Linux/Windows/Web réussies.
AppImage exacte : lancement, CLI, fermeture de l'éditeur et fermeture du moteur
pendant dialogue/choix sous XWayland vérifiés sans panic.
[Résultats Linux et captures](https://github.com/dawsoncarsoulle-lab/rust-vn-releases/blob/main/validation/20260923-linux/RESULTATS.md).

La candidate précédente a été testée partiellement sous Windows 11 ; le
correctif de fermeture de ce paquet doit encore être retesté sur Windows natif.
Restent notamment à valider : Ubuntu LTS distinct et systèmes propres, couverture
complète Firefox/Web/FR-EN, mises à jour, licences et testeurs extérieurs.
L'écriture progressive après chargement et les avertissements de traduction
signalés dans le rapport Windows restent à investiguer. Aucune validation
auditive complète de la musique et des effets n'est revendiquée.

## Sources et SHA-256

Éditeur : `98135295e9e3da0364c21888c92aa752bc914ff2`.
Moteur desktop/Web : `98d6a1c9497acfebddd52bd38d23bb5e2946147c`.

- Linux : `739c71a4781c4d2751738a164b046512adcd10e5d72e7f8a19ac0b652d01046c`.
- Windows : `cb1ec801fabd0fb1a2cb0d2a366c5a9d81c9e7b115e3774de4b0d61240149e21`.

## English

Public beta marked Latest, not a fully qualified stable release. Includes
editor/game close fixes, project-wide references and the redesigned label picker.
Linux package checks passed; native Windows retesting of the shutdown fix and
other qualification steps remain pending. Extract Windows into a fresh folder,
keep projects elsewhere, and do not disable antivirus protection. Re-export
games to include the corrected engine. The updater now offers 0.2.4.
