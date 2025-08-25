# Devoir 1 : Créateur de Palette de Couleurs

## Objectif
Créer une page web qui démontre votre compréhension des formats de couleurs CSS en construisant une vitrine de palette de couleurs. Vous créerez des échantillons de couleurs utilisant différents formats de couleurs et les appliquerez à divers éléments HTML.

## Exigences

### Structure HTML
Créez un fichier HTML avec :
1. Un titre principal (h1) pour le titre de la page
2. Six sections, chacune contenant :
   - Un sous-titre (h2) pour le nom du format de couleur
   - Au moins 3 éléments paragraphe démontrant différentes couleurs
   - Un élément article avec un arrière-plan coloré

### Exigences CSS
Vous devez démontrer TOUS les formats de couleurs suivants :
1. **Section Couleurs Nommées** : Utilisez au moins 5 couleurs nommées différentes
2. **Section Hexadécimale** : Utilisez les couleurs hex complètes (#RRVVBB) et abrégées (#RVB)
3. **Section RGB** : Créez des couleurs en utilisant les valeurs rgb()
4. **Section RGBA** : Montrez la transparence avec au moins 3 valeurs alpha différentes
5. **Section HSL** : Créez un schéma de couleurs en utilisant hsl()
6. **Section HSLA** : Combinez HSL avec la transparence

### Tâches Spécifiques
1. Créez un effet "arc-en-ciel" en utilisant au moins 7 couleurs différentes dans n'importe quel format
2. Démontrez la transparence en superposant des éléments avec RGBA ou HSLA
3. Créez un schéma de couleurs monochromatique (différentes nuances de la même couleur)
4. Stylisez la couleur du texte ET la couleur d'arrière-plan pour chaque section
5. Ajoutez un pied de page avec un effet de type dégradé en utilisant la transparence

## Code de Démarrage

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Vitrine de Palette de Couleurs</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Vitrine de Palette de Couleurs CSS</h1>
    </header>
    
    <main>
        <section>
            <h2>Couleurs Nommées</h2>
            <p>Ce texte utilise une couleur nommée.</p>
            <p>Celui-ci a une couleur nommée différente.</p>
            <p>Ceci combine des couleurs nommées de texte et d'arrière-plan.</p>
            <article>
                Cet article a un arrière-plan de couleur nommée.
            </article>
        </section>
        
        <!-- Ajoutez plus de sections pour chaque format de couleur -->
        
    </main>
    
    <footer>
        <p>Pied de page avec effets de couleurs créatifs</p>
    </footer>
</body>
</html>
```

styles.css
```css
        body {
            /* Ajoutez une couleur d'arrière-plan claire */
        }
        
        h1 {
            /* Centrez et stylisez le titre principal */
        }
        
        section {
            /* Ajoutez de l'espacement entre les sections */
        }
        
        /* Ajoutez vos styles de couleurs ci-dessous */


```

## Conseils
- Utilisez des commentaires dans votre CSS pour étiqueter chaque section de format de couleur
- Testez la transparence en superposant des éléments
- Rappelez-vous que les valeurs de teinte HSL vont de 0 à 360 degrés
- Pour l'arc-en-ciel, pensez à la roue chromatique
- Un schéma monochromatique peut utiliser différentes valeurs de luminosité ou de saturation

## Soumission
Soumettez deux fichiers :
1. `palette-couleurs.html` - Votre fichier HTML complet avec CSS intégré
2. Une capture d'écran de votre page web rendue

## Défi Bonus (Optionnel)
Créez un design de "carte de couleur" où chaque échantillon de couleur ressemble à une carte physique avec :
- Un effet d'ombre utilisant RGBA
- La valeur de la couleur affichée comme texte sur la carte
- Des coins arrondis en utilisant du CSS que vous recherchez vous-même