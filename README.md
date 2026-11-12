# Éditeur PDF

PWA pour modifier des PDF directement dans le navigateur, sans serveur : les fichiers ne quittent jamais l'appareil.

## Fonctions

- Ouvrir un ou plusieurs PDF (fusion dans l'ordre d'ajout)
- Réordonner les pages (appui long + glisser, ou flèches)
- Tourner, supprimer des pages
- Exporter tout le document ou seulement la sélection
- OCR optionnel (français + anglais) : ajoute une couche de texte invisible pour rendre les scans recherchables

## Mise en ligne avec GitHub Pages

1. Créer un dépôt sur GitHub et y déposer le contenu de ce dossier (`index.html` à la racine).
2. **Settings → Pages** → Source : *Deploy from a branch* → branche `main`, dossier `/ (root)` → Save.
3. Après 1 à 2 minutes, l'appli est disponible sur `https://<utilisateur>.github.io/<dépôt>/`.
4. Sur iPhone : ouvrir l'adresse dans Safari → Partager → **Sur l'écran d'accueil**.

## Mise à jour

Après une modification de `index.html`, changer `VERSION` dans `sw.js` (ex. `editeur-pdf-v2`) pour forcer le rafraîchissement du cache.

## Bibliothèques

- [pdf.js](https://mozilla.github.io/pdf.js/) 3.11.174 — affichage des pages
- [pdf-lib](https://pdf-lib.js.org/) 1.17.1 — modification et export
- [SortableJS](https://sortablejs.github.io/Sortable/) 1.15.0 — glisser-déposer
- [Tesseract.js](https://tesseract.projectnaptha.com/) 5.1.1 — OCR (chargé uniquement à la première utilisation)

Le premier OCR télécharge environ 10 Mo de données de langue, ensuite mises en cache par le navigateur.
