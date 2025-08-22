# Introduction au CSS - Notes de Cours

## Table des Matières

| Sujet | Description |
|-------|-------------|
| [1. Qu'est-ce que le CSS ?](#1-quest-ce-que-le-css) | Comprendre le CSS et son rôle dans le développement web |
| [2. Brève Histoire du CSS](#2-brève-histoire-du-css) | Évolution et versions du CSS |
| [3. Format du Sélecteur CSS](#3-format-du-sélecteur-css) | Syntaxe et structure de base |
| [4. CSS en Ligne](#4-css-en-ligne) | Stylisation directe dans les éléments HTML |
| [5. CSS Interne](#5-css-interne) | Stylisation dans le document HTML |
| [6. CSS Externe](#6-css-externe) | Liaison de fichiers CSS séparés |
| [Vocabulaire](#vocabulaire) | Termes et définitions clés |
| [Résumé](#résumé) | Points clés à retenir |
| [Ressources](#ressources) | Matériel d'apprentissage supplémentaire |

---

## 1. Qu'est-ce que le CSS ?

[⬆ Retour en Haut](#table-des-matières)

### Définition
**CSS** signifie **Feuilles de Style en Cascade** (Cascading Style Sheets). C'est un langage de stylisation utilisé pour décrire comment les éléments HTML doivent être affichés sur une page web.

### Objectif
Pensez au HTML comme le squelette d'une page web - il fournit la structure. Le CSS est comme les vêtements et le maquillage - il rend tout beau !

### La Relation Entre HTML et CSS

```
HTML = Structure (Quel contenu apparaît)
CSS = Présentation (Comment le contenu apparaît)
```

### Analogie Visuelle
Imaginez construire une maison :
- **HTML** = La charpente, les murs et les pièces (structure)
- **CSS** = La peinture, les décorations et les meubles (style)

### Pourquoi Utiliser le CSS ?
1. **Séparation des Préoccupations** : Garder la structure (HTML) séparée de la présentation (CSS)
2. **Réutilisabilité** : Une règle CSS peut styliser plusieurs éléments HTML
3. **Cohérence** : Maintenir une stylisation uniforme sur tout votre site web
4. **Efficacité** : Changer l'apparence de centaines de pages en éditant un fichier CSS

---

## 2. Brève Histoire du CSS

[⬆ Retour en Haut](#table-des-matières)

### Chronologie

| Année | Version | Caractéristiques Clés |
|------|---------|--------------|
| 1996 | CSS1 | Stylisation de base : polices, couleurs, espacement |
| 1998 | CSS2 | Positionnement, types de médias |
| 2011 | CSS3 | Animations, dégradés, ombres, design responsive |
| Présent | CSS3+ | Mises à jour modulaires continues |

### Avant le CSS
Dans les premiers jours du web, toute la stylisation était faite directement en HTML en utilisant des attributs comme :
```html
<font color="red">Ceci est du texte rouge</font>
```
Cela rendait les sites web difficiles à maintenir et à mettre à jour !

### Pourquoi le CSS a été Créé
- Pour résoudre le problème du mélange contenu/présentation
- Pour donner aux concepteurs web plus de contrôle sur la mise en page
- Pour réduire le code répétitif

---

## 3. Format du Sélecteur CSS

[⬆ Retour en Haut](#table-des-matières)

### Syntaxe CSS de Base

Chaque règle CSS se compose de deux parties principales :

```css
sélecteur {
    propriété: valeur;
}
```

### Composants Expliqués

1. **Sélecteur** : Quel(s) élément(s) HTML styliser
2. **Propriété** : Quel aspect changer (couleur, taille, etc.)
3. **Valeur** : En quoi le changer
4. **Déclaration** : Une paire propriété-valeur
5. **Bloc de Déclaration** : Tout ce qui est entre les accolades `{}`

### Diagramme Visuel

```
    sélecteur
       ↓
    h1 {
        color: blue;     ← déclaration
        ↑       ↑
    propriété valeur
        
        font-size: 24px; ← autre déclaration
    }
    ↑                 ↑
    accolade        accolade
    ouvrante        fermante
```

### Déclarations Multiples
Vous pouvez avoir plusieurs déclarations dans une règle :

```css
p {
    color: navy;
    font-size: 16px;
    line-height: 1.5;
}
```

### Commentaires en CSS
Utilisez `/* */` pour ajouter des commentaires :

```css
/* Ceci est un commentaire en CSS */
h1 {
    color: green; /* Ceci rend les titres verts */
}
```

---

## 4. CSS en Ligne

[⬆ Retour en Haut](#table-des-matières)

### Définition
Le CSS en ligne est du CSS écrit directement dans un élément HTML en utilisant l'attribut `style`.

### Syntaxe
```html
<balise style="propriété: valeur;">Contenu</balise>
```

### Exemples

#### Exemple 1 : Styliser un Paragraphe
```html
<p style="color: red;">Ce texte est rouge !</p>
```

#### Exemple 2 : Propriétés Multiples
```html
<h1 style="color: blue; font-size: 36px;">Grand Titre Bleu</h1>
```

#### Exemple 3 : Styliser Différents Éléments
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple de CSS en Ligne</title>
</head>
<body>
    <h1 style="color: purple;">Bienvenue !</h1>
    <p style="color: green; font-size: 18px;">Ceci est un paragraphe vert.</p>
    <p style="background-color: yellow;">Celui-ci a un fond jaune.</p>
</body>
</html>
```

### Propriétés Communes pour le CSS en Ligne

| Propriété | Description | Valeurs d'Exemple |
|----------|-------------|----------------|
| `color` | Couleur du texte | `red`, `#FF0000`, `rgb(255,0,0)` |
| `background-color` | Couleur de fond | `yellow`, `#FFFF00` |
| `font-size` | Taille du texte | `16px`, `1.5em`, `large` |
| `text-align` | Alignement du texte | `left`, `center`, `right` |
| `font-family` | Type de police | `Arial`, `"Times New Roman"` |

### Avantages et Inconvénients

**Avantages :**
- Rapide pour les tests
- Remplace les autres CSS (spécificité la plus élevée)
- Pas besoin de fichiers externes

**Inconvénients :**
- Non réutilisable
- Mélange présentation et contenu
- Difficile à maintenir
- Rend le HTML désordonné

---

## 5. CSS Interne

[⬆ Retour en Haut](#table-des-matières)

### Définition
Le CSS interne (aussi appelé CSS intégré) est écrit dans la section `<head>` d'un document HTML en utilisant la balise `<style>`.

### Syntaxe
```html
<head>
    <style>
        sélecteur {
            propriété: valeur;
        }
    </style>
</head>
```

### Exemple Complet
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple de CSS Interne</title>
    <style>
        h1 {
            color: navy;
            text-align: center;
        }
        
        p {
            color: gray;
            font-size: 16px;
            line-height: 1.6;
        }
        
        strong {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Bienvenue sur Mon Site Web</h1>
    <p>Ceci est un paragraphe avec du texte <strong>important</strong>.</p>
    <p>Tous les paragraphes auront le même style !</p>
</body>
</html>
```

### Sélecteurs d'Éléments
Sélectionnez les éléments HTML par leur nom de balise :

```css
h1 { color: blue; }
p { font-size: 14px; }
em { font-style: italic; }
strong { font-weight: bold; }
```

### Styliser Plusieurs Éléments
Appliquer le même style à plusieurs éléments :

```css
h1, h2, h3 {
    font-family: Arial;
    color: darkblue;
}
```

### Avantages et Inconvénients

**Avantages :**
- Les styles s'appliquent à toute la page
- Garde les styles séparés du contenu HTML
- Peut réutiliser les styles pour plusieurs éléments

**Inconvénients :**
- Fonctionne uniquement pour une page HTML
- Non réutilisable sur différentes pages
- Augmente la taille du fichier de la page

---

## 6. CSS Externe

[⬆ Retour en Haut](#table-des-matières)

### Définition
Le CSS externe est écrit dans un fichier `.css` séparé et lié aux documents HTML.

### Créer le Lien
Utilisez la balise `<link>` dans la section `<head>` :

```html
<link rel="stylesheet" href="styles.css">
```

### Exemple de Structure de Fichiers
```
mon-site-web/
│
├── index.html
├── about.html
├── contact.html
└── styles.css
```

### Fichier HTML (index.html)
```html
<!DOCTYPE html>
<html>
<head>
    <title>Mon Site Web</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenue sur Mon Site</h1>
    </header>
    <main>
        <section>
            <h2>À Propos de Nous</h2>
            <p>Nous créons des sites web incroyables !</p>
        </section>
    </main>
    <footer>
        <p>© 2024 Mon Site Web</p>
    </footer>
</body>
</html>
```

### Fichier CSS (styles.css)
```css
/* Réinitialiser les marges par défaut */
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

/* Styles de l'en-tête */
header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
}

/* Styles du contenu principal */
main {
    padding: 20px;
}

section {
    margin-bottom: 30px;
}

h2 {
    color: #333;
    border-bottom: 2px solid #333;
    padding-bottom: 5px;
}

/* Styles du pied de page */
footer {
    background-color: #f0f0f0;
    text-align: center;
    padding: 10px;
    color: #666;
}
```

### Lier le CSS depuis Différents Répertoires

#### CSS dans un sous-dossier :
```
mon-site-web/
│
├── index.html
└── css/
    └── styles.css
```

Lien : `<link rel="stylesheet" href="css/styles.css">`

#### CSS dans le dossier parent :
```
mon-site-web/
│
├── styles.css
└── pages/
    └── about.html
```

Lien depuis about.html : `<link rel="stylesheet" href="../styles.css">`

### Fichiers CSS Multiples
Vous pouvez lier plusieurs fichiers CSS :

```html
<link rel="stylesheet" href="css/reset.css">
<link rel="stylesheet" href="css/layout.css">
<link rel="stylesheet" href="css/colors.css">
```

### Avantages et Inconvénients

**Avantages :**
- Séparation complète du contenu et de la présentation
- Réutilisable sur plusieurs pages HTML
- Fichiers HTML plus petits
- Peut être mis en cache par les navigateurs (chargement plus rapide)
- Facile à maintenir et mettre à jour

**Inconvénients :**
- Nécessite une requête HTTP supplémentaire
- Peut causer un flash de contenu non stylisé (FOUC)

---

## Vocabulaire

[⬆ Retour en Haut](#table-des-matières)

| Terme | Définition |
|------|------------|
| **CSS** | Feuilles de Style en Cascade - langage pour styliser le HTML |
| **Sélecteur** | Identifie quels éléments HTML styliser |
| **Propriété** | L'aspect d'un élément que vous voulez changer |
| **Valeur** | Ce en quoi vous voulez changer la propriété |
| **Déclaration** | Une paire propriété-valeur (ex. `color: blue;`) |
| **Bloc de Déclaration** | Groupe de déclarations entre accolades |
| **CSS en Ligne** | CSS écrit directement dans les éléments HTML avec l'attribut `style` |
| **CSS Interne** | CSS écrit dans la balise `<style>` dans le `<head>` HTML |
| **CSS Externe** | CSS écrit dans des fichiers `.css` séparés |
| **Cascade** | L'ordre dans lequel les règles CSS sont appliquées |
| **Feuille de Style** | Une collection de règles CSS |
| **Balise Link** | Élément HTML utilisé pour connecter des fichiers CSS externes |
| **Spécificité** | Règles déterminant quelle règle CSS s'applique quand plusieurs règles ciblent le même élément |

---

## Résumé

[⬆ Retour en Haut](#table-des-matières)

### Points Clés à Retenir

1. **Le CSS rend les sites web beaux** - Il contrôle les couleurs, polices, espacement et mise en page
2. **Trois façons d'ajouter du CSS** :
   - **En ligne** : Rapide mais non réutilisable
   - **Interne** : Bon pour les pages uniques
   - **Externe** : Meilleur pour les sites multi-pages
3. **La syntaxe CSS est cohérente** : `sélecteur { propriété: valeur; }`
4. **Séparation des préoccupations** - Garder la structure (HTML) séparée du style (CSS)
5. **Le CSS externe est généralement le meilleur** pour les vrais sites web car il est :
   - Réutilisable sur plusieurs pages
   - Facile à maintenir
   - Garde le HTML propre

### Priorité CSS (Cascade)
Quand plusieurs règles CSS s'appliquent au même élément :
1. **CSS en ligne** (priorité la plus élevée)
2. **CSS interne**
3. **CSS externe** (priorité la plus basse)

### Meilleures Pratiques
- Commencez avec du CSS externe pour la cohérence
- Utilisez du CSS interne pour les styles spécifiques à une page
- Utilisez du CSS en ligne avec parcimonie (tests ou remplacements uniquement)
- Gardez votre CSS organisé avec des commentaires
- Utilisez des noms significatifs pour vos fichiers CSS

---

## Ressources

[⬆ Retour en Haut](#table-des-matières)

### Documentation
- [Documentation CSS MDN](https://developer.mozilla.org/fr/docs/Web/CSS)
- [Tutoriel CSS W3Schools](https://www.w3schools.com/css/)
- [Référence CSS](https://developer.mozilla.org/fr/docs/Web/CSS/Reference)

### Référence des Propriétés CSS
- [Propriétés CSS W3Schools](https://www.w3schools.com/cssref/)
- [Index des Propriétés CSS MDN](https://developer.mozilla.org/fr/docs/Web/CSS/CSS_Properties_Reference)

### Outils
- **WebStorm** : Votre IDE pour écrire HTML et CSS
- **Git** : Contrôle de version pour suivre les changements
- **GitHub** : Héberger et partager votre code

### Ressources de Pratique
- [Exercices CSS W3Schools](https://www.w3schools.com/css/exercise.asp)
- [Bases CSS sur MDN](https://developer.mozilla.org/fr/docs/Learn/Getting_started_with_the_web/CSS_basics)

### Prochaines Étapes
Après avoir maîtrisé ces bases, vous apprendrez :
- Les sélecteurs de classe et d'ID
- Le modèle de boîte
- Les mises en page Flexbox et Grid
- Le design responsive
- Les animations CSS

---

*Rappelez-vous : La meilleure façon d'apprendre le CSS est de pratiquer ! Commencez avec des styles simples et ajoutez progressivement plus de complexité au fur et à mesure que vous devenez à l'aise.*