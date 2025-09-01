# Devoir 1: Bases des Classes et IDs

## Objectif
Pratiquer l'utilisation des attributs class et id HTML et appliquer des styles CSS de base sur eux.

## Instructions

Créez un fichier HTML appelé `recipe-page.html` qui contient une page de recette avec les exigences suivantes:

### Exigences HTML

1. Créez un document HTML complet avec une structure appropriée (DOCTYPE, html, head, body)
2. Incluez un élément `<title>` avec "My Favorite Recipe"
3. Ajoutez les éléments suivants avec les classes et IDs spécifiés:

   **IDs à inclure:**
   - Donnez au `<header>` principal un id de "page-header"
   - Donnez au titre de recette `<h1>` un id de "recipe-title"
   - Donnez à la `<section>` des ingrédients un id de "ingredients-section"
   - Donnez à la `<section>` des instructions un id de "instructions-section"
   - Donnez au `<footer>` un id de "page-footer"

   **Classes à inclure:**
   - Donnez à au moins 3 ingrédients la classe "essential"
   - Donnez à au moins 2 étapes d'instruction la classe "important"
   - Créez un paragraphe avec les classes "note" et "warning" (plusieurs classes sur un élément)
   - Donnez au paragraphe du footer la classe "copyright"

### Exigences CSS

Ajoutez une section `<style>` dans le `<head>` et créez des règles CSS pour:

1. Styliser les sélecteurs d'ID:
   - `#page-header`: Donnez-lui une couleur de fond et du padding
   - `#recipe-title`: Changez la couleur du texte et centrez-le
   - `#page-footer`: Ajoutez une bordure supérieure et une couleur de fond différente

2. Styliser les sélecteurs de classe:
   - `.essential`: Rendez le texte en gras et donnez-lui une couleur différente
   - `.important`: Ajoutez une couleur de fond et du padding
   - `.note`: Ajoutez une bordure autour
   - `.warning`: Rendez le texte rouge

### Exigences de Contenu

Votre recette doit inclure:
- Un titre de recette
- Une liste d'au moins 6 ingrédients (utilisez `<ul>`)
- Une liste d'au moins 5 étapes d'instructions (utilisez `<ol>`)
- Au moins un paragraphe de note ou conseil
- Un footer avec des informations de copyright

## Code de Démarrage

Vous devriez bien sûr avoir un fichier de feuille de style séparé comme styles.css. Je ne fournirai pas de modèle là.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>My Favorite Recipe</title>
    <link rel="stylesheet" href="styles.css"
</head>
<body>
    <!-- Ajoutez votre contenu HTML ici -->
    
</body>
</html>
```

## Soumission

1. Sauvegardez votre fichier sous `recipe-page.html`
2. Testez-le dans votre navigateur pour vous assurer que tous les styles sont appliqués correctement
3. Effectuez un commit et push vers votre dépôt GitHub
4. Soumettez le lien vers votre dépôt

