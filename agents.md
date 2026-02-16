# Guide rapide du projet

Ce dépôt contient une **landing page statique** basée sur le template Namari.

## Structure

- `index.html` : page principale (contenu, sections, navigation, pied de page).
- `style.css` : styles globaux et mise en page.
- `namari-color.css` : thème de couleurs et styles typographiques principaux.
- `font-awesome.css` : styles des icônes Font Awesome.
- `logo.png` : logo affiché dans l'en-tête.

## Comprendre le fonctionnement

1. **Le HTML (`index.html`)** définit les sections (`#banner`, `#about`, `#services`, `#testimonials`, `#clients`, etc.).
2. **Le CSS principal (`style.css`)** gère la grille, les espacements, la navigation et le rendu responsive.
3. **Le CSS de thème (`namari-color.css`)** applique les couleurs et la typographie.
4. Les scripts JavaScript référencés en bas de `index.html` ajoutent les animations/effets, mais les fichiers JS ne sont pas présents dans ce dépôt.

## Conseils pour contribuer

- Modifier le contenu : `index.html`
- Modifier la mise en page : `style.css`
- Modifier les couleurs/typos : `namari-color.css`
- Garder les changements **petits et ciblés** pour limiter les effets de bord.
