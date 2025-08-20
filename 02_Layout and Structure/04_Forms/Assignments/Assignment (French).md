# Devoir 1 : Formulaire de Connexion Simple - Modèle

## Objectif
Créer un formulaire de connexion basique qui collecte un nom d'utilisateur et un mot de passe de l'utilisateur.

## Exigences

Votre formulaire de connexion doit inclure :

1. Un élément form avec un id de "loginForm"
2. Un champ nom d'utilisateur :
   - Utiliser le type d'input approprié
   - Inclure une étiquette (label)
   - Le rendre obligatoire
   - Ajouter un texte indicatif "Entrez le nom d'utilisateur"
3. Un champ mot de passe :
   - Utiliser le type d'input approprié
   - Inclure une étiquette (label)
   - Le rendre obligatoire
   - Ajouter un texte indicatif "Entrez le mot de passe"
4. Une case à cocher "Se souvenir de moi" avec une étiquette
5. Un bouton de soumission avec le texte "Se connecter"
6. Un bouton de réinitialisation avec le texte "Effacer"
7. Structure HTML appropriée avec DOCTYPE, html, head, title et body
8. JavaScript pour gérer la soumission du formulaire et afficher les valeurs dans la console

## Code de Départ

```html
<!DOCTYPE html>
<html>
<head>
    <title>Formulaire de Connexion</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Bon retour !</h1>
    </header>
    
    <main>
        <!-- Créez votre formulaire ici -->
        
        
        
    </main>
    
    <footer>
        <p>Vous n'avez pas de compte ? Inscrivez-vous aujourd'hui !</p>
    </footer>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const formData = new FormData(this);

            console.log('Formulaire de connexion soumis :');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

## Indices

- Rappelez-vous que les inputs de mot de passe doivent masquer le texte pendant la saisie
- L'attribut `for` dans les labels doit correspondre à l'`id` de l'input
- Utilisez `type="checkbox"` pour l'option se souvenir de moi
- Le formulaire a besoin d'un id pour attacher l'écouteur d'événement JavaScript
- Utilisez `FormData` pour obtenir toutes les valeurs du formulaire dans le JavaScript

## Résultat Attendu

Lorsque l'utilisateur remplit le formulaire et clique sur "Se connecter", la console devrait afficher quelque chose comme :
```
Formulaire de connexion soumis :
username: jeandupont
password: monmotdepasse123
remember: on
```

## Liste de Vérification pour la Soumission

- [ ] Le formulaire a l'attribut id approprié
- [ ] Champ nom d'utilisateur avec étiquette
- [ ] Champ mot de passe avec étiquette
- [ ] Case à cocher Se souvenir de moi avec étiquette
- [ ] Bouton de soumission
- [ ] Bouton de réinitialisation
- [ ] Attributs required sur nom d'utilisateur et mot de passe
- [ ] Texte indicatif sur les deux champs de texte
- [ ] JavaScript empêche la soumission réelle du formulaire
- [ ] JavaScript affiche toutes les données du formulaire dans la console
- [ ] Structure de document HTML appropriée