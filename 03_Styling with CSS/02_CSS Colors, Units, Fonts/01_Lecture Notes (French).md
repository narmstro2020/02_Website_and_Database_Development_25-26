# Couleurs, Unités et Polices CSS - Notes de Cours

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

## Table des Matières

| Sujet | Description |
|-------|-------------|
| [Introduction](#introduction) | Aperçu des couleurs, unités et polices CSS |
| [Couleurs CSS](#couleurs-css) | RGB, RGBA, HSL, HSLA, Hexadécimal et Couleurs Nommées |
| [Unités CSS](#unités-css) | Unités Absolues et Relatives |
| [Polices CSS](#polices-css) | Propriétés de Police et Typographie Web |
| [Vocabulaire](#vocabulaire) | Termes clés et définitions |
| [Devoirs](#devoirs) | Exercices pratiques |
| [Résumé](#résumé) | Points clés à retenir |
| [Ressources](#ressources) | Matériel d'apprentissage supplémentaire |

---

## Introduction

Dans cette leçon, nous explorerons trois aspects fondamentaux du style CSS qui transformeront vos pages web de texte simple en designs visuellement attrayants. Vous apprendrez comment ajouter des couleurs, contrôler les dimensions avec différentes unités et styliser le texte avec diverses propriétés de police.

### Prérequis
- Structure de document HTML (DOCTYPE, html, head, body)
- Balises HTML de base (h1-h6, p, em, strong)
- HTML sémantique (header, footer, main, section, article)
- Listes (ul, ol, li)
- Liens et images
- Syntaxe CSS de base et sélecteurs des leçons précédentes

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

---

## Couleurs CSS

CSS offre plusieurs façons de spécifier les couleurs. Chaque méthode a ses avantages et cas d'utilisation.

### 1. Couleurs Nommées

CSS prend en charge 140 noms de couleurs standard que vous pouvez utiliser directement.

```css
/* Utilisation des couleurs nommées */
p {
    color: red;
    background-color: lightblue;
}

h1 {
    color: darkgreen;
    background-color: gold;
}
```

**Couleurs Nommées Courantes :**
- Primaires : red, blue, green, yellow
- Neutres : black, white, gray, silver
- Étendues : coral, salmon, turquoise, violet

### 2. Couleurs Hexadécimales

Les couleurs hexadécimales (hex) utilisent un # suivi de 6 caractères (0-9 et A-F).

```css
/* Format de couleur hexadécimale : #RRVVBB */
p {
    color: #FF0000;      /* Rouge pur */
    background-color: #00FF00;  /* Vert pur */
}

h1 {
    color: #0000FF;      /* Bleu pur */
    background-color: #FFFFFF;  /* Blanc */
}

/* Hex abrégé (quand les paires correspondent) */
h2 {
    color: #F00;        /* Identique à #FF0000 */
    background-color: #0F0;     /* Identique à #00FF00 */
}
```

**Comprendre les Couleurs Hex :**
- Deux premiers caractères : Valeur rouge (00-FF)
- Deux caractères du milieu : Valeur verte (00-FF)
- Deux derniers caractères : Valeur bleue (00-FF)
- 00 = pas de couleur, FF = couleur maximale

### 3. Couleurs RGB

RGB utilise des valeurs décimales de 0-255 pour Rouge, Vert et Bleu.

```css
/* Format de couleur RGB : rgb(rouge, vert, bleu) */
p {
    color: rgb(255, 0, 0);      /* Rouge pur */
    background-color: rgb(0, 255, 0);   /* Vert pur */
}

h1 {
    color: rgb(0, 0, 255);      /* Bleu pur */
    background-color: rgb(128, 128, 128); /* Gris */
}

/* Mélange de couleurs */
h2 {
    color: rgb(255, 165, 0);    /* Orange */
    background-color: rgb(128, 0, 128);  /* Violet */
}
```

### 4. Couleurs RGBA

RGBA ajoute un canal alpha pour la transparence (0 = entièrement transparent, 1 = entièrement opaque).

```css
/* Format RGBA : rgba(rouge, vert, bleu, alpha) */
p {
    background-color: rgba(255, 0, 0, 0.5);   /* Rouge transparent à 50% */
}

section {
    background-color: rgba(0, 0, 255, 0.3);   /* Bleu opaque à 30% */
}

/* Superposition avec transparence */
header {
    background-color: rgba(0, 0, 0, 0.8);     /* Noir opaque à 80% */
    color: rgba(255, 255, 255, 1);            /* Blanc entièrement opaque */
}
```

### 5. Couleurs HSL

HSL signifie Teinte, Saturation et Luminosité - un modèle de couleur plus intuitif.

```css
/* Format HSL : hsl(teinte, saturation%, luminosité%) */
p {
    color: hsl(0, 100%, 50%);      /* Rouge */
    background-color: hsl(120, 100%, 50%);  /* Vert */
}

h1 {
    color: hsl(240, 100%, 50%);    /* Bleu */
}

/* Création de variations de couleur */
section {
    background-color: hsl(200, 50%, 70%);   /* Bleu clair */
}
```

**Comprendre HSL :**
- Teinte : 0-360 degrés sur la roue chromatique (0=rouge, 120=vert, 240=bleu)
- Saturation : 0% = gris, 100% = couleur complète
- Luminosité : 0% = noir, 50% = normal, 100% = blanc

### 6. Couleurs HSLA

HSLA ajoute la transparence aux couleurs HSL.

```css
/* Format HSLA : hsla(teinte, saturation%, luminosité%, alpha) */
article {
    background-color: hsla(60, 100%, 50%, 0.5);  /* Jaune transparent à 50% */
}

footer {
    background-color: hsla(0, 0%, 0%, 0.9);      /* Noir opaque à 90% */
}
```

### Guide Visuel des Couleurs

```css
/* Exemple complet de couleurs */
body {
    background-color: #f0f0f0;  /* Fond gris clair */
}

header {
    background-color: rgb(51, 51, 51);  /* Gris foncé */
    color: white;
}

main {
    background-color: rgba(255, 255, 255, 0.95);  /* Blanc légèrement transparent */
}

footer {
    background-color: hsl(210, 50%, 30%);  /* Bleu foncé */
    color: hsla(0, 0%, 100%, 0.9);  /* Blanc légèrement transparent */
}
```

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

---

## Unités CSS

Les unités CSS déterminent la taille des éléments. Elles se divisent en deux catégories : absolues et relatives.

### Unités Absolues

Les unités absolues ont une taille fixe indépendamment des autres paramètres.

#### Pixels (px)
Unité absolue la plus courante pour l'affichage à l'écran.

```css
p {
    font-size: 16px;
    margin: 20px;
    padding: 10px;
}

h1 {
    font-size: 32px;
    margin-bottom: 24px;
}

img {
    width: 300px;
    height: 200px;
}
```

#### Autres Unités Absolues
Moins couramment utilisées mais disponibles :

```css
/* Unités absolues rarement utilisées */
p {
    margin: 0.5in;    /* pouces */
    padding: 1cm;     /* centimètres */
    border: 2mm;      /* millimètres */
    width: 12pt;      /* points (1pt = 1/72 pouce) */
    height: 1pc;      /* picas (1pc = 12pt) */
}
```

### Unités Relatives

Les unités relatives s'adaptent en fonction d'autres valeurs, rendant les designs plus flexibles.

#### Pourcentages (%)
Relatif à la taille de l'élément parent.

```css
/* Unités en pourcentage */
section {
    width: 80%;           /* 80% de la largeur du parent */
    margin: 0 auto;       /* Centre la section */
}

article {
    width: 50%;           /* Moitié de la largeur du parent */
    padding: 5%;          /* 5% de la largeur du parent */
}

img {
    width: 100%;          /* Largeur complète du conteneur */
    height: auto;         /* Maintenir le ratio d'aspect */
}
```

#### Unités Em (em)
Relatif à la taille de police de l'élément (ou la taille de police du parent pour d'autres propriétés).

```css
/* Unités em */
p {
    font-size: 1em;       /* Identique à la taille de police du parent */
    margin: 1.5em;        /* 1,5 fois la taille de police */
    padding: 0.5em;       /* Moitié de la taille de police */
}

h1 {
    font-size: 2em;       /* Deux fois la taille de police du parent */
    margin-bottom: 0.5em; /* Moitié de la taille de police de h1 */
}

/* Valeurs em en cascade */
body {
    font-size: 16px;
}

article {
    font-size: 1.2em;     /* 19.2px (16px × 1.2) */
}

article p {
    font-size: 1.1em;     /* 21.12px (19.2px × 1.1) */
}
```

#### Unités Rem (rem)
Relatif à la taille de police de l'élément racine (généralement html).

```css
/* Unités rem - plus prévisibles que em */
html {
    font-size: 16px;      /* Taille de base */
}

p {
    font-size: 1rem;      /* 16px */
    margin: 1.5rem;       /* 24px */
}

h1 {
    font-size: 2.5rem;    /* 40px */
    margin-bottom: 1rem;  /* 16px */
}

h2 {
    font-size: 2rem;      /* 32px */
}
```

#### Unités de Viewport
Relatif à la taille du viewport du navigateur.

```css
/* Unités de viewport */
header {
    width: 100vw;         /* 100% de la largeur du viewport */
    height: 10vh;         /* 10% de la hauteur du viewport */
}

h1 {
    font-size: 5vw;       /* 5% de la largeur du viewport */
}

section {
    min-height: 100vh;    /* Hauteur minimale du viewport complet */
    padding: 5vw;         /* Padding responsive */
}

/* vmin et vmax */
article {
    width: 80vmin;        /* 80% de la plus petite dimension du viewport */
    font-size: 2vmax;     /* 2% de la plus grande dimension du viewport */
}
```

### Choisir la Bonne Unité

```css
/* Meilleures pratiques pour différents cas d'utilisation */

/* Tailles fixes - utiliser px */
img {
    border: 2px solid black;
}

/* Typographie - utiliser rem pour la cohérence */
body {
    font-size: 1rem;
}

h1 {
    font-size: 2.5rem;
}

/* Mises en page - utiliser % ou unités de viewport */
main {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

/* Espacement - utiliser em ou rem */
p {
    margin-bottom: 1em;
    padding: 1rem;
}
```

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

---

## Polices CSS

La typographie est cruciale pour le design web. CSS offre un contrôle étendu sur l'apparence du texte.

### Famille de Police

Spécifie quelle police utiliser. Toujours fournir des polices de secours.

```css
/* Famille de police avec polices de secours */
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1 {
    font-family: Georgia, 'Times New Roman', serif;
}

p {
    font-family: 'Courier New', Courier, monospace;
}

/* Utilisation de guillemets pour les noms de police avec espaces */
article {
    font-family: 'Segoe UI', Tahoma, sans-serif;
}
```

#### Familles de Polices Génériques
Toujours terminer par une famille générique comme ultime recours :
- **serif** : Times New Roman, Georgia (traits décoratifs)
- **sans-serif** : Arial, Helvetica (sans traits décoratifs)
- **monospace** : Courier New, Consolas (largeur de caractère égale)
- **cursive** : Comic Sans MS (style manuscrit)
- **fantasy** : Impact (décoratif)

### Taille de Police

Contrôle la taille du texte en utilisant n'importe quelle unité CSS.

```css
/* Différentes unités de taille de police */
p {
    font-size: 16px;      /* Taille absolue */
}

h1 {
    font-size: 2.5rem;    /* Relatif à la racine */
}

h2 {
    font-size: 2em;       /* Relatif au parent */
}

/* Tailles par mots-clés */
small {
    font-size: small;     /* Taille prédéfinie */
}

h3 {
    font-size: larger;    /* Mot-clé relatif */
}
```

### Graisse de Police

Contrôle l'épaisseur des caractères.

```css
/* Valeurs de graisse de police */
p {
    font-weight: normal;  /* Identique à 400 */
}

strong {
    font-weight: bold;    /* Identique à 700 */
}

h1 {
    font-weight: 900;     /* Extra gras */
}

h2 {
    font-weight: 300;     /* Léger */
}

/* Valeurs numériques : 100-900 */
h3 {
    font-weight: 600;     /* Semi-gras */
}
```

### Style de Police

Contrôle le texte italique ou oblique.

```css
/* Options de style de police */
p {
    font-style: normal;
}

em {
    font-style: italic;
}

footer {
    font-style: oblique;  /* Texte incliné */
}
```

### Décoration de Texte

Ajoute des lignes au texte.

```css
/* Décoration de texte */
a {
    text-decoration: underline;
}

h1 {
    text-decoration: none;
}

/* Décorations multiples */
h2 {
    text-decoration: underline overline;
}

/* Styles de décoration */
p {
    text-decoration: underline wavy red;
}
```

### Transformation de Texte

Change la capitalisation du texte.

```css
/* Transformation de texte */
h1 {
    text-transform: uppercase;   /* TOUT EN MAJUSCULES */
}

h2 {
    text-transform: lowercase;   /* tout en minuscules */
}

h3 {
    text-transform: capitalize;  /* Première Lettre De Chaque Mot */
}

p {
    text-transform: none;        /* Texte normal */
}
```

### Hauteur de Ligne

Contrôle l'espacement entre les lignes de texte.

```css
/* Hauteur de ligne */
p {
    line-height: 1.5;     /* 1,5 fois la taille de police */
}

body {
    line-height: 1.6;     /* Bon pour la lisibilité */
}

h1 {
    line-height: 1.2;     /* Plus serré pour les titres */
}

/* Utilisation d'unités */
article {
    line-height: 24px;    /* Hauteur fixe */
}
```

### Espacement des Lettres et des Mots

Contrôle l'espace entre les lettres et les mots.

```css
/* Espacement des lettres */
h1 {
    letter-spacing: 2px;
}

p {
    letter-spacing: 0.5px;
}

/* Espacement des mots */
p {
    word-spacing: 5px;
}

h2 {
    word-spacing: -2px;  /* Négatif rapproche les mots */
}
```

### Alignement du Texte

Contrôle l'alignement horizontal du texte.

```css
/* Alignement du texte */
h1 {
    text-align: center;
}

p {
    text-align: left;     /* Par défaut pour les langues LTR */
}

footer {
    text-align: right;
}

article {
    text-align: justify;  /* Étire les lignes à la largeur complète */
}
```

### Exemple Complet de Police

```css
/* Style de police complet */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 16px;
    line-height: 1.6;
    color: #333333;
}

h1 {
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 2.5rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
    text-align: center;
    color: #2c3e50;
    line-height: 1.2;
}

h2 {
    font-family: inherit;  /* Hérite du parent */
    font-size: 2rem;
    font-weight: 600;
    color: #34495e;
    margin-bottom: 1rem;
}

p {
    font-size: 1rem;
    line-height: 1.8;
    text-align: justify;
    margin-bottom: 1em;
}

em {
    font-style: italic;
    color: #e74c3c;
}

strong {
    font-weight: bold;
    color: #c0392b;
}

a {
    color: #3498db;
    text-decoration: none;
    font-weight: 500;
}

/* Effet de survol pour les liens */
a:hover {
    text-decoration: underline;
    color: #2980b9;
}
```

### Polices Web

Bien que n'utilisant pas de services externes, vous pouvez utiliser les polices système de manière créative :

```css
/* Piles de polices système pour différents systèmes d'exploitation */
body {
    /* Polices système modernes */
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 
                 Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 
                 'Helvetica Neue', sans-serif;
}

/* Polices système monospace */
pre {
    font-family: 'SF Mono', Monaco, 'Cascadia Code', 
                 'Roboto Mono', Consolas, 'Courier New', 
                 monospace;
}
```

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

---

## Vocabulaire

### Termes de Couleur
- **RGB** : Modèle de couleur Rouge, Vert, Bleu utilisant des valeurs 0-255
- **RGBA** : RGB avec canal Alpha (transparence)
- **HSL** : Modèle de couleur Teinte, Saturation, Luminosité
- **HSLA** : HSL avec canal Alpha
- **Hexadécimal** : Système de numération en base 16 utilisant 0-9 et A-F
- **Canal Alpha** : Contrôle la transparence (0 = transparent, 1 = opaque)
- **Teinte** : La couleur elle-même sur une roue chromatique de 360 degrés
- **Saturation** : Intensité de la couleur (0% = gris, 100% = vif)
- **Luminosité** : Clarté ou obscurité de la couleur

### Termes d'Unité
- **Unités Absolues** : Mesures fixes (px, in, cm, mm, pt, pc)
- **Unités Relatives** : Mesures relatives à autre chose (%, em, rem, vw, vh)
- **Pixel (px)** : Point unique sur un écran
- **Em (em)** : Relatif à la taille de police de l'élément
- **Rem (rem)** : Relatif à la taille de police de l'élément racine
- **Viewport** : Zone visible d'une page web
- **Largeur du Viewport (vw)** : 1% de la largeur du viewport
- **Hauteur du Viewport (vh)** : 1% de la hauteur du viewport

### Termes de Police
- **Famille de Police** : La police à utiliser
- **Graisse de Police** : Épaisseur des caractères (100-900)
- **Style de Police** : Normal, italique ou oblique
- **Hauteur de Ligne** : Espace entre les lignes de texte
- **Espacement des Lettres** : Espace entre les caractères
- **Espacement des Mots** : Espace entre les mots
- **Transformation de Texte** : Contrôle de la capitalisation
- **Décoration de Texte** : Lignes ajoutées au texte (souligné, surligné, barré)
- **Serif** : Polices avec traits décoratifs
- **Sans-serif** : Polices sans traits décoratifs
- **Monospace** : Polices où tous les caractères ont une largeur égale
- **Polices de Secours** : Polices alternatives si le premier choix n'est pas disponible

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

---

## Devoirs

### Devoir 1 : Créateur de Palette de Couleurs
Créez une page web qui démontre tous les formats de couleur en construisant une vitrine de palette de couleurs.
[Voir Devoir 1](assignment1.md)

### Devoir 2 : Typographie Responsive
Construisez une page spécimen de typographie utilisant diverses propriétés de police et unités.
[Voir Devoir 2](assignment2.md)

### Devoir 3 : Guide de Style Complet
Créez un guide de style complet combinant couleurs, unités et polices.
[Voir Devoir 3](assignment3.md)

### Solutions
- [Solution Devoir 1](assignment1-solution.md)
- [Solution Devoir 2](assignment2-solution.md)
- [Solution Devoir 3](assignment3-solution.md)

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

---

## Résumé

### Points Clés à Retenir

1. **Couleurs CSS**
   - Plusieurs formats disponibles : nommées, hex, RGB, RGBA, HSL, HSLA
   - Utilisez RGBA/HSLA pour les effets de transparence
   - HSL est intuitif pour créer des variations de couleur
   - Toujours considérer le contraste pour l'accessibilité

2. **Unités CSS**
   - Unités absolues (px) pour les tailles fixes
   - Unités relatives (%, em, rem) pour les designs flexibles
   - Unités de viewport (vw, vh) pour les mises en page responsives
   - Choisir les unités selon le contexte et les besoins

3. **Polices CSS**
   - Toujours fournir des polices de secours
   - Utiliser rem pour un dimensionnement cohérent
   - Combiner les propriétés pour un contrôle typographique complet
   - Considérer la lisibilité avec une hauteur de ligne appropriée

### Meilleures Pratiques
- Utiliser des noms de couleur sémantiques dans votre CSS pour la maintenabilité
- Préférer rem à em pour un dimensionnement plus prévisible
- Toujours inclure des familles de polices génériques comme secours
- Tester vos designs à différentes tailles d'écran
- Maintenir de bons ratios de contraste pour l'accessibilité

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)

---

## Ressources

### Documentation
- [MDN Couleurs CSS](https://developer.mozilla.org/fr/docs/Web/CSS/color)
- [MDN Unités CSS](https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Values_and_units)
- [MDN Polices CSS](https://developer.mozilla.org/fr/docs/Web/CSS/font)

### Références W3Schools
- [W3Schools Couleurs CSS](https://www.w3schools.com/css/css_colors.asp)
- [W3Schools Unités CSS](https://www.w3schools.com/css/css_units.asp)
- [W3Schools Polices CSS](https://www.w3schools.com/css/css_font.asp)

### Outils
- IDE WebStorm pour l'édition de code
- Git pour le contrôle de version
- GitHub pour le dépôt de code

### Outils de Couleur
- Sélecteur de couleurs des DevTools du navigateur
- Utilitaires de sélection de couleurs système

[Retour en haut](#couleurs-unités-et-polices-css---notes-de-cours)