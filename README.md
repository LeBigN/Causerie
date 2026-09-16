# Causerie Sécurité — Démarrage de chantier (PWA)

Fiche de causerie sécurité LOXAM Module : consignes du jour à cocher, échanges de
l'équipe, émargement tactile des participants, signature de l'animateur et PDF
officiel A4 (même charte que les autres apps LOXAM Module).

## Contenu

- `index.html` — l'appli (seul fichier à modifier pour changer le contenu)
- `manifest.json` — nom, icône, couleurs de l'app installée
- `service-worker.js` — fonctionnement hors-ligne (cache `causerie-securite-v1`)
- `icons/` — icônes de l'app (casque blanc sur fond rouge)
- `vendor/jspdf.umd.min.js` — génération de PDF embarquée en local (repli CDN si absent)

## Mise en ligne (GitHub Pages)

1. Nouveau dépôt, par ex. `Causerie-Securite`, en **Public**
2. **Add file → Upload files** : déposer tout le contenu du dossier
   (`index.html`, `manifest.json`, `service-worker.js`, `README.md`, `icons/`, `vendor/`)
3. **Settings → Pages** → Deploy from a branch → `main` / `(root)` → Save
4. URL : `https://<pseudo>.github.io/Causerie-Securite/`

## Installation sur téléphone / tablette

- Android (Chrome) : menu ⋮ → « Ajouter à l'écran d'accueil »
- iPhone / iPad (Safari) : Partager → « Sur l'écran d'accueil »

## Fonctionnement

- Brouillon enregistré automatiquement sur l'appareil (y compris les signatures)
- Pavés de signature verrouillés : appuyer sur « Appuyer pour signer » avant de tracer
- Aucune consigne cochée par défaut ; la date du jour est pré-remplie (modifiable)
- Chantiers, animateurs et entreprises déjà saisis sont proposés en suggestion
- Avant le PDF, une fenêtre liste les points manquants (« Compléter » ou « Générer quand même »)
- PDF sur une page dans le cas courant ; 6 lignes d'émargement au minimum
  (lignes vierges pour signature manuscrite), en-tête de tableau répété si plusieurs pages
- Envoi du PDF par le partage natif (WhatsApp, Mail…) quand l'appareil le permet,
  sinon téléchargement classique

## Mise à jour

Remplacer `index.html`, puis passer `CACHE_NAME` à `causerie-securite-v2`
(v3, v4…) dans `service-worker.js`, et `APP_VERSION` dans `index.html`.
