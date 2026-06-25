# La Galaxie ARLEN — Poste de commande

Tableau de bord vivant des chantiers ARLEN (D42). Vue d'ensemble pilotable : *où on est · où on va · qui fait quoi*.

- **V1** — lecture seule, données en dur, 3 vues + swipe. Statique pur (1 fichier `index.html`, zéro build, zéro dépendance). Servi par GitHub Pages.
- **DA** — objets flottants dans un ciel blanc cassé, pastel apaisé, full motion doux.

## Vues
- **Galaxie** — les 7 territoires flottants (toggle *par territoire / par instance*) + le chemin critique vers l'ASR. Clic → carte de détail.
- **Liste** — tous les chantiers, filtrables (instance · état · territoire) et triables.
- **Calendrier** — chantiers par date d'action ou date-cible.

## Données / Rendu
`index.html` sépare strictement les **données** (objet `CHANTIERS`, en haut du `<script>`, commenté) du **rendu** (fonctions `render*`). Mise à jour V1 = éditer `CHANTIERS` à la main (Build + Lead, au fil de l'eau).

**Phase 2** (séparée) : remplacer la fonction `loadData()` par une lecture depuis la Galaxie Notion — sans toucher au rendu.

## Lancer en local
Ouvrir `index.html`, ou servir le dossier (`python3 -m http.server`).
