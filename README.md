# BK Consulting — site vitrine

Site statique une page pour BK Consulting (développement logiciel et conseil IT, France).

## Structure

- `public/` — le site déployé (HTML statique, aucun build)
  - `index.html` — la page
  - `assets/ceo.png` — photo du fondateur
- `BK Consulting.dc.html`, `support.js`, `uploads/` — export source Claude Design (référence, non déployé)

## Déploiement

Hébergé sur Render en tant que **static site**, branche `main`, `publishPath: public`.
Chaque push sur `main` déclenche un déploiement automatique.

## Personnalisation

- **Grille TJM** : par défaut la section Tarifs affiche « Grille TJM sur demande ».
  Pour afficher la grille de prix, passer `<body data-show-tjm="false">` à `"true"` dans `public/index.html`.
- **Formulaire de contact** : ouvre le client mail du visiteur avec la demande pré-remplie
  (adresse dans la constante `CONTACT_EMAIL` du script en bas de page). Brancher un backend
  (Formspree, Resend, etc.) si un envoi serveur est souhaité.
- Coordonnées, témoignages et logos clients sont des placeholders à remplacer.
