# Devoir 2: Espacement du Modèle de Boîte

## Objectif
Créer une mise en page de cartes qui démontre la maîtrise du Modèle de Boîte CSS. Vous construirez trois cartes d'information avec un espacement approprié en utilisant margin, padding et borders.

## Exigences
1. Créer trois cartes affichant différents types de contenu
2. Utiliser padding pour créer un espacement interne dans chaque carte
3. Utiliser margins pour séparer les cartes les unes des autres
4. Ajouter des borders pour définir les limites des cartes
5. Centrer le conteneur de cartes sur la page
6. Faire en sorte que les cartes aient la même hauteur quel que soit le contenu

## Structure HTML de Départ
styles.css
```css
        /* Réinitialiser les styles par défaut */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            /* TODO: Ajouter padding au body */
        }
        
        .container {
            /* TODO: Définir max-width */
            /* TODO: Centrer le conteneur avec margin */
            /* TODO: Ajouter couleur de fond */
            /* TODO: Ajouter padding */
        }
        
        h1 {
            /* TODO: Ajouter margin bottom */
            /* TODO: Centrer le texte */
            /* TODO: Ajouter couleur */
        }
        
        .cards {
            /* TODO: Configurer le conteneur pour les cartes */
        }
        
        .card {
            /* TODO: Définir largeur (considérer l'utilisation de pourcentages) */
            /* TODO: Ajouter padding pour espacement interne */
            /* TODO: Ajouter margin pour espacement externe */
            /* TODO: Ajouter border */
            /* TODO: Définir couleur de fond */
            /* TODO: Définir hauteur minimale */
        }
        
        .card h2 {
            /* TODO: Ajouter margin bottom */
            /* TODO: Ajouter padding bottom */
            /* TODO: Ajouter border inférieur */
            /* TODO: Définir couleur */
        }
        
        .card p {
            /* TODO: Ajouter margin bottom pour espacement des paragraphes */
            /* TODO: Définir hauteur de ligne */
        }
        
        .card-footer {
            /* TODO: Ajouter margin top */
            /* TODO: Ajouter padding top */
            /* TODO: Ajouter border supérieur */
            /* TODO: Définir alignement du texte */
        }
        
        .button {
            /* TODO: Supprimer les styles par défaut du bouton */
            /* TODO: Ajouter padding */
            /* TODO: Ajouter margin */
            /* TODO: Ajouter border */
            /* TODO: Définir couleur de fond */
            /* TODO: Définir couleur du texte */
            /* TODO: Ajouter cursor pointer */
        }
        
        .button:hover {
            /* TODO: Ajouter effet hover */
        }
        
        /* Styles spéciaux pour cartes */
        .featured {
            /* TODO: Ajouter style spécial pour carte mise en avant */
            /* TODO: Considérer border ou fond différent */
        }
```

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Mise en Page de Cartes du Modèle de Boîte</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Nos Services</h1>
        
        <div class="cards">
            <div class="card">
                <h2>Conception Web</h2>
                <p>Créer de beaux sites web réactifs qui fonctionnent sur tous les appareils. Nos conceptions sont modernes, épurées et conviviales.</p>
                <p>Nous utilisons les dernières technologies incluant HTML5, CSS3 et des frameworks modernes.</p>
                <div class="card-footer">
                    <button class="button">En Savoir Plus</button>
                </div>
            </div>
            
            <div class="card featured">
                <h2>Développement</h2>
                <p>Construire des applications web robustes avec un code propre et maintenable. Des sites simples aux applications complexes.</p>
                <p>Services de développement full-stack avec un focus sur la performance et la sécurité.</p>
                <p>Offre spéciale : Obtenez 20% de réduction sur votre premier projet !</p>
                <div class="card-footer">
                    <button class="button">Commencer</button>
                </div>
            </div>
            
            <div class="card">
                <h2>Conseil</h2>
                <p>Conseils d'experts pour aider votre entreprise à réussir en ligne. Nous analysons vos besoins et fournissons des solutions sur mesure.</p>
                <div class="card-footer">
                    <button class="button">Nous Contacter</button>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

## Tâches à Accomplir

### Tâche 1: Configuration du Conteneur
1. Définir une max-width pour le conteneur (suggestion : 1200px)
2. Centrer le conteneur en utilisant margin auto
3. Ajouter du padding pour créer de l'espace à l'intérieur du conteneur

### Tâche 2: Stylisation des Cartes
1. Ajouter du padding interne à chaque carte (essayer 20px)
2. Ajouter des margins entre les cartes (suggestion : 15px)
3. Ajouter un border pour définir les bords des cartes
4. Définir une hauteur minimale pour que toutes les cartes soient égales

### Tâche 3: Espacement du Contenu
1. Ajouter de la margin aux titres et paragraphes
2. Créer une séparation visuelle entre l'en-tête de la carte et le contenu
3. Styliser le pied de carte avec des borders et de l'espacement

### Tâche 4: Carte Mise en Avant
1. Donner à la carte mise en avant une couleur ou un style de border différent
2. Considérer l'ajout d'une couleur de fond différente
3. Peut-être augmenter le padding ou ajouter une ombre de boîte

### Tâche 5: Stylisation des Boutons
1. Supprimer l'apparence par défaut du bouton
2. Ajouter du padding pour une meilleure zone de clic
3. Styliser avec des couleurs et des borders
4. Ajouter des effets hover

## Résultat Attendu
- Trois cartes espacées uniformément dans une rangée
- Espacement interne cohérent dans chaque carte
- Hiérarchie visuelle claire avec en-têtes, contenu et pieds
- La carte mise en avant se distingue des autres
- Les boutons sont stylisés et interactifs