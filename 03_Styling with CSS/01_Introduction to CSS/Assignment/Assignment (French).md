# Devoir 3 : Site Web Multi-Pages - Modèle

## Instructions
Créez un site web de 3 pages en utilisant du **CSS externe**. Toutes les pages doivent être liées au même fichier CSS.

## Liste des Exigences
- [ ] Créer trois fichiers HTML : home.html, about.html, contact.html
- [ ] Créer un fichier styles.css
- [ ] Lier toutes les pages HTML au même fichier CSS
- [ ] Inclure des liens de navigation entre toutes les pages
- [ ] Styliser les en-têtes, paragraphes et liens de manière cohérente
- [ ] Utiliser une structure HTML appropriée sur toutes les pages

## Structure des Fichiers
```
assignment3/
│
├── home.html
├── about.html
├── contact.html
└── styles.css
```

## Modèles HTML

### home.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Accueil - Mon Site Web</title>
    <meta charset="UTF-8">
    <!-- Lien vers le fichier CSS externe -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenue sur Mon Site Web</h1>
        <nav>
            <ul>
                <li><a href="home.html">Accueil</a></li>
                <li><a href="about.html">À propos</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Page d'Accueil</h2>
            <p>Bienvenue sur mon site web ! Ceci est la page d'accueil.</p>
            <p>Ajoutez plus de contenu sur ce que votre site web offre.</p>
        </section>
        
        <section>
            <h3>Contenu Vedette</h3>
            <p>Ajoutez du contenu intéressant ici.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Mon Site Web. Tous droits réservés.</p>
    </footer>
</body>
</html>
```

### about.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>À propos - Mon Site Web</title>
    <meta charset="UTF-8">
    <!-- Lien vers le fichier CSS externe -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>À Propos de Nous</h1>
        <nav>
            <ul>
                <li><a href="home.html">Accueil</a></li>
                <li><a href="about.html">À propos</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Notre Histoire</h2>
            <p>Racontez votre histoire ici.</p>
            <p>Ajoutez des informations sur votre parcours.</p>
        </section>
        
        <section>
            <h3>Notre Mission</h3>
            <p>Décrivez votre mission ou vos objectifs.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Mon Site Web. Tous droits réservés.</p>
    </footer>
</body>
</html>
```

### contact.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Contact - Mon Site Web</title>
    <meta charset="UTF-8">
    <!-- Lien vers le fichier CSS externe -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Contactez-nous</h1>
        <nav>
            <ul>
                <li><a href="home.html">Accueil</a></li>
                <li><a href="about.html">À propos</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Prenez Contact</h2>
            <p>Nous serions ravis d'avoir de vos nouvelles !</p>
            
            <h3>Informations de Contact</h3>
            <p><strong>Courriel :</strong> info@monsite.com</p>
            <p><strong>Téléphone :</strong> (555) 123-4567</p>
            <p><strong>Adresse :</strong> 123 Rue Web, Ville Internet, WWW 12345</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Mon Site Web. Tous droits réservés.</p>
    </footer>
</body>
</html>
```

### styles.css (Modèle)
```css
/* Réinitialiser les styles par défaut */
body {
    /* Ajouter des styles pour le body */
}

/* Styles de l'en-tête */
header {
    /* Ajouter les styles de l'en-tête */
}

/* Styles des titres */
h1 {
    /* Ajouter les styles de h1 */
}

h2 {
    /* Ajouter les styles de h2 */
}

h3 {
    /* Ajouter les styles de h3 */
}

/* Styles de navigation */
nav {
    /* Ajouter les styles de nav */
}

nav ul {
    /* Ajouter des styles pour la liste de navigation */
}

nav li {
    /* Ajouter des styles pour les éléments de liste */
}

/* Styles des liens */
a {
    /* Ajouter les styles des liens */
}

a:hover {
    /* Ajouter l'effet hover pour les liens */
}

/* Styles du contenu principal */
main {
    /* Ajouter les styles de main */
}

/* Styles de section */
section {
    /* Ajouter les styles de section */
}

/* Styles des paragraphes */
p {
    /* Ajouter les styles des paragraphes */
}

/* Styles du pied de page */
footer {
    /* Ajouter les styles du pied de page */
}
```

## Propriétés CSS à Considérer
- Couleurs d'arrière-plan et de texte
- Familles et tailles de police
- Rembourrage et marges
- Alignement du texte
- Bordures
- Propriétés d'affichage pour la navigation
- Effets de survol pour les liens

## Conseils
1. Gardez votre CSS organisé avec des commentaires
2. Testez tous les liens de navigation
3. Assurez-vous que le chemin du fichier CSS est correct dans tous les fichiers HTML
4. Utilisez un espacement et des couleurs cohérents sur toutes les pages
5. Envisagez d'ajouter un effet de survol aux liens de navigation

## Instructions de Soumission
1. Créez un dossier appelé `assignment3`
2. Placez les quatre fichiers dans ce dossier
3. Testez toutes les pages et la navigation dans votre navigateur
4. Validez dans Git avec le message : "Terminer le Devoir 3 : Site Web Multi-Pages avec CSS Externe"
5. Poussez vers GitHub