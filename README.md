# OhMyFood

OhMyFood est une plateforme de réservation de menu de restaurants en ligne, développée dans le cadre d'un projet de formation. Le site permet aux utilisateurs de découvrir des restaurants d'exception et de consulter leurs menus de manière interactive et moderne.

🌐 **[Voir le site en ligne](https://mavaki64.github.io/OhMyFood/)**

## 🎯 Fonctionnalités

### Page d'accueil
- **Loader animé** : Animation de chargement avec spinner et texte animé
- **Section Hero** : Présentation du concept avec call-to-action
- **Fonctionnement** : Guide en 3 étapes pour utiliser le service
- **Restaurants** : Liste des restaurants disponibles avec images et badges "Nouveau"
- **Cœurs animés** : Animation de remplissage au clic sur les favoris (sans JavaScript)

### Pages de menus
- **4 restaurants** disponibles :
  - À la française
  - La palette du goût
  - La note enchantée
  - Le délice des sens
- **Cartes de menu interactives** :
  - Animation de glissement au clic pour sélectionner un plat
  - Troncature automatique du texte avec ellipsis
  - Prix affiché dynamiquement
- **Animation d'apparition** : Les catégories (Entrées, Plats, Desserts) apparaissent progressivement
- **Bouton de retour** : Navigation vers la page d'accueil

## 🛠️ Technologies utilisées

- **HTML5** : Structure sémantique et accessible
- **SCSS/SASS** : Préprocesseur CSS avec architecture 7-1
- **CSS3** : Animations, transitions, Flexbox, Grid
- **Font Awesome** : Icônes
- **Google Fonts** : Roboto et Shrikhand

## 📁 Structure du projet

```
OhMyFood/
├── assets/
│   ├── css/
│   │   ├── style.css          # CSS compilé
│   │   └── style.css.map      # Source map
│   └── images/
│       ├── logo/
│       └── restaurants/
├── restaurants/               # Pages de menus
│   ├── a-la-francaise.html
│   ├── la-palette-du-gout.html
│   ├── la-note-enchantee.html
│   └── le-delice-des-sens.html
├── scss/
│   ├── abstracts/            # Variables, mixins, fonctions, placeholders
│   ├── base/                 # Styles de base et typographie
│   ├── components/           # Boutons, cartes
│   ├── layout/               # Header, footer, loader
│   ├── pages/                # Styles spécifiques aux pages
│   └── style.scss            # Fichier principal
├── index.html                # Page d'accueil
└── README.md
```

## 🎨 Architecture SCSS (7-1)

Le projet suit l'architecture **7-1** pour une organisation modulaire et maintenable :

- **Abstracts** : Variables, mixins, fonctions, placeholders
- **Base** : Reset, typographie, styles de base
- **Components** : Composants réutilisables (boutons, cartes)
- **Layout** : Structure de la page (header, footer, loader)
- **Pages** : Styles spécifiques aux pages
- **Themes** : Thème de couleur
- **Vendors** : Librairies

## 🎭 Animations et interactions

### Loader
- Animation de spinner rotatif
- Texte "Chargement" avec points animés
- Désactivation du scroll pendant le chargement

### Cartes de menu
- **Glissement** : Animation de slide depuis la droite au clic
- **Sélection** : Icône de validation apparaît avec animation fluide
- **Texte** : Troncature automatique avec ellipsis pour les titres longs

### Cœurs (favoris)
- Animation de remplissage au clic
- Dégradé violet/rose animé
- Persistance de l'état sans JavaScript (checkbox CSS)

### Catégories de menu
- Apparition progressive avec délai entre chaque catégorie
- Animation fade-in + slide-up

## 📱 Responsive Design

Le site est développé avec une approche **mobile-first** :

- **Mobile** : < 768px (design principal)
- **Tablette** : ≥ 768px et < 1024px
- **Desktop** : ≥ 1024px

### Breakpoints
```scss
$breakpoint-tablet: 768px;
$breakpoint-desktop: 1024px;
```

## 🎯 Méthodologie BEM

Le projet utilise la méthodologie **BEM** (Block Element Modifier) pour la nomenclature CSS :

```scss
.block {}                    // Bloc
.block__element {}           // Élément
.block--modifier {}          // Modificateur
```

### Exemples
- `.menu-card` : Bloc
- `.menu-card__title` : Élément
- `.btn--primary` : Modificateur

## 🚀 Installation et utilisation

### Prérequis
- Un compilateur SCSS (Sass, Dart Sass, ou un outil comme Live Sass Compiler)

### Compilation SCSS
```bash
# Avec Sass
sass scss/style.scss assets/css/style.css --watch

# Ou avec npm/yarn
npm install -g sass
sass scss/style.scss assets/css/style.css
```

### Ouverture du projet
1. Ouvrir `index.html` dans un navigateur
2. Pour les pages de menus, ouvrir les fichiers dans `restaurants/`

## 📝 Notes de développement

- **Aucun JavaScript** : Toutes les interactions sont gérées en CSS pur
- **Performance** : Utilisation de `transform` et `opacity` pour des animations fluides
- **Maintenabilité** : Code modulaire et bien organisé avec SCSS
- **DRY** : Utilisation de mixins, variables et placeholders pour éviter la répétition

## 👤 Auteur

**Killian GAYEZ**

Projet réalisé dans le cadre de la formation "Intégrateur Web" - Projet 4 : Amélioration de l'interface d'un site mobile avec des animations CSS

## 📄 Licence

Ce projet est un projet de formation et est fourni à des fins éducatives.
```

Ce README couvre :
- Description du projet
- Fonctionnalités principales
- Technologies utilisées
- Structure du projet
- Architecture SCSS
- Animations et interactions
- Responsive design
- Méthodologie BEM
- Instructions d'installation
- Notes de développement
