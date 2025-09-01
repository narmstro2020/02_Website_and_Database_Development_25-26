# Devwa 1: Baz Class ak ID

## Objektif
Pratike itilize atribi class ak id HTML epi aplike estil CSS debaz sou yo.

## Enstriksyon

Kreye yon fichye HTML ki rele `recipe-page.html` ki gen yon paj resèt ak kondisyon sa yo:

### Kondisyon HTML

1. Kreye yon dokiman HTML konplè ak bon estrikti (DOCTYPE, html, head, body)
2. Mete yon eleman `<title>` ak "My Favorite Recipe"
3. Ajoute eleman sa yo ak class ak ID espesifye yo:

   **ID pou mete:**
   - Bay `<header>` prensipal la yon id "page-header"
   - Bay tit resèt `<h1>` la yon id "recipe-title"
   - Bay seksyon engredyan `<section>` an yon id "ingredients-section"
   - Bay seksyon enstriksyon `<section>` an yon id "instructions-section"
   - Bay `<footer>` la yon id "page-footer"

   **Class pou mete:**
   - Bay omwen 3 engredyan class "essential"
   - Bay omwen 2 etap enstriksyon class "important"
   - Kreye yon paragraf ak class "note" ak "warning" (plizyè class sou yon eleman)
   - Bay paragraf footer la class "copyright"

### Kondisyon CSS

Ajoute yon seksyon `<style>` nan `<head>` la epi kreye règ CSS pou:

1. Bay estil selektè ID yo:
   - `#page-header`: Bay li yon koulè background ak padding
   - `#recipe-title`: Chanje koulè tèks la epi santre li
   - `#page-footer`: Ajoute yon bordure anwo ak yon koulè background diferan

2. Bay estil selektè class yo:
   - `.essential`: Fè tèks la fonse epi bay li yon koulè diferan
   - `.important`: Ajoute yon koulè background ak padding
   - `.note`: Ajoute yon bordure alantou li
   - `.warning`: Fè tèks la wouj

### Kondisyon Konteni

Resèt ou a ta dwe gen ladan:
- Yon tit resèt
- Yon lis omwen 6 engredyan (itilize `<ul>`)
- Yon lis omwen 5 etap enstriksyon (itilize `<ol>`)
- Omwen yon paragraf nòt oswa konsèy
- Yon footer ak enfòmasyon copyright

## Kòd Kòmansman

Ou ta dwe gen yon fichye stylesheet separe kòm styles.css. Mwen p ap bay yon modèl la.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>My Favorite Recipe</title>
    <link rel="stylesheet" href="styles.css"
</head>
<body>
    <!-- Ajoute konteni HTML ou a isit la -->
    
</body>
</html>
```

## Soumèt Travay la

1. Sove fichye ou a kòm `recipe-page.html`
2. Teste li nan navigatè ou pou asire w tout estil yo aplike kòrèkteman
3. Commit epi push nan repozitwa GitHub ou
4. Soumèt lyen repozitwa ou a

