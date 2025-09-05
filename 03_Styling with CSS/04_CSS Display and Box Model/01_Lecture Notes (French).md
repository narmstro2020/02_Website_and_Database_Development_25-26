# Propriétés d'Affichage CSS et le Modèle de Boîte CSS

## Table des Matières

| Sujet | Description |
|-------|-------------|
| [Introduction](#introduction) | Aperçu des propriétés d'affichage et du modèle de boîte |
| [Vocabulaire](#vocabulaire) | Termes clés et définitions |
| [Propriétés d'Affichage CSS](#propriétés-daffichage-css) | Comprendre block, inline, inline-block et none |
| [Le Modèle de Boîte CSS](#le-modèle-de-boîte-css) | Margin, padding, border et content |
| [Exemples Visuels](#exemples-visuels) | Démonstrations interactives |
| [Résumé](#résumé) | Points clés |
| [Ressources](#ressources) | Matériel d'apprentissage supplémentaire |

---

## Introduction

Bienvenue à notre leçon sur les Propriétés d'Affichage CSS et le Modèle de Boîte CSS ! Ce sont des concepts fondamentaux qui contrôlent comment les éléments apparaissent et occupent l'espace sur une page web. À la fin de cette leçon, vous comprendrez comment contrôler la mise en page et l'espacement des éléments comme un développeur web professionnel.

### Ce que Vous Apprendrez
- Comment différentes propriétés d'affichage affectent le comportement des éléments
- Les composants du Modèle de Boîte CSS
- Comment contrôler l'espacement à l'intérieur et à l'extérieur des éléments
- Techniques pratiques pour créer des mises en page

[↑ Retour au Début](#table-des-matières)

---

## Vocabulaire

### Termes des Propriétés d'Affichage
- **Propriété Display** : Propriété CSS qui détermine comment un élément est affiché dans le flux du document
- **Élément Block** : Un élément qui commence sur une nouvelle ligne et prend toute la largeur disponible
- **Élément Inline** : Un élément qui s'intègre dans le texte et ne prend que la largeur nécessaire
- **Élément Inline-Block** : Combine les caractéristiques des éléments inline et block
- **Flux du Document** : L'ordre dans lequel les éléments apparaissent dans le HTML et comment ils s'empilent sur la page

### Termes du Modèle de Boîte
- **Content** : Le contenu réel de l'élément (texte, images, etc.)
- **Padding** : Espace entre le contenu et la bordure
- **Border** : Une ligne qui entoure le padding et le contenu
- **Margin** : Espace à l'extérieur de la bordure qui sépare l'élément des autres éléments
- **Outline** : Une ligne dessinée à l'extérieur de la bordure qui n'affecte pas la mise en page
- **Box-Sizing** : Propriété qui détermine comment la largeur et la hauteur sont calculées

[↑ Retour au Début](#table-des-matières)

---

## Propriétés d'Affichage CSS

### Comprendre les Types d'Affichage

La propriété `display` est l'une des propriétés CSS les plus importantes pour contrôler la mise en page. Elle détermine comment un élément se comporte dans le flux du document.

### 1. Éléments Block (`display: block`)

Les éléments block sont comme des paragraphes dans un livre - ils commencent sur une nouvelle ligne et s'étendent sur toute la largeur disponible.

**Caractéristiques :**
- Commencent sur une nouvelle ligne
- Prennent toute la largeur disponible
- Peuvent avoir largeur et hauteur définies
- Respectent toutes les valeurs de margin et padding

**Éléments Block par Défaut :**
- `<div>`, `<p>`, `<h1>` à `<h6>`
- `<header>`, `<footer>`, `<main>`, `<section>`, `<article>`
- `<ul>`, `<ol>`, `<li>`

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple d'Éléments Block</title>
    <style>
        .block-example {
            display: block;
            background-color: lightblue;
            padding: 10px;
            margin: 10px 0;
            border: 2px solid darkblue;
        }
    </style>
</head>
<body>
    <div class="block-example">Je suis un élément block</div>
    <div class="block-example">Je commence sur une nouvelle ligne</div>
    <p class="block-example">Les paragraphes sont des blocks par défaut</p>
</body>
</html>
```

### 2. Éléments Inline (`display: inline`)

Les éléments inline sont comme des mots dans une phrase - ils s'intègrent dans le texte et ne prennent que l'espace nécessaire.

**Caractéristiques :**
- Ne commencent pas sur une nouvelle ligne
- Ne prennent que la largeur nécessaire
- Ne peuvent pas avoir largeur et hauteur définies
- Les margin et padding verticaux n'affectent pas les éléments environnants
- Les margin et padding horizontaux fonctionnent normalement

**Éléments Inline par Défaut :**
- `<span>`, `<a>`, `<strong>`, `<em>`
- `<img>` (cas spécial - accepte largeur/hauteur)

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple d'Éléments Inline</title>
    <style>
        .inline-example {
            display: inline;
            background-color: yellow;
            padding: 5px;
            margin: 5px;
            border: 1px solid orange;
        }
    </style>
</head>
<body>
    <p>
        Ceci est un paragraphe avec des 
        <span class="inline-example">éléments</span> 
        inline qui 
        <span class="inline-example">s'intègrent</span> 
        dans le texte.
    </p>
</body>
</html>
```

### 3. Éléments Inline-Block (`display: inline-block`)

Les éléments inline-block combinent le meilleur des deux mondes - ils s'intègrent comme des éléments inline mais acceptent les dimensions comme les éléments block.

**Caractéristiques :**
- S'intègrent dans le texte comme les éléments inline
- Acceptent largeur et hauteur comme les éléments block
- Respectent toutes les valeurs de margin et padding
- Ne forcent pas un saut de ligne

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple Inline-Block</title>
    <style>
        .inline-block-example {
            display: inline-block;
            width: 100px;
            height: 100px;
            background-color: lightgreen;
            margin: 10px;
            padding: 10px;
            border: 2px solid darkgreen;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="inline-block-example">Boîte 1</div>
    <div class="inline-block-example">Boîte 2</div>
    <div class="inline-block-example">Boîte 3</div>
</body>
</html>
```

### 4. None (`display: none`)

Les éléments avec `display: none` sont complètement supprimés du flux du document.

**Caractéristiques :**
- L'élément n'est pas visible
- Ne prend aucun espace sur la page
- Différent de `visibility: hidden` (qui cache mais préserve l'espace)

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple Display None</title>
    <style>
        .hidden {
            display: none;
        }
        .visible {
            background-color: lightcoral;
            padding: 10px;
            margin: 5px;
        }
    </style>
</head>
<body>
    <div class="visible">Je suis visible</div>
    <div class="hidden">Je suis complètement caché et ne prends aucun espace</div>
    <div class="visible">J'apparais juste après le premier div</div>
</body>
</html>
```

[↑ Retour au Début](#table-des-matières)

---

## Le Modèle de Boîte CSS

Chaque élément HTML est essentiellement une boîte rectangulaire. Le Modèle de Boîte CSS décrit comment ces boîtes sont structurées et comment leurs dimensions sont calculées.

### Composants du Modèle de Boîte (de l'intérieur vers l'extérieur)

1. **Content** : Le contenu réel de l'élément
2. **Padding** : Espace entre le contenu et la bordure
3. **Border** : Le bord de la boîte de l'élément
4. **Margin** : Espace à l'extérieur de la bordure

### Représentation Visuelle

```
+------------------------------------------+
|              MARGIN (transparent)        |
|  +------------------------------------+  |
|  |          BORDER                    |  |
|  |  +------------------------------+  |  |
|  |  |        PADDING               |  |  |
|  |  |  +------------------------+  |  |  |
|  |  |  |                        |  |  |  |
|  |  |  |       CONTENT          |  |  |  |
|  |  |  |                        |  |  |  |
|  |  |  +------------------------+  |  |  |
|  |  |                              |  |  |
|  |  +------------------------------+  |  |
|  |                                    |  |
|  +------------------------------------+  |
|                                          |
+------------------------------------------+
```

### 1. Zone de Contenu

La zone de contenu contient le contenu réel - texte, images ou autres éléments.

**Propriétés :**
- `width` : Définit la largeur de la zone de contenu
- `height` : Définit la hauteur de la zone de contenu

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple de Zone de Contenu</title>
    <style>
        .content-box {
            width: 200px;
            height: 100px;
            background-color: #e8f4f8;
        }
    </style>
</head>
<body>
    <div class="content-box">
        Ceci est la zone de contenu. Largeur : 200px, Hauteur : 100px
    </div>
</body>
</html>
```

### 2. Padding

Le padding crée de l'espace entre le contenu et la bordure. Il est transparent et affiche la couleur d'arrière-plan de l'élément.

**Propriétés :**
- `padding-top`, `padding-right`, `padding-bottom`, `padding-left`
- Raccourci : `padding: 10px;` (tous les côtés)
- Raccourci : `padding: 10px 20px;` (haut/bas, gauche/droite)
- Raccourci : `padding: 10px 20px 30px 40px;` (haut, droite, bas, gauche - sens horaire)

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple de Padding</title>
    <style>
        .padding-demo {
            background-color: lightblue;
            border: 2px solid navy;
            padding: 20px;
            margin-bottom: 10px;
        }
        
        .padding-varied {
            background-color: lightgreen;
            border: 2px solid darkgreen;
            padding-top: 10px;
            padding-right: 20px;
            padding-bottom: 30px;
            padding-left: 40px;
        }
    </style>
</head>
<body>
    <div class="padding-demo">
        Padding uniforme de 20px sur tous les côtés
    </div>
    <div class="padding-varied">
        Padding différent sur chaque côté
    </div>
</body>
</html>
```

### 3. Border

La bordure entoure le padding et le contenu. Elle peut avoir différents styles, largeurs et couleurs.

**Propriétés :**
- `border-width` : Épaisseur de la bordure
- `border-style` : solid, dashed, dotted, double, etc.
- `border-color` : Couleur de la bordure
- Raccourci : `border: 2px solid black;`

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple de Border</title>
    <style>
        .border-solid {
            border: 3px solid #333;
            padding: 10px;
            margin: 10px;
        }
        
        .border-dashed {
            border: 2px dashed red;
            padding: 10px;
            margin: 10px;
        }
        
        .border-mixed {
            border-top: 5px solid blue;
            border-right: 3px dotted green;
            border-bottom: 2px dashed orange;
            border-left: 4px double purple;
            padding: 10px;
            margin: 10px;
        }
    </style>
</head>
<body>
    <div class="border-solid">Bordure solide</div>
    <div class="border-dashed">Bordure en tirets</div>
    <div class="border-mixed">Styles de bordure mixtes</div>
</body>
</html>
```

### 4. Margin

La margin crée de l'espace à l'extérieur de la bordure, séparant l'élément des autres éléments.

**Propriétés :**
- `margin-top`, `margin-right`, `margin-bottom`, `margin-left`
- Le raccourci fonctionne comme padding
- Valeur spéciale : `margin: 0 auto;` (centre les éléments block horizontalement)
- Les margins peuvent être négatives (rapproche les éléments)

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple de Margin</title>
    <style>
        .margin-demo {
            background-color: #ffeb3b;
            border: 2px solid #f57c00;
            padding: 10px;
            margin: 20px;
        }
        
        .centered {
            width: 300px;
            background-color: #e1bee7;
            border: 2px solid #7b1fa2;
            padding: 20px;
            margin: 20px auto;
        }
        
        .margin-collapse-1 {
            background-color: #c8e6c9;
            padding: 10px;
            margin-bottom: 30px;
        }
        
        .margin-collapse-2 {
            background-color: #ffccbc;
            padding: 10px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="margin-demo">Margin de 20px sur tous les côtés</div>
    <div class="centered">Centré avec margin: 20px auto</div>
    <div class="margin-collapse-1">Margin inférieure : 30px</div>
    <div class="margin-collapse-2">Margin supérieure : 20px (fusionnée à 30px d'espace total)</div>
</body>
</html>
```

### 5. Outline (Cas Spécial)

L'outline est dessiné à l'extérieur de la bordure mais n'affecte pas la mise en page ni ne prend d'espace.

**Propriétés :**
- `outline-width` : Épaisseur
- `outline-style` : Style (comme border-style)
- `outline-color` : Couleur
- `outline-offset` : Espace entre bordure et outline
- Raccourci : `outline: 2px solid red;`

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple d'Outline</title>
    <style>
        .outline-demo {
            border: 2px solid blue;
            outline: 3px dashed red;
            outline-offset: 5px;
            padding: 10px;
            margin: 20px;
        }
    </style>
</head>
<body>
    <div class="outline-demo">
        Ceci a à la fois une bordure (bleue) et un outline (rouge en tirets)
    </div>
</body>
</html>
```

### Propriété Box-Sizing

Par défaut, largeur et hauteur ne définissent que la taille de la zone de contenu. La propriété `box-sizing` peut changer ce comportement.

**Valeurs :**
- `content-box` (par défaut) : Largeur/hauteur s'applique au contenu seulement
- `border-box` : Largeur/hauteur inclut padding et border

**Exemple de Code :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemple de Box-Sizing</title>
    <style>
        .content-box {
            box-sizing: content-box;
            width: 200px;
            padding: 20px;
            border: 5px solid black;
            background-color: lightblue;
            margin-bottom: 10px;
        }
        
        .border-box {
            box-sizing: border-box;
            width: 200px;
            padding: 20px;
            border: 5px solid black;
            background-color: lightgreen;
        }
    </style>
</head>
<body>
    <div class="content-box">
        content-box : Largeur totale = 200 + 40 + 10 = 250px
    </div>
    <div class="border-box">
        border-box : Largeur totale = 200px
    </div>
</body>
</html>
```

[↑ Retour au Début](#table-des-matières)

---

## Fusion des Marges : Un Ajout Important

### Qu'est-ce que la Fusion des Marges ?

La fusion des marges est un comportement CSS où les marges verticales d'éléments block-level adjacents se combinent (ou "fusionnent") en une seule marge. Cela ne se produit qu'avec les **marges verticales** (haut et bas), jamais avec les marges horizontales (gauche et droite).

### Quand la Fusion des Marges Se Produit-elle ?

La fusion des marges se produit dans trois situations principales :

#### 1. Frères et Sœurs Adjacents
Quand deux éléments block sont empilés verticalement, leurs marges qui se touchent fusionnent.

**Exemple :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Fusion de Marges entre Frères et Sœurs Adjacents</title>
    <style>
        .box1 {
            background-color: lightblue;
            padding: 20px;
            margin-bottom: 30px;
        }
        
        .box2 {
            background-color: lightgreen;
            padding: 20px;
            margin-top: 20px;
        }
        
        /* Résultat : Seulement 30px d'espace entre les boîtes, pas 50px ! */
    </style>
</head>
<body>
    <div class="box1">Boîte 1 a margin-bottom: 30px</div>
    <div class="box2">Boîte 2 a margin-top: 20px</div>
    <p>L'espace entre les boîtes est 30px (la plus grande marge), pas 50px !</p>
</body>
</html>
```

#### 2. Parent et Premier/Dernier Enfant
Si un parent n'a pas de padding ou de border, ses marges peuvent fusionner avec les marges de son premier ou dernier enfant.

**Exemple :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Fusion de Marges Parent-Enfant</title>
    <style>
        .parent {
            background-color: #ffeb3b;
            margin-top: 40px;
            /* Pas de padding ou border en haut */
        }
        
        .child {
            background-color: #ff9800;
            padding: 20px;
            margin-top: 30px;
        }
        
        /* Le haut du parent apparaît à 40px de l'élément précédent,
           pas 70px (40px + 30px) */
    </style>
</head>
<body>
    <div style="background: #ccc; padding: 10px;">Élément Précédent</div>
    <div class="parent">
        <div class="child">
            Enfant avec margin-top: 30px dans parent avec margin-top: 40px
        </div>
    </div>
</body>
</html>
```

#### 3. Blocs Vides
Si un élément block n'a pas de contenu, padding, border ou height, ses marges supérieure et inférieure fusionnent.

**Exemple :**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Fusion de Marges de Bloc Vide</title>
    <style>
        .before {
            background-color: lightcoral;
            padding: 20px;
            margin-bottom: 30px;
        }
        
        .empty {
            margin-top: 20px;
            margin-bottom: 40px;
            /* Pas de contenu, padding ou border */
        }
        
        .after {
            background-color: lightseagreen;
            padding: 20px;
            margin-top: 25px;
        }
        
        /* L'espace sera 40px (la plus grande de toutes les marges) */
    </style>
</head>
<body>
    <div class="before">Élément précédent</div>
    <div class="empty"></div>
    <div class="after">Élément suivant</div>
</body>
</html>
```

### Règles de la Fusion des Marges

1. **Seules les Marges Verticales Fusionnent**
   - Les marges supérieure et inférieure peuvent fusionner
   - Les marges gauche et droite ne fusionnent JAMAIS

2. **La Plus Grande Marge Gagne**
   - Quand les marges fusionnent, la valeur de marge la plus grande est utilisée
   - La plus petite marge est ignorée

3. **Marges Négatives**
   - Si une marge est négative, soustrayez-la de la marge positive
   - Si les deux sont négatives, utilisez la valeur la plus négative

### Quand les Marges ne Fusionnent PAS

Les marges ne fusionneront PAS quand :

1. **Les éléments sont flottants** - Les éléments flottants ne fusionnent jamais les marges
2. **Éléments inline-block** - Seuls les éléments block fusionnent les marges
3. **Éléments positionnés absolument** - Position: absolute/fixed empêche la fusion
4. **Overflow est défini** - Les éléments avec overflow autre que visible ne fusionnent pas
5. **Padding ou border les sépare** - N'importe quel padding/border empêche la fusion
6. **Les éléments sont dans différents contextes de formatage** - Comme les conteneurs flexbox ou grid

### Prévenir la Fusion des Marges

Voici des techniques courantes pour prévenir la fusion des marges indésirable :

**Méthode 1 : Ajouter Padding ou Border**
```css
.parent {
    padding-top: 1px; /* Empêche la fusion avec le premier enfant */
    padding-bottom: 1px; /* Empêche la fusion avec le dernier enfant */
}
/* OU */
.parent {
    border-top: 1px solid transparent;
    border-bottom: 1px solid transparent;
}
```

**Méthode 2 : Utiliser Overflow**
```css
.parent {
    overflow: auto; /* ou hidden, scroll */
}
```

**Méthode 3 : Utiliser les Propriétés Display**
```css
.element {
    display: inline-block; /* Empêche la fusion des marges */
}
```

**Méthode 4 : Utiliser les Pseudo-éléments**
```css
.parent::before,
.parent::after {
    content: "";
    display: table;
}
```

### Exemple Pratique : Mise en Page de Cartes avec Fusion des Marges

```html
<!DOCTYPE html>
<html>
<head>
    <title>Fusion des Marges en Pratique</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
            background: #f0f0f0;
        }
        
        .container {
            background: white;
            border-radius: 8px;
            /* Pas de padding - les marges peuvent fusionner */
        }
        
        .container-fixed {
            background: white;
            border-radius: 8px;
            padding: 1px 20px; /* Le padding empêche la fusion */
            margin-top: 30px;
        }
        
        .card {
            background: #e3f2fd;
            padding: 20px;
            margin: 30px 20px; /* Les marges verticales peuvent fusionner */
        }
        
        h2 {
            background: #1976d2;
            color: white;
            padding: 10px;
            margin: 0 0 20px 0;
        }
        
        .demo-info {
            background: #fff3e0;
            padding: 10px;
            margin: 15px 0;
            border-left: 4px solid #ff9800;
        }
    </style>
</head>
<body>
    <h1>Démonstration de la Fusion des Marges</h1>
    
    <div class="demo-info">
        <strong>Problème :</strong> Sans padding, la marge supérieure de la première carte fusionne avec le conteneur
    </div>
    
    <div class="container">
        <div class="card">
            Première carte - ma marge supérieure (30px) s'échappe du conteneur !
        </div>
        <div class="card">
            Deuxième carte - les marges entre cartes fusionnent à 30px, pas 60px
        </div>
        <div class="card">
            Troisième carte - ma marge inférieure (30px) s'échappe aussi !
        </div>
    </div>
    
    <div class="demo-info">
        <strong>Solution :</strong> Ajouter 1px de padding empêche la fusion des marges
    </div>
    
    <div class="container-fixed">
        <div class="card">
            Première carte - maintenant correctement contenue dans le parent
        </div>
        <div class="card">
            Deuxième carte - les marges fusionnent encore entre cartes (c'est souvent souhaité)
        </div>
        <div class="card">
            Troisième carte - marge inférieure aussi contenue
        </div>
    </div>
</body>
</html>
```

### Pourquoi la Fusion des Marges Existe-t-elle ?

La fusion des marges peut sembler déroutante, mais elle existe pour de bonnes raisons :

1. **Typographie** : Dans les documents texte, vous voulez un espacement cohérent entre les paragraphes indépendamment des paramètres de marge individuels
2. **Flexibilité** : Permet aux éléments de définir leur espacement souhaité sans doubler
3. **Historique** : Ce comportement vient de la typographie d'impression traditionnelle

### Meilleures Pratiques

1. **Être Conscient** : Rappelez-vous toujours que les marges verticales peuvent fusionner
2. **Utiliser Padding** : Quand vous avez besoin d'espace garanti, utilisez padding à la place
3. **Direction Unique** : Considérez utiliser seulement `margin-bottom` OU `margin-top`, pas les deux
4. **Tester Vos Mises en Page** : Vérifiez l'espacement entre éléments pendant le développement
5. **Documenter l'Intention** : Commentez quand vous comptez sur ou prévenez la fusion

### Problèmes Courants

1. **Premier élément dans un conteneur** poussant vers le bas le conteneur lui-même
2. **Espaces inattendus** qui sont plus petits que prévu
3. **Marges "s'échappant"** de leurs conteneurs
4. **Éléments vides** ne créant pas l'espace attendu

Comprendre la fusion des marges vous aide à :
- Déboguer les problèmes d'espacement inattendus
- Créer des mises en page plus prévisibles
- Écrire du CSS plus propre et maintenable
- Éviter les problèmes de mise en page frustrants

[↑ Retour au Début](#table-des-matières)

---

## Exemples Visuels

### Démonstration Complète du Modèle de Boîte

```html
<!DOCTYPE html>
<html>
<head>
    <title>Démo Complète du Modèle de Boîte</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        
        .box-model-demo {
            width: 300px;
            height: 150px;
            margin: 50px auto;
            padding: 30px;
            border: 10px solid #2196F3;
            background-color: #E3F2FD;
            position: relative;
        }
        
        .label {
            position: absolute;
            background: white;
            padding: 2px 5px;
            font-size: 12px;
            border: 1px solid #ccc;
        }
        
        .margin-label {
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .border-label {
            top: 5px;
            left: 5px;
        }
        
        .padding-label {
            top: 20px;
            left: 20px;
        }
        
        .content-label {
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    </style>
</head>
<body>
    <div class="box-model-demo">
        <span class="label margin-label">MARGIN: 50px</span>
        <span class="label border-label">BORDER: 10px</span>
        <span class="label padding-label">PADDING: 30px</span>
        <span class="label content-label">CONTENT: 300x150px</span>
    </div>
</body>
</html>
```

### Comparaison des Propriétés Display

```html
<!DOCTYPE html>
<html>
<head>
    <title>Comparaison des Propriétés Display</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        
        .container {
            background-color: #f5f5f5;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
        }
        
        .block-item {
            display: block;
            background-color: #ff9800;
            color: white;
            padding: 10px;
            margin: 5px 0;
        }
        
        .inline-item {
            display: inline;
            background-color: #4caf50;
            color: white;
            padding: 10px;
            margin: 5px;
        }
        
        .inline-block-item {
            display: inline-block;
            background-color: #2196f3;
            color: white;
            padding: 10px;
            margin: 5px;
            width: 100px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <h3>Éléments Block</h3>
        <div class="block-item">Block 1</div>
        <div class="block-item">Block 2</div>
        <div class="block-item">Block 3</div>
    </div>
    
    <div class="container">
        <h3>Éléments Inline</h3>
        <span class="inline-item">Inline 1</span>
        <span class="inline-item">Inline 2</span>
        <span class="inline-item">Inline 3</span>
    </div>
    
    <div class="container">
        <h3>Éléments Inline-Block</h3>
        <div class="inline-block-item">IB 1</div>
        <div class="inline-block-item">IB 2</div>
        <div class="inline-block-item">IB 3</div>
    </div>
</body>
</html>
```

[↑ Retour au Début](#table-des-matières)

---

## Résumé

### Points Clés

1. **Les Propriétés Display Contrôlent le Flux de Mise en Page**
   - Les éléments block s'empilent verticalement et prennent toute la largeur
   - Les éléments inline s'intègrent horizontalement et s'ajustent au texte
   - Inline-block combine les avantages des deux
   - Display: none supprime complètement les éléments

2. **Le Modèle de Boîte a Quatre Parties Principales**
   - Content : Le contenu réel de l'élément
   - Padding : Espace à l'intérieur de la bordure
   - Border : Le bord de l'élément
   - Margin : Espace à l'extérieur de la bordure

3. **Box-Sizing Change les Calculs**
   - content-box : Largeur/hauteur s'applique au contenu seulement
   - border-box : Largeur/hauteur inclut padding et border

4. **Les Marges Peuvent Fusionner**
   - Les marges verticales entre éléments fusionnent à la valeur la plus grande
   - Les marges horizontales ne fusionnent jamais

5. **Les Outlines N'Affectent Pas la Mise en Page**
   - Utiles pour mettre en surbrillance sans déplacer d'autres éléments

### Cas d'Usage Courants

- **Menus de Navigation** : Utiliser inline ou inline-block pour les menus horizontaux
- **Mises en Page de Cartes** : Combiner padding pour l'espacement interne et margin pour la séparation
- **Centrage** : Utiliser `margin: 0 auto` pour le centrage horizontal des éléments block
- **Design Responsive** : Box-sizing: border-box rend les calculs de largeur prévisibles

[↑ Retour au Début](#table-des-matières)

---

## Ressources

### Documentation
- [MDN Web Docs - CSS Display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- [MDN Web Docs - CSS Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
- [W3Schools - CSS Display Property](https://www.w3schools.com/css/css_display_visibility.asp)
- [W3Schools - CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp)

### Outils de Pratique
- [Visualiseur du Modèle de Boîte CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_box_model_and_inline_boxes)
- Utiliser les DevTools du navigateur (F12) pour inspecter et modifier les propriétés du modèle de boîte

### Prochaines Étapes
Après avoir maîtrisé ces concepts, vous serez prêt à apprendre :
- Positionnement CSS (static, relative, absolute, fixed)
- Mise en page Flexbox
- CSS Grid
- Techniques de design responsive

[↑ Retour au Début](#table-des-matières)