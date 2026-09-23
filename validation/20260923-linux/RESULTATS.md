# Fermeture du jeu sur Linux — 23 septembre 2026

## Retest du paquet final

AppImage SHA-256 : `739c71a4781c4d2751738a164b046512adcd10e5d72e7f8a19ac0b652d01046c`.
Le paquet exact destiné au brouillon a également été testé :

- Accueil de l'éditeur affiché sous Wayland, depuis /tmp avec PATH limité ;
  fermeture par la croix via son API d'entrée : code de sortie 0.
- CLI embarqué : --help réussi.
- Moteur embarqué (--engine), dialogue puis choix dans deux processus
  indépendants sous XWayland : fermeture demandée par wmctrl, sorties 0,
  aucun panic dans les journaux joints.
- Captures appimage-launch.png, appimage-dialogue.png et appimage-choice.png
  inspectées visuellement ; aucune fenêtre de test laissée ouverte.

Les limites du backend XWayland et l'absence de retest Windows restent valables.

## Premier test du moteur hors paquet

Moteur release corrigé, commit `98d6a1c9497acfebddd52bd38d23bb5e2946147c`.
Projet temporaire avec menus personnalisés Dialogue, Choices et QuickActions,
copiés du modèle Illustré. Aucun projet ni fichier de sauvegarde utilisateur utilisé.

Exécution graphique réelle sous Pop!_OS, backend X11 via XWayland
(`WINIT_UNIX_BACKEND=x11`, `WAYLAND_DISPLAY` vide).
Le pilote QA existant avance au dialogue puis au choix et prend des captures.
Un contrôleur externe envoie la demande du gestionnaire de fenêtres
`wmctrl -ic` à la fenêtre identifiée par le PID du processus de test, dès la
capture de l'état attendu. Aucun kill ni AppExit forcé utilisé dans ces deux cas.

- Dialogue affiché (dialogue.png), fermeture demandée : processus terminé avec code 0.
- Choix affiché (choice.png), fermeture demandée : processus terminé avec code 0.
- Les deux journaux ne contiennent aucun panic, NoEntities ou backtrace.
- Aucune fenêtre de test restante après vérification.

Limites : ce test ne simule pas physiquement le clic sur la croix ni Alt+F4.
Il teste la demande de fermeture du gestionnaire de fenêtres sur XWayland,
pas le backend Wayland natif ni Windows. Le moteur a été lancé directement
sur le projet temporaire, pas via un nouvel AppImage ni depuis l'éditeur.
Un premier essai exploratoire ayant dépassé le choix avant fermeture a été
exclu des résultats ; seules les deux relances synchronisées sont retenues.
