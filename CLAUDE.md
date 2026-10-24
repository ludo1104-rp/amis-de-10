# Les amis de 10

Appli élèves (famille 1, style « doux et illustré », skill `appli-eleve-ipad`).
Compléments à 10 avec le cadre de 10. Code couleur : bleu = le nombre donné,
orange = son ami (ce qui manque pour faire 10).

## État
- 1.0 publiée le 24/10/2026 (dépôt public ludo1104-rp/amis-de-10, GitHub Pages) : reconstruite sur le gabarit de la skill à partir de
  l'artefact « Les compléments de 10 » (`_a-trier/artefacts/complements-de-10/`).
- Jeux : Apprendre, Trouve l'ami, Les paires, Le labyrinthe, Mes calculs
  difficiles, Mes progrès. Ouverture animée, styles Couleurs/Simple, 3 tailles.
- 1.1 publiée le 24/10/2026 : contenu enrichi, les élèves finissaient trop vite.
  Trouve l'ami : 12 / 15 / 20 questions ; calculs à trous variés (7 + ? = 10,
  ? + 7 = 10, 10 = 7 + ?, 10 − 7 = ?), 10 petites histoires (`HISTOIRES`,
  moyen et grand défi), 70 + ? = 100 au grand défi (`TYPES_COMP`).
  Paires : 6 / 8 / 10 lignes, 4 / 6 / 9 nombres. Labyrinthe : 4×4 / 5×5 / 6×6,
  calculs à 3 nombres au grand défi.
- Défis : Trouve l'ami (cadre affiché + 3 choix / 3 choix / clavier 0-10).
- Animations : points du cadre qui apparaissent, cases vides qui se remplissent
  en orange après la réponse, chemin du labyrinthe qui s'allume, anneau et
  étoiles du résultat. Coupées si l'iPad réduit les animations.
- Source : aucun document de départ (« Application produite par IA »).
- 24/10/2026 : logo « Ludo. » tout en haut à gauche de l'accueil (déplacé le 24/10, non cliquable) + lien rprof1.com dans les mentions (publié le 24/10/2026).

## Fichiers
- `index.html` : toute l'appli. Réglages `APP` et contenu en section 2.
- `window.__appli` expose bonneReponse, paire, chemin pour les tests.

## Pièges
- Ne jamais changer `APP.cle` (`amis-de-10`) ni les clés `c:0`…`c:10`
  (calculs) et `p:0`…`p:5` (paires) : la progression des iPads en dépend.
- Les histoires et le « 100 » gardent la clé `c:a` (même ami de 10).
- Histoires : nombre de 1 à 9 seulement ; accord `{bille|billes}` selon le nombre.
- Tests : `verif_ipad.py` de la skill + un parcours Playwright headless (3 défis
  × 3 parties de chaque jeu), à recréer depuis `test_parcours.py` de la skill.

## Prochaine étape
- Essai sur iPad : voix (Écouter), vrai doigt, webclip.
