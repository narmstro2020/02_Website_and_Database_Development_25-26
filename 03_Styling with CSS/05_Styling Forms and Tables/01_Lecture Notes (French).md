# Styliser les Formulaires et Tableaux avec CSS

## Table des Matières

| Sujet | Description |
|-------|-------------|
| [Introduction](#introduction) | Aperçu du style des formulaires et tableaux |
| [Vocabulaire](#vocabulaire) | Termes clés et définitions |
| [1. Styliser les Tableaux avec CSS](#1-styliser-les-tableaux-avec-css) | Apprendre à styliser les tableaux HTML |
| [2. Styliser les Formulaires avec CSS](#2-styliser-les-formulaires-avec-css) | Apprendre à styliser les formulaires HTML |
| [Exemples Visuels](#exemples-visuels) | Exemples complets fonctionnels |
| [Devoirs](#devoirs) | Exercices pratiques |
| [Résumé](#résumé) | Points clés à retenir |
| [Ressources](#ressources) | Matériel d'apprentissage supplémentaire |

---

## Introduction

Bienvenue dans notre leçon sur le style des formulaires et tableaux avec CSS ! Les formulaires et tableaux sont des composants essentiels du développement web. Les tableaux nous aident à organiser les données en lignes et colonnes, tandis que les formulaires permettent aux utilisateurs de saisir et soumettre des informations. Dans cette leçon, nous apprendrons comment rendre ces éléments visuellement attrayants et conviviaux en utilisant CSS.

### Ce que Vous Allez Apprendre :
- Comment styliser les bordures, espacements et arrière-plans des tableaux
- Comment créer des formulaires attrayants et accessibles
- Les meilleures pratiques pour la conception de formulaires et tableaux
- Les propriétés CSS spécifiques aux formulaires et tableaux

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

## Vocabulaire

### Termes Liés aux Tableaux
- **border-collapse** : Propriété CSS qui détermine si les bordures de tableau sont séparées ou fusionnées en une seule bordure
- **border-spacing** : Propriété CSS qui définit la distance entre les bordures de cellules adjacentes
- **caption-side** : Propriété CSS qui positionne la légende d'un tableau
- **thead** : Élément HTML qui groupe le contenu d'en-tête dans un tableau
- **tbody** : Élément HTML qui groupe le contenu du corps dans un tableau
- **tfoot** : Élément HTML qui groupe le contenu de pied de page dans un tableau
- **nth-child()** : Sélecteur de pseudo-classe CSS qui correspond aux éléments basés sur leur position

### Termes Liés aux Formulaires
- **fieldset** : Élément HTML qui groupe les contrôles de formulaire liés
- **legend** : Élément HTML qui fournit une légende pour un fieldset
- **placeholder** : Attribut HTML qui fournit un texte d'indication dans les entrées de formulaire
- **focus** : L'état quand un élément de formulaire est sélectionné/actif
- **:focus** : Pseudo-classe CSS qui stylise un élément quand il a le focus
- **:hover** : Pseudo-classe CSS qui stylise un élément quand la souris survole
- **:disabled** : Pseudo-classe CSS qui stylise les éléments de formulaire désactivés
- **outline** : Propriété CSS qui dessine une ligne autour des éléments (souvent visible sur focus)

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

## 1. Styliser les Tableaux avec CSS

Les tableaux sont des outils puissants pour afficher des données structurées. Apprenons comment les rendre beaux et fonctionnels.

### Révision de la Structure de Base des Tableaux

```html
<table>
    <caption>Notes des Étudiants</caption>
    <thead>
        <tr>
            <th>Nom</th>
            <th>Note</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Alice</td>
            <td>A</td>
        </tr>
        <tr>
            <td>Bob</td>
            <td>B+</td>
        </tr>
    </tbody>
</table>
```

### Propriétés Essentielles de Style des Tableaux

#### 1. Fusion des Bordures

La propriété `border-collapse` contrôle le comportement des bordures de tableau :

```css
/* Bordures séparées (par défaut) */
table {
    border-collapse: separate;
    border-spacing: 2px;
}

/* Bordures fusionnées (recommandé) */
table {
    border-collapse: collapse;
}
```

#### 2. Ajout de Bordures

```css
table {
    border: 2px solid #333;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
}
```

#### 3. Style des En-têtes de Tableau

```css
th {
    background-color: #4CAF50;
    color: white;
    font-weight: bold;
    text-align: left;
    padding: 12px;
}
```

#### 4. Couleurs de Lignes Alternées (Rayures Zébrées)

```css
/* Lignes paires */
tbody tr:nth-child(even) {
    background-color: #f2f2f2;
}

/* Lignes impaires */
tbody tr:nth-child(odd) {
    background-color: white;
}
```

#### 5. Effets de Survol

```css
tbody tr:hover {
    background-color: #ddd;
    cursor: pointer;
}
```

### Exemple Complet de Tableau

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tableau Stylisé</title>
    <style>
        table {
            border-collapse: collapse;
            width: 100%;
            margin: 20px 0;
            font-family: Arial, sans-serif;
        }
        
        caption {
            font-size: 1.2em;
            margin-bottom: 10px;
            font-weight: bold;
            color: #333;
        }
        
        th {
            background-color: #4CAF50;
            color: white;
            padding: 12px;
            text-align: left;
        }
        
        td {
            padding: 10px;
            border-bottom: 1px solid #ddd;
        }
        
        tbody tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        
        tbody tr:hover {
            background-color: #f5f5f5;
        }
    </style>
</head>
<body>
    <table>
        <caption>Inventaire des Produits</caption>
        <thead>
            <tr>
                <th>Produit</th>
                <th>Quantité</th>
                <th>Prix</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Ordinateur Portable</td>
                <td>15</td>
                <td>999€</td>
            </tr>
            <tr>
                <td>Souris</td>
                <td>50</td>
                <td>25€</td>
            </tr>
            <tr>
                <td>Clavier</td>
                <td>30</td>
                <td>75€</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### Tableaux Responsives

Pour un meilleur affichage mobile :

```css
/* Conteneur pour défilement horizontal sur petits écrans */
.table-container {
    overflow-x: auto;
}

table {
    min-width: 600px;
}
```

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

## 2. Styliser les Formulaires avec CSS

Les formulaires sont la façon dont les utilisateurs interagissent avec votre site web. Une bonne conception de formulaire améliore l'expérience utilisateur et augmente les taux de completion.

### Révision de la Structure de Base des Formulaires

```html
<form>
    <label for="nom">Nom :</label>
    <input type="text" id="nom" name="nom">
    
    <label for="email">Email :</label>
    <input type="email" id="email" name="email">
    
    <input type="submit" value="Envoyer">
</form>
```

### Techniques Essentielles de Style des Formulaires

#### 1. Style de Base des Entrées

```css
input[type="text"],
input[type="email"],
input[type="password"],
textarea {
    width: 100%;
    padding: 10px;
    margin: 8px 0;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-size: 16px;
    box-sizing: border-box;
}
```

#### 2. Style des Étiquettes

```css
label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}
```

#### 3. États de Focus

```css
input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
    outline: none;
    border-color: #4CAF50;
    box-shadow: 0 0 5px rgba(76, 175, 80, 0.3);
}
```

#### 4. Style des Boutons

```css
input[type="submit"],
button {
    background-color: #4CAF50;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s;
}

input[type="submit"]:hover,
button:hover {
    background-color: #45a049;
}
```

#### 5. Fieldset et Legend

```css
fieldset {
    border: 2px solid #ddd;
    border-radius: 4px;
    padding: 20px;
    margin-bottom: 20px;
}

legend {
    font-weight: bold;
    color: #333;
    padding: 0 10px;
}
```

### Exemple Complet de Formulaire

```html
<!DOCTYPE html>
<html>
<head>
    <title>Formulaire Stylisé</title>
    <style>
        * {
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            padding: 20px;
        }
        
        form {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            max-width: 500px;
            margin: 0 auto;
        }
        
        h2 {
            color: #333;
            text-align: center;
            margin-bottom: 30px;
        }
        
        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
            font-weight: bold;
        }
        
        input[type="text"],
        input[type="email"],
        input[type="password"],
        select,
        textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 14px;
        }
        
        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="password"]:focus,
        select:focus,
        textarea:focus {
            outline: none;
            border-color: #4CAF50;
            box-shadow: 0 0 5px rgba(76, 175, 80, 0.2);
        }
        
        button {
            background-color: #4CAF50;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <form>
        <h2>Formulaire d'Inscription</h2>
        
        <label for="prenom">Prénom :</label>
        <input type="text" id="prenom" name="prenom" placeholder="Entrez votre prénom">
        
        <label for="nom">Nom :</label>
        <input type="text" id="nom" name="nom" placeholder="Entrez votre nom">
        
        <label for="email">Email :</label>
        <input type="email" id="email" name="email" placeholder="votre@email.com">
        
        <label for="pays">Pays :</label>
        <select id="pays" name="pays">
            <option value="">Sélectionnez votre pays</option>
            <option value="france">France</option>
            <option value="canada">Canada</option>
            <option value="belgique">Belgique</option>
        </select>
        
        <button type="submit">S'inscrire</button>
    </form>
</body>
</html>
```

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

## Exemples Visuels

### Exemple 1 : Tableau de Données Professionnel

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tableau Professionnel</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            padding: 20px;
            background-color: #f5f5f5;
        }
        
        .table-container {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        caption {
            font-size: 1.5em;
            margin-bottom: 15px;
            text-align: left;
            color: #2c3e50;
        }
        
        th {
            background-color: #3498db;
            color: white;
            padding: 15px;
            text-align: left;
            font-weight: 500;
        }
        
        td {
            padding: 12px 15px;
            border-bottom: 1px solid #ecf0f1;
        }
        
        tbody tr:hover {
            background-color: #f8f9fa;
            transition: background-color 0.2s;
        }
        
        .status {
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.85em;
            font-weight: bold;
        }
        
        .status-actif {
            background-color: #d4edda;
            color: #155724;
        }
        
        .status-en-attente {
            background-color: #fff3cd;
            color: #856404;
        }
    </style>
</head>
<body>
    <div class="table-container">
        <table>
            <caption>Annuaire des Employés</caption>
            <thead>
                <tr>
                    <th>Nom</th>
                    <th>Département</th>
                    <th>Email</th>
                    <th>Statut</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Jean Dupont</td>
                    <td>Ingénierie</td>
                    <td>jean@entreprise.com</td>
                    <td><span class="status status-actif">Actif</span></td>
                </tr>
                <tr>
                    <td>Marie Martin</td>
                    <td>Marketing</td>
                    <td>marie@entreprise.com</td>
                    <td><span class="status status-actif">Actif</span></td>
                </tr>
                <tr>
                    <td>Pierre Durand</td>
                    <td>Ventes</td>
                    <td>pierre@entreprise.com</td>
                    <td><span class="status status-en-attente">En Attente</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

## Devoirs

### Devoir 1 : Styliser un Tableau de Produits
Créez et stylisez un tableau affichant au moins 5 produits avec des colonnes pour le Nom du Produit, Catégorie, Prix et Statut du Stock.

**Exigences :**
- Utiliser des couleurs de lignes alternées
- Ajouter des effets de survol
- Styliser l'en-tête avec une couleur de fond distincte
- Inclure une légende de tableau
- Rendre les bordures fusionnées
- Ajouter un espacement approprié

### Devoir 2 : Créer un Formulaire d'Inscription Stylisé
Construisez un formulaire d'inscription avec différents types d'entrées et un style professionnel.

**Exigences :**
- Inclure des champs texte, email, mot de passe, select et textarea
- Utiliser des fieldsets pour grouper les champs liés
- Ajouter des états de focus à toutes les entrées
- Styliser le bouton de soumission avec effet de survol
- Inclure du texte placeholder
- Rendre le formulaire responsive

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

## Résumé

### Points Clés à Retenir

#### Tableaux
- Utilisez `border-collapse: collapse` pour des conceptions de tableaux plus nettes
- Appliquez les sélecteurs `:nth-child()` pour les couleurs de lignes alternées
- Incluez toujours une structure de tableau appropriée (thead, tbody, tfoot)
- Ajoutez des effets de survol pour améliorer l'interaction utilisateur
- Utilisez du padding pour créer de l'espace dans les cellules

#### Formulaires
- Stylisez tous les états de formulaire : par défaut, survol, focus et désactivé
- Groupez les champs liés avec des fieldsets
- Utilisez un espacement et alignement cohérents
- Fournissez un retour visuel clair pour les interactions utilisateur
- Incluez toujours des étiquettes pour l'accessibilité
- Utilisez du texte placeholder pour guider les utilisateurs

### Propriétés CSS Apprises

**Propriétés de Tableau :**
- `border-collapse`
- `border-spacing`
- `caption-side`
- `:nth-child()`

**Propriétés de Formulaire :**
- `:focus`
- `:hover`
- `:disabled`
- `:valid` / `:invalid`
- `outline`
- `box-shadow`
- `transition`

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

## Ressources

### Documentation
- [MDN - Styliser les Tableaux](https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Styling_tables)
- [MDN - Styliser les Formulaires](https://developer.mozilla.org/fr/docs/Learn/Forms/Styling_web_forms)
- [W3Schools - Tableaux CSS](https://www.w3schools.com/css/css_table.asp)
- [W3Schools - Formulaires CSS](https://www.w3schools.com/css/css_form.asp)

### Références CSS
- [MDN - border-collapse](https://developer.mozilla.org/fr/docs/Web/CSS/border-collapse)
- [MDN - :nth-child()](https://developer.mozilla.org/fr/docs/Web/CSS/:nth-child)
- [MDN - :focus](https://developer.mozilla.org/fr/docs/Web/CSS/:focus)
- [MDN - fieldset](https://developer.mozilla.org/fr/docs/Web/HTML/Element/fieldset)

[↑ Retour au Sommaire](#styliser-les-formulaires-et-tableaux-avec-css)

---

*Fin des Notes de Cours - Styliser les Formulaires et Tableaux avec CSS*