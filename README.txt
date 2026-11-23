RTS MÉDIÉVAL v6.9 — fichiers à placer à la racine du dépôt GitHub

  main.py  game.py  net.py  campaign.py  assets_data.py  sounds_data.py
  make_icons.py  presplash.png  icon.png  buildozer.spec

Compilation : .github/workflows/build.yml (inclus ; sinon le créer sur GitHub avec le contenu de build.yml.txt).
L'APK est dans Actions > dernier run > Artifacts > rtsmedieval-apk.
(presplash.png et icon.png sont aussi recréés automatiquement pendant la compilation s'ils manquent.)

Nouveautés v6.1 : personnages et Horde de l'intro corrigés (miroir), mise en page de l'interface sans chevauchement,
écran de démarrage Android, menu de la partie (reprendre / sauvegarder / charger / quitter),
sauvegarde et chargement dans chaque mode (escarmouche, campagne y compris tutoriels, multijoueur côté hôte).

v6.2 : boutons et noms de l'interface de jeu refaits : textes qui s'adaptent à la place disponible,
cartes d'action plus grandes (icône, nom sur 2 lignes, coût), boutons d'outils dimensionnés d'après l'écran,
aucun chevauchement entre ressources, objectifs, messages, minicarte, outils et barre du bas.

v6.3 : cartes d'action et boutons d'outils reconstruits en empilement vertical simple (icône, nom, coût/état) :
plus d'icônes ni de noms empilés sur la première carte, icônes d'outils visibles. Seul main.py a changé depuis v6.2.

v6.9 : cartes d'action (barre du bas) réécrites : chaque carte dessine elle-même son icône (haut), son nom (milieu, 2 lignes possibles)
et son coût ou son état (bas) à partir de sa propre taille. Corrige les icônes invisibles, les noms coupés et les icônes de coût décalées.
Seul main.py a changé depuis v6.3 (plus buildozer.spec : version 6.9).

v6.9.1 : « Poser ici » et « Annuler » réagissent dès le toucher (le relâchement du doigt se perdait et il fallait taper plusieurs fois) ;
le son du clic est joué après l'action, sans pouvoir la bloquer ; garde contre un double déclenchement de la pose.

v6.9.2 : « Poser ici » et « Annuler » : l'appui est maintenant capté au niveau de la fenêtre (avant tous les autres widgets),
ce qui évite que ces deux boutons ne reçoivent pas le toucher dans la barre du bas.
