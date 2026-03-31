# 📋 TODO - Améliorations possibles pour Test2

Ce fichier liste toutes les améliorations potentielles du projet Test2, organisées par catégorie et priorité.

## 🔴 **1. Infrastructure & Configuration** (HAUTE PRIORITÉ)

- [ ] **README.md** - Ajouter une documentation complète avec :
  - Description du projet
  - Instructions d'installation
  - Guide d'utilisation
  - Informations de déploiement

- [ ] **package.json** - Créer pour documenter les dépendances CDN et les versions:
  ```json
  {
    "name": "test2-landing",
    "version": "1.0.0",
    "description": "Landing page - Template Namari"
  }
  ```

- [ ] **.gitignore** - Ajouter les entrées communes:
  ```
  node_modules/
  .DS_Store
  *.log
  dist/
  build/
  .env*
  ```

- [ ] **LICENSE** - Ajouter une licence MIT ou appropriée

- [ ] **.editorconfig** - Pour la cohérence du code entre éditeurs:
  ```
  [*]
  charset = utf-8
  end_of_line = lf
  insert_final_newline = true
  trim_trailing_whitespace = true

  [*.{html,css,js}]
  indent_style = space
  indent_size = 2
  ```

---

## ⚡ **2. Performance** (HAUTE PRIORITÉ)

- [ ] **Mettre à jour jQuery** - Upgrade jQuery 1.8.3 vers 3.x (sécurité + performance)
  - Tester la compatibilité des plugins
  - Remplacer `site.js` si nécessaire

- [ ] **Minification CSS** - Minifier les fichiers CSS en production:
  - `style.css` → `style.min.css` (2332 → ~1500 lignes)
  - `namari-color.css` → `namari-color.min.css`
  - `font-awesome.css` → `font-awesome.min.css`

- [ ] **Image Optimization**
  - Compresser `logo.png` (actuellement 2.8K)
  - Convertir en WebP avec fallback PNG
  - Ajouter responsive images avec `srcset`

- [ ] **Lazy Loading**
  - Implémenter lazy loading pour les images
  - Charger les scripts tiers (jQuery plugins) de manière asynchrone
  - Defer ou async sur les scripts non-critiques

- [ ] **Service Worker** - Ajouter pour :
  - Cache offline
  - Amélioration des performances de chargement
  - Support PWA basique

- [ ] **Créer sitemap.xml** - Pour le SEO:
  ```xml
  <urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
      <loc>https://domain.com/</loc>
      <changefreq>monthly</changefreq>
      <priority>1.0</priority>
    </url>
  </urlset>
  ```

- [ ] **Gzip/Brotli Compression** - Configurer au niveau serveur

---

## 🌐 **3. Accessibilité & SEO** (PRIORITÉ MOYENNE)

### SEO
- [ ] **Meta Tags complets** - Ajouter dans `<head>`:
  ```html
  <meta name="description" content="...">
  <meta name="keywords" content="...">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta property="og:title" content="...">
  <meta property="og:description" content="...">
  <meta property="og:image" content="...">
  <meta name="twitter:card" content="summary_large_image">
  ```

- [ ] **robots.txt** - Créer pour les crawlers:
  ```
  User-agent: *
  Allow: /
  Sitemap: https://domain.com/sitemap.xml
  ```

- [ ] **Structured Data** - Ajouter JSON-LD pour:
  - Organization
  - LocalBusiness
  - Review/Rating

### Accessibilité
- [ ] **ARIA Labels** - Ajouter pour:
  - Navigation principale
  - Boutons icon-only
  - Sections principales (landmark roles)
  - Formulaires

- [ ] **Alt Text** - Ajouter à toutes les images:
  ```html
  <img src="logo.png" alt="Test2 Logo">
  ```

- [ ] **Contraste des couleurs** - Vérifier ratio WCAG:
  - Couleur primaire doré (#d2b356) sur fond blanc
  - Utiliser outil de test: WebAIM Contrast Checker

- [ ] **Structure des en-têtes** - Assurer une hiérarchie correcte:
  - Un seul `<h1>` par page
  - Hiérarchie logique h1 → h2 → h3

- [ ] **Focus Visible** - Améliorer le style focus pour clavier:
  ```css
  *:focus-visible {
    outline: 2px solid #d2b356;
    outline-offset: 2px;
  }
  ```

- [ ] **Tester avec** :
  - axe DevTools
  - WAVE WebAIM
  - Lighthouse Accessibility

---

## 💅 **4. Code Quality** (PRIORITÉ MOYENNE)

### CSS
- [ ] **Refactoriser CSS** :
  - Supprimer les doublons
  - Introduire CSS Variables:
    ```css
    :root {
      --color-primary: #d2b356;
      --color-text: #333;
      --spacing-unit: 1rem;
    }
    ```
  - Remplacer le système de grille custom par CSS Grid/Flexbox

- [ ] **Organiser les fichiers CSS** :
  ```
  /styles
    ├── base.css (reset, variables)
    ├── layout.css (grid, flexbox)
    ├── components.css (buttons, cards)
    ├── theme.css (colors)
    └── responsive.css (media queries)
  ```

- [ ] **Ajouter Stylelint** - Linter CSS:
  ```bash
  npm install --save-dev stylelint stylelint-config-standard
  ```

### HTML
- [ ] **Ajouter HTMLHint** - Validation HTML:
  ```bash
  npm install --save-dev htmlhint
  ```

- [ ] **Vérifier les balises fermées correctement**
- [ ] **Améliorer la sémantique HTML** :
  - Utiliser `<header>`, `<nav>`, `<section>`, `<article>`, `<footer>`
  - Remplacer `<div>` par des balises sémantiques appropriées

### JavaScript
- [ ] **Tester tous les plugins jQuery** avec la nouvelle version
- [ ] **Ajouter ESLint** si du JS custom est ajouté:
  ```bash
  npm install --save-dev eslint eslint-config-standard
  ```

---

## 🛠️ **5. Développement** (PRIORITÉ MOYENNE)

- [ ] **Bundler/Build Tool** - Ajouter Vite ou Parcel:
  ```bash
  npm install --save-dev vite
  ```
  - Minification automatique
  - Hot Module Replacement
  - Optimisation des assets

- [ ] **Watch Mode** - Script développement:
  ```json
  "scripts": {
    "dev": "vite --host",
    "build": "vite build",
    "preview": "vite preview"
  }
  ```

- [ ] **Makefile** (optionnel) - Pour commandes courantes:
  ```makefile
  .PHONY: dev build lint test
  dev:
    npm run dev
  ```

- [ ] **Pre-commit Hooks** - Avec husky:
  ```bash
  npm install --save-dev husky
  npx husky install
  npx husky add .husky/pre-commit "npm run lint"
  ```

---

## ✅ **6. Testing & CI/CD** (PRIORITÉ BASSE)

- [ ] **Lighthouse** - Tests de performance:
  ```bash
  npm install --save-dev @lhci/cli@^0.8.0 @lhci/config@^0.8.0
  ```

- [ ] **GitHub Actions** - CI/CD basique:
  - Lint CSS/HTML
  - Build du projet
  - Tests Lighthouse
  - Déploiement automatique

- [ ] **Tests d'accessibilité** - axe-core:
  ```bash
  npm install --save-dev @axe-core/react
  ```

- [ ] **Cross-browser testing** - BrowserStack ou Sauce Labs

---

## 🚀 **7. Déploiement** (PRIORITÉ BASSE)

- [ ] **Documenter le déploiement** dans README

- [ ] **Netlify/Vercel** - Configuration (optionnel):
  - `netlify.toml` ou `vercel.json`
  - Env variables
  - Build commands

- [ ] **Docker** (optionnel) - Ajouter Dockerfile:
  ```dockerfile
  FROM nginx:alpine
  COPY . /usr/share/nginx/html
  ```

- [ ] **HTTPS Enforcement** - Configuration serveur

- [ ] **CDN** - Mettre en cache les assets statiques

---

## 📚 **8. Documentation** (PRIORITÉ BASSE)

- [ ] **CONTRIBUTING.md** - Guide de contribution:
  - Comment forker et cloner
  - Workflow de développement
  - Code style guidelines
  - Comment soumettre un PR

- [ ] **CHANGELOG.md** - Historique des versions:
  ```markdown
  ## [1.0.0] - 2024-XX-XX
  ### Added
  - Initial release
  ```

- [ ] **Architecture.md** - Structure du projet et guide de navigation

- [ ] **Ajouter commentaires** dans le code:
  - Sections CSS complexes
  - Logique JavaScript spécifique
  - Sections non-évidentes

---

## 🎨 **9. Contenu & UX** (PRIORITÉ BASSE)

- [ ] **Pricing Tables** - Terminer la section pricing:
  - Structure HTML complète
  - Styling cohérent
  - Boutons d'action

- [ ] **Formulaire de contact** - Ajouter fonctionnalité:
  - Validation côté client
  - Backend/Email service (Formspree, Netlify Forms, etc)
  - Feedback utilisateur (success/error messages)

- [ ] **Valider tous les liens externes**
  - Tester les réseaux sociaux
  - Vérifier les URLs

- [ ] **Navigation mobile** - Tester complètement:
  - Menu hamburger
  - Responsive design
  - Touch interactions

- [ ] **Animations** - Optimiser:
  - Réduire si motion preference = reduce
  - Vérifier les performances
  - Utiliser GPU-accelerated properties

---

## 🔒 **10. Sécurité** (PRIORITÉ BASSE)

- [ ] **Content Security Policy (CSP)** - Headers:
  ```
  Content-Security-Policy: default-src 'self'; script-src 'self' 'unsafe-inline'
  ```

- [ ] **Audit des dépendances CDN**:
  - Vérifier vulnérabilités jQuery 1.8.3
  - Vérifier plugins jQuery
  - Considérer les alternatives modernes

- [ ] **CORS Configuration** - Si API externe utilisée

- [ ] **Vérifier les secrets** - Aucune clé API exposée

- [ ] **X-Frame-Options** - Prévention du clickjacking:
  ```
  X-Frame-Options: SAMEORIGIN
  ```

---

## 📊 Checklist Rapide

### Avant v1.1
- [ ] README.md + package.json
- [ ] .gitignore + .editorconfig
- [ ] Mettre à jour jQuery
- [ ] Minifier CSS
- [ ] Ajouter meta tags & SEO basiques

### Avant v1.2
- [ ] ARIA labels & accessibility
- [ ] Lazy loading images
- [ ] Refactoriser CSS (variables)
- [ ] Linting (Stylelint + HTMLHint)

### Version 2.0
- [ ] Build tool (Vite)
- [ ] GitHub Actions
- [ ] PWA/Service Worker
- [ ] Documented deployment

---

## 🔗 Ressources Utiles

- **SEO**: [Moz SEO Checklist](https://moz.com/)
- **Accessibility**: [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- **Performance**: [Lighthouse](https://developers.google.com/web/tools/lighthouse)
- **CSS**: [MDN CSS Guidelines](https://developer.mozilla.org/en-US/docs/Web/CSS)
- **HTML**: [MDN HTML Guidelines](https://developer.mozilla.org/en-US/docs/Web/HTML)

---

**Dernière mise à jour**: 2024-03-31
**Mainteneur**: Team Dev
