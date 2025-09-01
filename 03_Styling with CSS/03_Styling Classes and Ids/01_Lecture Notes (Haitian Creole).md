# Atribi Class ak ID HTML ak Estil

## Tab Matyè

| Sijè                                                    | Deskripsyon                                    |
|---------------------------------------------------------|------------------------------------------------|
| [1. Entwodiksyon](#entwodiksyon)                       | Apèsi sou atribi class ak id                  |
| [2. Atribi Class HTML](#atribi-class-html)             | Konprann ak itilize atribi class              |
| [3. Atribi ID HTML](#atribi-id-html)                   | Konprann ak itilize atribi id                 |
| [4. Bay Estil Class ak ID](#bay-estil-class-ak-id)     | Kijan pou aplike CSS sou class ak id          |
| [5. Règ Kaskad](#règ-kaskad)                           | Konprann espesifisite CSS ak kaskad           |
| [6. Gwoupman ak Chèn](#gwoupman-ak-chèn)               | Teknik selektè avanse                         |
| [7. Rezime](#rezime)                                   | Pwen kle yo                                   |
| [8. Resous](#resous)                                   | Materyèl aprantisaj adisyonèl                 |

---

## Entwodiksyon

Nan leson anvan nou yo, nou te aprann kijan pou kreye dokiman HTML ak plizyè eleman tankou tit, paragraf, lis, ak lyen. Nou te aprann tou sou eleman HTML semantik tankou `<header>`, `<main>`, ak `<footer>`. Jodi a, n ap aprann sou de atribi HTML ki gen pouvwa ki ede nou idantifye ak bay estil eleman espesifik: **class** ak **id**.

### Vokabilè

- **Atribi**: Enfòmasyon adisyonèl nou bay eleman HTML yo
- **Class**: Yon atribi ki ka aplike sou plizyè eleman pou gwoupman
- **ID**: Yon idantifyan inik pou yon sèl eleman
- **Selektè**: Yon modèl nou itilize nan CSS pou chwazi eleman pou estil
- **Kaskad**: Lòd kote règ CSS yo aplike
- **Espesifisite**: Pwa yo bay diferan selektè CSS
- **Gwoupman**: Aplike menm estil yo sou plizyè selektè
- **Chèn**: Konbine plizyè selektè pou vize eleman espesifik

[⬆ Retounen Anwo](#tab-matyè)

---

## Atribi Class HTML

Atribi **class** la pèmèt ou bay youn oswa plizyè eleman menm idantifyan an. Panse de li tankou mete yon etikèt sou bagay yo - plizyè atik ka gen menm etikèt la.

### Sentaks

```html
<element class="nonclass">Konteni</element>
```

### Pwen Kle sou Class yo

1. **Plizyè eleman** ka gen menm class la
2. Yon eleman ka gen **plizyè class** (separe pa espas)
3. Non class yo **sansib a majiskil/miniskil**
4. Non class yo ta dwe **deskriptif** ak gen sans

### Egzanp Kòd

#### Yon Sèl Class

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Egzanp Class</title>
    </head>
    <body>
        <p class="highlight">Paragraf sa a gen yon class highlight.</p>
        <p>Paragraf sa a pa gen class.</p>
        <p class="highlight">Paragraf sa a gen class highlight tou.</p>
    </body>
</html>
```

#### Plizyè Class sou Yon Eleman

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Plizyè Class</title>
    </head>
    <body>
        <p class="highlight important">Sa a gen de class!</p>
        <p class="highlight">Sa a gen yon class.</p>
        <p class="important large">Sa a gen de class diferan.</p>
    </body>
</html>
```

### Èd Vizyèl: Estrikti Atribi Class

```
<p class="warning-text">
 │    │        │
 │    │        └── Non class (ou chwazi sa a)
 │    └────────────── atribi class
 └────────────────────── eleman HTML
```

### Konvansyon pou Bay Non Class yo

- Itilize lèt miniskil
- Itilize tirè pou mo ki gen plizyè pati (egz., `main-content`)
- Fè yo deskriptif (egz., `error-message` pa sèlman `red`)
- Evite kòmanse ak nimewo

[⬆ Retounen Anwo](#tab-matyè)

---

## Atribi ID HTML

Atribi **id** la bay yon idantifyan inik pou yon eleman. Panse de li tankou nimewo sekirite sosyal yon moun - sèlman yon moun ka gen nimewo espesifik sa a.

### Sentaks

```html
<element id="nonid">Konteni</element>
```

### Pwen Kle sou ID yo

1. Chak id dwe **inik** nan tout dokiman HTML la
2. Yon eleman ka gen sèlman **yon** id
3. ID yo **sansib a majiskil/miniskil**
4. ID yo ka itilize pou **navigasyon** ak lyen ankraj

### Egzanp Kòd

#### Itilizasyon Bazik ID

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Egzanp ID</title>
    </head>
    <body>
        <header id="page-header">
            <h1>Byenveni sou Sit Mwen</h1>
        </header>

        <section id="main-content">
            <p>Sa a se zòn konteni prensipal la.</p>
        </section>

        <footer id="page-footer">
            <p>Copyright 2024</p>
        </footer>
    </body>
</html>
```

#### Itilize ID pou Navigasyon

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Navigasyon ak ID</title>
    </head>
    <body>
        <nav>
            <ul>
                <li><a href="#section1">Ale nan Seksyon 1</a></li>
                <li><a href="#section2">Ale nan Seksyon 2</a></li>
                <li><a href="#section3">Ale nan Seksyon 3</a></li>
            </ul>
        </nav>

        <section id="section1">
            <h2>Seksyon 1</h2>
            <p>Konteni pou seksyon 1...</p>
        </section>

        <section id="section2">
            <h2>Seksyon 2</h2>
            <p>Konteni pou seksyon 2...</p>
        </section>

        <section id="section3">
            <h2>Seksyon 3</h2>
            <p>Konteni pou seksyon 3...</p>
        </section>
    </body>
</html>
```

### Èd Vizyèl: ID kont Class

```
Class yo (ka pataje):
┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│ class="box" │  │ class="box" │  │ class="box" │
└─────────────┘  └─────────────┘  └─────────────┘
      ✓               ✓                ✓       (Tout bon!)

ID yo (dwe inik):
┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│ id="header"  │  │ id="content" │  │ id="footer"  │
└──────────────┘  └──────────────┘  └──────────────┘
      ✓                ✓                 ✓      (Tout diferan - Bon!)

┌──────────────┐  ┌──────────────┐
│ id="special" │  │ id="special" │
└──────────────┘  └──────────────┘
      ✓                ✗           (Menm ID - PA BON!)
```

[⬆ Retounen Anwo](#tab-matyè)

---

## Bay Estil Class ak ID

Kounye a ke nou konprann class ak ID, ann aprann kijan pou bay yo estil ak CSS!

### Selektè CSS pou Class ak ID

- **Selektè class**: Itilize yon pwen (`.`) swivi pa non class la
- **Selektè ID**: Itilize yon dyèz (`#`) swivi pa non id la

### Sentaks

```css
/* Selektè class */
.nonclass {
    pwopriyete: valè;
}

/* Selektè ID */
#nonid {
    pwopriyete: valè;
}
```

### Egzanp Konplè ak Estil

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Bay Estil Class ak ID</title>
        <style>
            /* Bay estil yon class */
            .highlight {
                background-color: yellow;
                padding: 5px;
            }

            .important {
                font-weight: bold;
                color: red;
            }

            /* Bay estil yon ID */
            #main-title {
                font-size: 36px;
                text-align: center;
                color: navy;
            }

            #special-paragraph {
                border: 2px solid green;
                padding: 10px;
                margin: 20px;
            }
        </style>
    </head>
    <body>
        <h1 id="main-title">Byenveni nan Estil CSS!</h1>

        <p class="highlight">Paragraf sa a gen highlight.</p>

        <p class="important">Tèks sa a enpòtan!</p>

        <p class="highlight important">Sa a gen tou de class yo aplike!</p>

        <p id="special-paragraph">
            Paragraf sa a gen yon ID espesyal ak estil inik.
        </p>
    </body>
</html>
```

### Èd Vizyèl: Estrikti Selektè CSS

```
Selektè Class:
.warning-text {
│      │
│      └── Non class (koresponn ak class="warning-text")
└────────── Pwen endike selektè class

Selektè ID:
#page-header {
│      │
│      └── Non ID (koresponn ak id="page-header")
└────────── Dyèz endike selektè ID
```

[⬆ Retounen Anwo](#tab-matyè)

---

## Règ Kaskad

**Kaskad** la nan CSS detèmine ki estil yo aplike lè plizyè règ vize menm eleman an. Konprann sa a enpòtan pou ekri CSS efikas.

### Yerachi Espesifisite

Soti nan **pi espesifik** (genyen) rive nan **mwens espesifik** (pèdi):

1. **Estil enliy** (atribi style) - Nou poko kouvri sa a
2. **ID yo** (#nonid)
3. **Class yo** (.nonclass)
4. **Eleman yo** (p, h1, div, etc.)

### Egzanp Espesifisite

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Règ Kaskad CSS</title>
        <style>
            /* Selektè eleman - mwens espesifik */
            p {
                color: blue;
                font-size: 14px;
            }

            /* Selektè class - pi espesifik */
            .special {
                color: green;
                font-size: 16px;
            }

            /* Selektè ID - pi espesifik */
            #unique {
                color: red;
                font-size: 18px;
            }
        </style>
    </head>
    <body>
        <!-- Sa a ap ble, 14px -->
        <p>Paragraf regilye</p>

        <!-- Sa a ap vèt, 16px (class bat eleman) -->
        <p class="special">Paragraf ak class</p>

        <!-- Sa a ap wouj, 18px (ID bat tout bagay) -->
        <p class="special" id="unique">Paragraf ak class E id</p>
    </body>
</html>
```

### Lòd Enpòtan Tou!

Lè selektè yo gen **menm espesifisite**, dènye a genyen:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Lòd Enpòtan</title>
        <style>
            .first {
                color: blue;
            }

            .second {
                color: red; /* Sa a genyen paske li vini dènye */
            }
        </style>
    </head>
    <body>
        <!-- Sa a ap wouj -->
        <p class="first second">Ki koulè mwen ye?</p>
        <p class="second first">Mwen wouj tou!</p>
    </body>
</html>
```

### Èd Vizyèl: Nechèl Espesifisite

```
Pi Espesifik (Genyen)
        ↑
    ┌───────┐
    │  ID   │  (Vo 100 pwen)
    └───────┘
        ↑
    ┌───────┐
    │ Class │  (Vo 10 pwen)
    └───────┘
        ↑
    ┌───────┐
    │Eleman │  (Vo 1 pwen)
    └───────┘
        ↑
Mwens Espesifik (Pèdi)
```

[⬆ Retounen Anwo](#tab-matyè)

---

## Gwoupman ak Chèn

### Gwoupman Selektè yo

**Gwoupman** pèmèt ou aplike menm estil yo sou plizyè selektè lè w separe yo ak vigil.

#### Sentaks

```css
selektè1, selektè2, selektè3 {
    pwopriyete: valè;
}
```

#### Egzanp

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Gwoupman Selektè</title>
        <style>
            /* San gwoupman - repete twòp */
            /*
            h1 {
                color: navy;
                font-family: Arial;
            }
            h2 {
                color: navy;
                font-family: Arial;
            }
            h3 {
                color: navy;
                font-family: Arial;
            }
            */

            /* Ak gwoupman - pi pwòp! */
            h1, h2, h3 {
                color: navy;
                font-family: Arial;
            }

            /* Gwoupman diferan tip selektè */
            #special, .highlight, p {
                margin: 10px;
                padding: 5px;
            }
        </style>
    </head>
    <body>
        <h1>Tit 1</h1>
        <h2>Tit 2</h2>
        <h3>Tit 3</h3>
        <p>Yon paragraf</p>
        <p class="highlight">Paragraf ak highlight</p>
        <p id="special">Paragraf espesyal</p>
    </body>
</html>
```

### Chèn Selektè

**Chèn** pèmèt ou vize eleman ki ranpli plizyè kritè lè w konbine selektè san espas.

#### Sentaks pou Chèn Class

```css
.class1.class2 {
    pwopriyete: valè;
}
```

#### Egzanp

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Chèn Selektè</title>
        <style>
            /* Vize eleman ak class="warning" */
            .warning {
                font-weight: bold;
            }

            /* Vize eleman ak class="text" */
            .text {
                font-family: Arial;
            }

            /* Vize SÈLMAN eleman ki gen TOU DE class yo */
            .warning.text {
                color: red;
                background-color: yellow;
            }

            /* Chèn eleman ak class */
            p.highlight {
                background-color: lightblue;
            }

            /* Sa a p ap afekte eleman div ak class highlight */
            div.highlight {
                background-color: lightgreen;
            }
        </style>
    </head>
    <body>
        <p class="warning">Sèlman class warning - fonse sèlman</p>
        <p class="text">Sèlman class text - fon Arial sèlman</p>
        <p class="warning text">Tou de class - tèks wouj sou jòn!</p>

        <p class="highlight">Paragraf ak highlight - ble klè</p>
        <div class="highlight">Div ak highlight - vèt klè</div>
    </body>
</html>
```

### Èd Vizyèl: Gwoupman kont Chèn

```
GWOUPMAN (ak vigil):
.class1, .class2 { }
   ↓       ↓
Aplike sou eleman ak class1 OSWA class2

CHÈN (san espas):
.class1.class2 { }
   ↓    ↓
Aplike sou eleman ak class1 E class2

Egzanp:
<p class="big">         Match: .big ✓, .big, .red ✓
<p class="red">         Match: .red ✓, .big, .red ✓
<p class="big red">     Match: .big ✓, .red ✓, .big.red ✓, .big, .red ✓
```

[⬆ Retounen Anwo](#tab-matyè)

---

## Rezime

### Pwen Kle yo

1. **Class yo** (`.nonclass`)
    - Ka itilize sou plizyè eleman
    - Yon eleman ka gen plizyè class
    - Pafè pou bay estil gwoup eleman ki sanble

2. **ID yo** (`#nonid`)
    - Dwe inik nan dokiman an
    - Chak eleman ka gen sèlman yon ID
    - Bon pou eleman inik ak ankraj navigasyon

3. **Kaskad ak Espesifisite**
    - Selektè ID pi espesifik pase selektè class
    - Selektè class pi espesifik pase selektè eleman
    - Lè espesifisite egal, dènye règ la genyen

4. **Gwoupman** (`,`)
    - Itilize vigil pou aplike menm estil yo sou plizyè selektè
    - Diminye repetisyon kòd

5. **Chèn**
    - Konbine selektè san espas pou vize eleman espesifik
    - Itil pou eleman ki ranpli plizyè kritè

### Bon Pratik

- Itilize non **semantik** (ki gen sans) pou class ak ID
- Itilize **class** pou estil ki ka reutilize
- Itilize **ID** rarman e sèlman pou eleman inik
- Kenbe CSS ou **òganize** epi evite repetisyon
- **Teste** estil ou yo nan navigatè souvan

[⬆ Retounen Anwo](#tab-matyè)

---

## Resous

### Dokimantasyon

- [MDN Web Docs - Atribi Class](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/class)
- [MDN Web Docs - Atribi ID](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id)
- [MDN Web Docs - Selektè CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)

### Titoryèl W3Schools

- [Class HTML](https://www.w3schools.com/html/html_classes.asp)
- [ID HTML](https://www.w3schools.com/html/html_id.asp)
- [Selektè CSS](https://www.w3schools.com/css/css_selectors.asp)
- [Espesifisite CSS](https://www.w3schools.com/css/css_specificity.asp)

### Zouti

- **WebStorm**: IDE ou pou ekri HTML ak CSS
- **Git**: Kontwòl vèsyon pou swiv chanjman yo
- **GitHub**: Ebèje kòd repozitwa ou yo

[⬆ Retounen Anwo](#tab-matyè)