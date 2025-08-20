# Devwa 1: Fòm Koneksyon Senp - Modèl

## Objektif
Kreye yon fòm koneksyon debaz ki kolekte yon non itilizatè ak modpas nan men itilizatè a.

## Egzijans yo

Fòm koneksyon ou a dwe gen:

1. Yon eleman form ak yon id "loginForm"
2. Yon chan non itilizatè:
   - Sèvi ak tip input ki apwopriye
   - Gen yon etikèt (label)
   - Fè li obligatwa
   - Ajoute tèks endikas "Antre non itilizatè"
3. Yon chan modpas:
   - Sèvi ak tip input ki apwopriye
   - Gen yon etikèt (label)
   - Fè li obligatwa
   - Ajoute tèks endikas "Antre modpas"
4. Yon bwat pou tcheke "Sonje mwen" ak yon etikèt
5. Yon bouton pou soumèt ak tèks "Konekte"
6. Yon bouton pou reyinisyalize ak tèks "Efase"
7. Bon estrikti HTML ak DOCTYPE, html, head, title, ak body
8. JavaScript pou jere soumisyon fòm lan epi montre valè yo nan konsòl la

## Kòd Kòmansman

```html
<!DOCTYPE html>
<html>
<head>
    <title>Fòm Koneksyon</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Byenveni Ankò!</h1>
    </header>
    
    <main>
        <!-- Kreye fòm ou a isit la -->
        
        
        
    </main>
    
    <footer>
        <p>Ou pa gen kont? Enskri jodi a!</p>
    </footer>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const formData = new FormData(this);

            console.log('Fòm koneksyon soumèt:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

## Endikas yo

- Sonje input modpas yo dwe kache tèks la pandan itilizatè a ap tape
- Atribi `for` nan label yo dwe koresponn ak `id` input la
- Sèvi ak `type="checkbox"` pou opsyon sonje mwen an
- Fòm lan bezwen yon id pou atache pwogram JavaScript la
- Sèvi ak `FormData` pou jwenn tout valè fòm lan nan JavaScript

## Rezilta Espere

Lè itilizatè a ranpli fòm lan epi klike sou "Konekte", konsòl la ta dwe montre yon bagay tankou:
```
Fòm koneksyon soumèt:
username: janjak
password: modpas123
remember: on
```

## Lis Verifikasyon pou Soumèt

- [ ] Fòm lan gen bon atribi id
- [ ] Chan non itilizatè ak etikèt
- [ ] Chan modpas ak etikèt
- [ ] Bwat pou tcheke Sonje mwen ak etikèt
- [ ] Bouton pou soumèt
- [ ] Bouton pou reyinisyalize
- [ ] Atribi required sou non itilizatè ak modpas
- [ ] Tèks endikas sou tou de chan tèks yo
- [ ] JavaScript anpeche fòm lan vrèman soumèt
- [ ] JavaScript montre tout done fòm lan nan konsòl
- [ ] Bon estrikti dokiman HTML