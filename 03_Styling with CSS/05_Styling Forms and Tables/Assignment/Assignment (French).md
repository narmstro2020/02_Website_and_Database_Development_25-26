# Devoir 1 : Styliser un Tableau de Produits

## Objectif
Styliser un tableau affichant au moins 5 produits avec un style professionnel.

## Exigences
- [ ] Utiliser des couleurs de lignes alternées (rayures zébrées)
- [ ] Ajouter des effets de survol aux lignes du tableau
- [ ] Styliser l'en-tête avec une couleur de fond distincte
- [ ] Inclure une légende descriptive du tableau
- [ ] Utiliser des bordures fusionnées
- [ ] Ajouter un espacement approprié à toutes les cellules
- [ ] Rendre le tableau responsive et visuellement attrayant

## Code de Départ

### styles.css 

```css
/* Reset et styles de base */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    /* Ajoutez vos styles de body ici */
}

/* Styles de tableau */
table {
    /* Ajoutez vos styles de tableau ici */
}

caption {
    /* Stylisez la légende du tableau */
}

/* Styles d'en-tête */
thead {
    /* Ajoutez les styles thead si nécessaire */
}

th {
    /* Stylisez les en-têtes du tableau */
}

/* Styles de corps */
tbody {
    /* Ajoutez les styles tbody si nécessaire */
}

td {
    /* Stylisez les cellules du tableau */
}

/* Rayures zébrées - couleurs de lignes alternées */
/* Ajoutez vos sélecteurs nth-child ici */

/* Effet de survol */
/* Ajoutez vos styles de survol ici */
```

### index.html déjà construit

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tableau d'Inventaire des Produits</title>
    <style>

        
    </style>
</head>
<body>
    <div class="table-wrapper">
        <table>
            <caption>Inventaire des Produits - Magasin d'Électronique</caption>
            <thead>
                <tr>
                    <th>Nom du Produit</th>
                    <th>Catégorie</th>
                    <th>Prix</th>
                    <th>Statut du Stock</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>MacBook Pro 14"</td>
                    <td>Ordinateurs Portables</td>
                    <td>1 999,00 €</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>iPhone 15 Pro</td>
                    <td>Smartphones</td>
                    <td>999,00 €</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>iPad Air</td>
                    <td>Tablettes</td>
                    <td>599,00 €</td>
                    <td><span class="stock-status low-stock">Stock Faible</span></td>
                </tr>
                <tr>
                    <td>AirPods Pro</td>
                    <td>Audio</td>
                    <td>249,00 €</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>Apple Watch Series 9</td>
                    <td>Objets Connectés</td>
                    <td>399,00 €</td>
                    <td><span class="stock-status out-of-stock">Rupture de Stock</span></td>
                </tr>
                <tr>
                    <td>Magic Keyboard</td>
                    <td>Accessoires</td>
                    <td>299,00 €</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>Studio Display</td>
                    <td>Moniteurs</td>
                    <td>1 599,00 €</td>
                    <td><span class="stock-status low-stock">Stock Faible</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

## Conseils
1. Utilisez `border-collapse: collapse` sur le tableau pour des bordures plus nettes
2. Considérez l'utilisation de couleurs qui correspondent à un schéma de couleurs cohérent
3. Pour les rayures zébrées, utilisez `tbody tr:nth-child(even)` et `tbody tr:nth-child(odd)`
4. Ajoutez une transition subtile pour l'effet de survol pour le rendre fluide
5. Considérez l'ajout de couleurs différentes ou de badges pour le statut du stock (En Stock, Stock Faible, Rupture de Stock)

## Défis Bonus
- Ajouter une section tfoot avec des totaux
- Styliser le statut du stock avec des badges colorés
- Aligner la colonne des prix à droite
- Ajouter une ombre portée subtile au tableau

## Soumission
Sauvegardez votre fichier sous `tableau-produits.html` et testez-le dans votre navigateur. Assurez-vous que toutes les exigences sont respectées avant de soumettre via GitHub.