# Descriptions des Fichiers - Namari Landing Page Template

## 📋 Vue d'ensemble du Projet

**Namari** est un modèle de page d'accueil gratuit et réactif (version 1.1.0) créé par ShapingRain. C'est un template HTML5/CSS3 complet conçu pour les sites web marketing, promotionnels et de présentation professionnelle. Le projet inclut une mise en page responsive, des effets de parallaxe, des animations fluides et une intégration avec les réseaux sociaux.

### Caractéristiques principales
- Design responsive et mobile-friendly
- Effets de parallaxe et animations
- Section features/services avec icônes
- Galerie de clients avec overlay
- Section testimonials/avis clients
- Section pricing avec plans tarifaires
- Intégration réseaux sociaux (Facebook, Twitter, Instagram, Google+, Behance)
- Navigation fluide avec scroll-up automatique

---

## 📁 Structure du Répertoire

```
Test2/
├── index.html              # Page d'accueil principale (436 lignes)
├── style.css               # Feuille de style principale (2,332 lignes)
├── namari-color.css        # Variables de couleur/thème (328 lignes)
├── font-awesome.css        # Bibliothèque d'icônes Font Awesome (2,337 lignes)
├── logo.png                # Logo du site (326 × 57 pixels)
├── FILE_DESCRIPTIONS.md    # Ce fichier
└── .git/                   # Répertoire Git (historique et métadonnées)
```

---

## 📄 Descriptions Détaillées des Fichiers

### 1. **index.html** - Page d'Accueil Principale
**Type:** Document HTML
**Taille:** 436 lignes
**Importance:** 🔴 Critique

#### Contenu et Structure
Le fichier `index.html` est le cœur du template. Il contient la structure complète de la page d'accueil avec les sections suivantes:

**En-tête et Métadonnées:**
- Charset UTF-8
- Meta tags pour viewport responsive
- Titre de la page
- Liens vers les fichiers CSS (style.css, namari-color.css, font-awesome.css)

**Sections de Contenu:**
1. **Header/Navigation**
   - Logo du site (logo.png)
   - Menu principal: Accueil, À propos, Galerie, Services, Avis, Clients, Tarification
   - Icônes réseaux sociaux (Facebook, Google+, Twitter, Instagram, Behance)

2. **Banner/Hero Section**
   - Headline: "A FREE AND SIMPLE LANDING PAGE"
   - Bouton d'appel à l'action (CTA)
   - Image/fond de bannière

3. **Section Features**
   - 4 blocs avec icônes:
     - HTML5/CSS3 (technologie web moderne)
     - Easy to Use (simplicité d'utilisation)
     - Responsive (design adaptatif)
     - Parallax Effect (effets visuels)

4. **Section Services**
   - Description des services
   - Intégration vidéo
   - Témoignages clients

5. **Section Testimonials**
   - Citations de clients satisfaits
   - Noms et titres des clients

6. **Section Clients**
   - Logos des entreprises partenaires
   - Overlays au survol

7. **Section Pricing**
   - Plans tarifaires avec features

8. **Footer**
   - Informations de copyright
   - Icônes réseaux sociaux

#### Dépendances Externes
```javascript
- jQuery
- WOW.js (animations au scroll)
- Featherlight (galerie lightbox)
- Parallax.js (effets de parallaxe)
- jQuery ScrollUp
- site.js (script personnalisé local)
```

#### Répertoires Référencés (non inclus)
- `images/` - Toutes les images du site (bannière, icônes, galerie, clients)
- `js/` - Fichiers JavaScript supplémentaires

#### Notes
- Le fichier référence des répertoires `images/` et `js/` qui ne sont pas présents dans le repository
- Utilise les icônes Font Awesome pour les éléments visuels
- Conçu pour être complété avec des assets externes

---

### 2. **style.css** - Feuille de Style Principale
**Type:** Feuille de style CSS3
**Taille:** 2,332 lignes
**Importance:** 🔴 Critique

#### Contenu et Sections
Le fichier `style.css` contient tous les styles visuels du template et est organisé en sections logiques:

**Styles Généraux:**
- Reset CSS (box-sizing, margin, padding par défaut)
- Typography globale (polices, tailles)
- Éléments HTML de base (html, body, div, etc.)

**Composants UI:**
- **Header:** styling du menu de navigation, logo, icônes sociales
- **Buttons:** styles des boutons avec états (normal, hover, active)
- **Navigation:** menu responsive, styles de lien
- **Images:** responsive images, lazy loading support

**Sections de Contenu:**
- **Banner:** full-width hero section, overlay, texte centré
- **Features/Services:** grid layout, card styling, icônes
- **Testimonials:** carousel/slider styling
- **Gallery:** grid layout, lightbox triggers
- **Clients:** logo grid avec overlays
- **Pricing:** plans comparison, tables

**Responsive Design:**
- Media queries pour tablettes et mobiles
- Breakpoints pour adaptatif

**Effets Visuels:**
- Transitions CSS3 smooth
- Transform pour animations
- Opacity transitions
- Hover effects

**Footer:**
- Styling de pied de page
- Spacing et positionnement

#### Caractéristiques
- Utilise des variables CSS et des préfixes vendeurs (-webkit-, -moz-, -ms-)
- Tous les styles sont dans un seul fichier pour performance
- Bien organisé avec sections commentées
- Support complet de la compatibilité cross-browser

#### Dépendances
- Police externe: Google Fonts ou système
- Font Awesome icons (via font-awesome.css)
- Couleurs définies dans namari-color.css

---

### 3. **namari-color.css** - Variables de Couleur et Thème
**Type:** Feuille de style CSS
**Taille:** 328 lignes
**Importance:** 🟡 Importante

#### Contenu et Structure
Le fichier `namari-color.css` définit la palette de couleurs et les variables visuelles du template, permettant une personnalisation facile du thème sans modifier le CSS principal.

**Schéma de Couleur Principal:**
- **Couleur d'accent:** #d2b356 (or/tan doré)
- **Couleur de fond:** Blanc/clair
- **Texte primaire:** Gris foncé/noir
- **Texte secondaire:** Gris moyen

**Sections Thématisées:**
1. **Website Default**
   - Couleurs de fond et lien globales
   - Couleurs par défaut des éléments

2. **Header/Navigation**
   - Couleur du menu
   - Couleur du hover de menu
   - Couleur des icônes sociales

3. **Primary & Secondary Colors**
   - Couleur primaire (or #d2b356)
   - Couleur secondaire pour contraste

4. **Banner Section**
   - Couleurs du texte bannière
   - Overlay background

5. **Typography**
   - Couleurs des titres (h1-h6)
   - Couleurs du corps de texte

6. **Buttons**
   - Couleur de fond
   - Couleur au hover
   - Couleur du texte

7. **Footer**
   - Couleur de fond du footer
   - Couleur du texte
   - Couleur des liens

#### Utilisation
Ces couleurs sont appliquées via des sélecteurs CSS dans `style.css`. Modifier ce fichier permet de changer le thème global sans toucher aux autres feuilles de style.

#### Exemple d'Utilisation
```css
.button {
  background-color: #d2b356;
  color: white;
}

.button:hover {
  background-color: #c9a646;
}
```

---

### 4. **font-awesome.css** - Bibliothèque d'Icônes Font Awesome
**Type:** Feuille de style CSS (Bibliothèque)
**Taille:** 2,337 lignes
**Importance:** 🟡 Importante

#### Contenu et Spécifications
Le fichier `font-awesome.css` est la feuille de style pour Font Awesome version 4.7.0, une bibliothèque d'icônes vectorielles complète.

**Font Face Declarations:**
- Supporte plusieurs formats de police:
  - `.eot` - Internet Explorer
  - `.woff2` - Web fonts (optimisé)
  - `.woff` - Compatibilité large
  - `.ttf` - TrueType
  - `.svg` - Fallback SVG

**Icônes Disponibles (600+):**
Le fichier définit les styles pour plus de 600 icônes Font Awesome, notamment:
- `fa-html5`, `fa-css3` - Technologies web
- `fa-tablet`, `fa-mobile` - Appareils
- `fa-rocket`, `fa-gear` - Actions
- `fa-heart`, `fa-star` - Sentiment
- `fa-facebook`, `fa-twitter`, `fa-instagram` - Réseaux sociaux
- Et beaucoup d'autres...

**Classes Utilitaires:**
- `.fa-lg` - Large
- `.fa-2x`, `.fa-3x`, `.fa-4x`, `.fa-5x` - Multiplicateurs de taille
- `.fa-fw` - Fixed width (alignement)
- `.fa-rotate-90`, `.fa-rotate-180`, `.fa-rotate-270` - Rotations
- `.fa-flip-horizontal`, `.fa-flip-vertical` - Flip
- `.fa-spin` - Animation rotation
- `.fa-pulse` - Animation pulsation

**Licences:**
- Font: SIL OFL (Open Font License) 1.1
- CSS: MIT License

#### Utilisation dans le Template
Les icônes sont utilisées via la syntaxe:
```html
<i class="fa fa-html5"></i>
<i class="fa fa-rocket"></i>
<i class="fa fa-facebook"></i>
```

#### Dépendances
- **Fichiers de police:** Situées dans un répertoire `fonts/` (non inclus dans ce repository)
- Chemins des fonts: `/fonts/fontawesome-webfont.*`

---

### 5. **logo.png** - Logo du Site
**Type:** Image PNG
**Format:** PNG 8-bit RGBA (avec transparence)
**Dimensions:** 326 × 57 pixels
**Taille:** ~2.8 KB
**Importance:** 🟢 Supplémentaire (mais important pour la marque)

#### Spécifications Techniques
- **Compression:** Non-interlacée
- **Couleurs:** Palette optimisée 8-bit
- **Transparence:** Support RGBA (fond transparent)
- **Résolution:** 72 DPI (standard web)

#### Utilisation
Le logo est affiché dans le header/navigation du site (voir `index.html` ligne ~50):
```html
<img src="logo.png" alt="Namari Logo" class="logo">
```

#### Dimensions et Aspect Ratio
- Largeur: 326px
- Hauteur: 57px
- Aspect ratio: ~5.7:1 (format horizontal allongé, typique pour un logo)

#### Notes
- Le logo est utilisé dans la navigation principale
- Peut être redimensionné via CSS pour responsive design
- Format PNG permet transparence, idéal pour fond variable

---

## 🛠️ Stack Technologique

### Frontend
- **HTML5** - Structure et sémantique
- **CSS3** - Styling avec media queries responsive
- **JavaScript** - Interactivité (jQuery-based)

### Bibliothèques Externes
| Bibliothèque | Version | Utilisation |
|---|---|---|
| jQuery | (version non spécifiée) | DOM manipulation et events |
| WOW.js | - | Animations au scroll |
| Featherlight | - | Galerie lightbox |
| Parallax.js | - | Effets de parallaxe |
| jQuery ScrollUp | - | Bouton "retour au top" |
| Font Awesome | 4.7.0 | Icônes vectorielles |

### Outils de Support
- Git - Contrôle de version
- Responsive Web Design - Mobile-first approach

---

## 📦 Dépendances Manquantes

Les fichiers et répertoires suivants sont référencés dans le code mais **ne sont pas présents** dans ce repository:

### Répertoires
- `images/` - Images du site (bannière, icônes, galerie, logos clients)
- `js/` - Fichiers JavaScript supplémentaires et libraires

### Fichiers
- `js/site.js` - Script personnalisé local
- `fonts/fontawesome-webfont.*` - Fichiers de police Font Awesome (tous formats)

### Bibliothèques JavaScript
- jQuery (CDN ou local)
- WOW.js (CDN ou local)
- Featherlight (CDN ou local)
- Parallax.js (CDN ou local)
- jQuery ScrollUp (CDN ou local)

---

## ⚙️ Configuration et Personnalisation

### Pour Modifier le Thème de Couleur
Éditer `namari-color.css`:
1. Localiser la section correspondante
2. Modifier les valeurs hex (#d2b356 → votre couleur)
3. Sauvegarder et tester dans le navigateur

### Pour Ajouter/Modifier du Contenu
Éditer `index.html`:
1. Localiser la section à modifier
2. Mettre à jour le texte, images ou structure
3. Ajouter/remplacer les images dans le répertoire `images/`

### Pour Ajuster les Styles
Éditer `style.css`:
1. Trouver la section pertinente (commentée)
2. Modifier les propriétés CSS
3. Utiliser les media queries pour responsive

---

## 📝 Notes Importantes

1. **État du Repository:** Le template est complet mais les assets externes (images, polices, scripts) ne sont pas inclus. C'est typique pour un template de distribution.

2. **Performance:** Avec 2,300+ lignes CSS, considérer la minification et la compression pour production.

3. **Compatibilité:** Conçu pour navigateurs modernes (IE10+, tous les navigateurs récents).

4. **Responsive:** Utilise mobile-first avec breakpoints pour tablette et desktop.

5. **SEO:** Utilise la sémantique HTML5 appropriée pour une bonne structure SEO.

---

## 📚 Ressources Utiles

- Font Awesome 4.7: https://fontawesome.com/v4.7.0/
- jQuery: https://jquery.com/
- HTML5: https://html.spec.whatwg.org/
- CSS3: https://www.w3.org/Style/CSS/

---

**Document créé:** 2026-03-04
**Version Template:** Namari 1.1.0
**Créateur:** ShapingRain
