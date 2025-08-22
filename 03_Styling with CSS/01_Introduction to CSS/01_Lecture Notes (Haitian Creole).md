# Entwodiksyon nan CSS - Nòt Kou

## Tab Matyè

| Sijè | Deskripsyon |
|-------|-------------|
| [1. Kisa CSS ye?](#1-kisa-css-ye) | Konprann CSS ak wòl li nan devlopman entènèt |
| [2. Ti Istwa CSS](#2-ti-istwa-css) | Evolisyon ak vèsyon CSS |
| [3. Fòma Selektè CSS](#3-fòma-selektè-css) | Sentaks ak estrikti debaz |
| [4. CSS Aliy](#4-css-aliy) | Estil dirèkteman nan eleman HTML |
| [5. CSS Entèn](#5-css-entèn) | Estil nan dokiman HTML |
| [6. CSS Ekstèn](#6-css-ekstèn) | Konekte fichye CSS separe |
| [Vokabilè](#vokabilè) | Tèm ak definisyon kle |
| [Devwa Pwogramasyon](#devwa-pwogramasyon) | Egzèsis pratik |
| [Rezime](#rezime) | Pwen kle yo |
| [Resous](#resous) | Materyèl aprantisaj adisyonèl |

---

## 1. Kisa CSS ye?

[⬆ Retounen Anwo](#tab-matyè)

### Definisyon
**CSS** vle di **Cascading Style Sheets** (Fèy Estil Kaskad). Se yon langaj estil yo itilize pou dekri kijan eleman HTML yo dwe parèt sou yon paj entènèt.

### Objektif
Panse HTML tankou eskèlèt yon paj entènèt - li bay estrikti. CSS se tankou rad ak makiyaj - li fè tout bagay vin bèl!

### Relasyon ant HTML ak CSS

```
HTML = Estrikti (Ki kontni ki parèt)
CSS = Prezantasyon (Kijan kontni an parèt)
```

### Analoji Vizyèl
Imajine w ap konstwi yon kay:
- **HTML** = Ankadreman, mi yo ak chanm yo (estrikti)
- **CSS** = Penti, dekorasyon ak mèb (estil)

### Poukisa Itilize CSS?
1. **Separasyon Pwoblèm**: Kenbe estrikti (HTML) separe ak prezantasyon (CSS)
2. **Ka Reutilize**: Yon règ CSS ka bay estil a plizyè eleman HTML
3. **Konsistans**: Kenbe estil inifòm sou tout sit entènèt ou
4. **Efikasite**: Chanje aparans santèn paj lè w edite yon sèl fichye CSS

---

## 2. Ti Istwa CSS

[⬆ Retounen Anwo](#tab-matyè)

### Liy Tan

| Ane | Vèsyon | Karakteristik Kle |
|------|---------|--------------|
| 1996 | CSS1 | Estil debaz: polis, koulè, espas |
| 1998 | CSS2 | Pozisyonman, tip medya |
| 2011 | CSS3 | Animasyon, degrade, lonbraj, konsèpsyon reponsiv |
| Kounye a | CSS3+ | Aktyalizasyon modilè kontinye |

### Anvan CSS
Nan premye jou entènèt la, tout estil te fèt dirèkteman nan HTML lè yo te itilize atribi tankou:
```html
<font color="red">Sa se tèks wouj</font>
```
Sa te fè sit entènèt yo difisil pou kenbe ak aktyalize!

### Poukisa Yo Te Kreye CSS
- Pou rezoud pwoblèm melanje kontni ak prezantasyon
- Pou bay konseptè entènèt plis kontwòl sou aranjman
- Pou diminye kòd repetitif

---

## 3. Fòma Selektè CSS

[⬆ Retounen Anwo](#tab-matyè)

### Sentaks Debaz CSS

Chak règ CSS gen de pati prensipal:

```css
selektè {
    pwopriyete: valè;
}
```

### Konpozan Eksplike

1. **Selektè**: Ki eleman HTML pou bay estil
2. **Pwopriyete**: Ki aspè pou chanje (koulè, gwosè, elatriye)
3. **Valè**: Kisa pou chanje li
4. **Deklarasyon**: Yon pè pwopriyete-valè
5. **Blòk Deklarasyon**: Tout sa ki nan bouklèt `{}`

### Dyagram Vizyèl

```
    selektè
       ↓
    h1 {
        color: blue;     ← deklarasyon
        ↑       ↑
    pwopriyete valè
        
        font-size: 24px; ← yon lòt deklarasyon
    }
    ↑                 ↑
    bouklèt         bouklèt
    ouvri           fèmen
```

### Plizyè Deklarasyon
Ou ka gen plizyè deklarasyon nan yon règ:

```css
p {
    color: navy;
    font-size: 16px;
    line-height: 1.5;
}
```

### Kòmantè nan CSS
Itilize `/* */` pou ajoute kòmantè:

```css
/* Sa se yon kòmantè nan CSS */
h1 {
    color: green; /* Sa fè tit yo vèt */
}
```

---

## 4. CSS Aliy

[⬆ Retounen Anwo](#tab-matyè)

### Definisyon
CSS aliy se CSS ki ekri dirèkteman nan yon eleman HTML lè w itilize atribi `style`.

### Sentaks
```html
<etikèt style="pwopriyete: valè;">Kontni</etikèt>
```

### Egzanp

#### Egzanp 1: Bay Estil yon Paragraf
```html
<p style="color: red;">Tèks sa a wouj!</p>
```

#### Egzanp 2: Plizyè Pwopriyete
```html
<h1 style="color: blue; font-size: 36px;">Gwo Tit Ble</h1>
```

#### Egzanp 3: Bay Estil Diferan Eleman
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp CSS Aliy</title>
</head>
<body>
    <h1 style="color: purple;">Byenveni!</h1>
    <p style="color: green; font-size: 18px;">Sa se yon paragraf vèt.</p>
    <p style="background-color: yellow;">Sa gen yon background jòn.</p>
</body>
</html>
```

### Pwopriyete Komen pou CSS Aliy

| Pwopriyete | Deskripsyon | Valè Egzanp |
|----------|-------------|----------------|
| `color` | Koulè tèks | `red`, `#FF0000`, `rgb(255,0,0)` |
| `background-color` | Koulè background | `yellow`, `#FFFF00` |
| `font-size` | Gwosè tèks | `16px`, `1.5em`, `large` |
| `text-align` | Aliyman tèks | `left`, `center`, `right` |
| `font-family` | Tip polis | `Arial`, `"Times New Roman"` |

### Avantaj ak Dezavantaj

**Avantaj:**
- Rapid pou tès
- Ranplase lòt CSS (pi wo espesifisite)
- Pa bezwen fichye ekstèn

**Dezavantaj:**
- Pa ka reutilize
- Melanje prezantasyon ak kontni
- Difisil pou kenbe
- Fè HTML vin sal

---

## 5. CSS Entèn

[⬆ Retounen Anwo](#tab-matyè)

### Definisyon
CSS entèn (yo rele tou CSS entegre) ekri nan seksyon `<head>` yon dokiman HTML lè w itilize etikèt `<style>`.

### Sentaks
```html
<head>
    <style>
        selektè {
            pwopriyete: valè;
        }
    </style>
</head>
```

### Egzanp Konplè
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp CSS Entèn</title>
    <style>
        h1 {
            color: navy;
            text-align: center;
        }
        
        p {
            color: gray;
            font-size: 16px;
            line-height: 1.6;
        }
        
        strong {
            color: red;
        }
    </style>
</head>
<body>
    <h1>Byenveni sou Sit Entènèt Mwen</h1>
    <p>Sa se yon paragraf ak tèks <strong>enpòtan</strong>.</p>
    <p>Tout paragraf yo ap gen menm estil!</p>
</body>
</html>
```

### Selektè Eleman
Chwazi eleman HTML pa non etikèt yo:

```css
h1 { color: blue; }
p { font-size: 14px; }
em { font-style: italic; }
strong { font-weight: bold; }
```

### Bay Estil Plizyè Eleman
Aplike menm estil a plizyè eleman:

```css
h1, h2, h3 {
    font-family: Arial;
    color: darkblue;
}
```

### Avantaj ak Dezavantaj

**Avantaj:**
- Estil aplike sou tout paj la
- Kenbe estil separe ak kontni HTML
- Ka reutilize estil pou plizyè eleman

**Dezavantaj:**
- Sèlman travay pou yon paj HTML
- Pa ka reutilize sou diferan paj
- Ogmante gwosè fichye paj la

---

## 6. CSS Ekstèn

[⬆ Retounen Anwo](#tab-matyè)

### Definisyon
CSS ekstèn ekri nan yon fichye `.css` separe epi konekte ak dokiman HTML.

### Kreye Lyen an
Itilize etikèt `<link>` nan seksyon `<head>`:

```html
<link rel="stylesheet" href="styles.css">
```

### Egzanp Estrikti Fichye
```
sit-entènèt-mwen/
│
├── index.html
├── about.html
├── contact.html
└── styles.css
```

### Fichye HTML (index.html)
```html
<!DOCTYPE html>
<html>
<head>
    <title>Sit Entènèt Mwen</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Byenveni sou Sit Mwen</h1>
    </header>
    <main>
        <section>
            <h2>Konsènan Nou</h2>
            <p>Nou kreye sit entènèt enkyab!</p>
        </section>
    </main>
    <footer>
        <p>© 2024 Sit Entènèt Mwen</p>
    </footer>
</body>
</html>
```

### Fichye CSS (styles.css)
```css
/* Reyinisyalize maj pa defo */
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

/* Estil antèt */
header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
}

/* Estil kontni prensipal */
main {
    padding: 20px;
}

section {
    margin-bottom: 30px;
}

h2 {
    color: #333;
    border-bottom: 2px solid #333;
    padding-bottom: 5px;
}

/* Estil pye paj */
footer {
    background-color: #f0f0f0;
    text-align: center;
    padding: 10px;
    color: #666;
}
```

### Konekte CSS soti nan Diferan Katab

#### CSS nan yon sou-katab:
```
sit-entènèt-mwen/
│
├── index.html
└── css/
    └── styles.css
```

Lyen: `<link rel="stylesheet" href="css/styles.css">`

#### CSS nan katab paran:
```
sit-entènèt-mwen/
│
├── styles.css
└── pages/
    └── about.html
```

Lyen soti nan about.html: `<link rel="stylesheet" href="../styles.css">`

### Plizyè Fichye CSS
Ou ka konekte plizyè fichye CSS:

```html
<link rel="stylesheet" href="css/reset.css">
<link rel="stylesheet" href="css/layout.css">
<link rel="stylesheet" href="css/colors.css">
```

### Avantaj ak Dezavantaj

**Avantaj:**
- Separasyon konplè ant kontni ak prezantasyon
- Ka reutilize sou plizyè paj HTML
- Fichye HTML pi piti
- Ka mete nan kach pa navigatè (chaje pi rapid)
- Fasil pou kenbe ak aktyalize

**Dezavantaj:**
- Mande yon demann HTTP adisyonèl
- Kapab koze yon flash kontni san estil (FOUC)

---

## Vokabilè

[⬆ Retounen Anwo](#tab-matyè)

| Tèm | Definisyon |
|------|------------|
| **CSS** | Cascading Style Sheets - langaj pou bay estil HTML |
| **Selektè** | Idantifye ki eleman HTML pou bay estil |
| **Pwopriyete** | Aspè yon eleman ou vle chanje |
| **Valè** | Sa ou vle chanje pwopriyete a |
| **Deklarasyon** | Yon pè pwopriyete-valè (egz., `color: blue;`) |
| **Blòk Deklarasyon** | Gwoup deklarasyon nan bouklèt |
| **CSS Aliy** | CSS ekri dirèkteman nan eleman HTML ak atribi `style` |
| **CSS Entèn** | CSS ekri nan etikèt `<style>` nan `<head>` HTML |
| **CSS Ekstèn** | CSS ekri nan fichye `.css` separe |
| **Kaskad** | Lòd règ CSS yo aplike |
| **Fèy Estil** | Yon koleksyon règ CSS |
| **Etikèt Link** | Eleman HTML yo itilize pou konekte fichye CSS ekstèn |
| **Espesifisite** | Règ ki detèmine ki règ CSS aplike lè plizyè règ vize menm eleman |

---

## Devwa Pwogramasyon

[⬆ Retounen Anwo](#tab-matyè)

### Devwa 1: Paj Pwofil Pèsonèl
Kreye yon paj pwofil pèsonèl lè w itilize **sèlman CSS aliy**. Bay estil omwen 5 eleman diferan.

**Kondisyon:**
- Itilize h1 pou non ou
- Itilize etikèt p pou enfòmasyon biyografik
- Mete yon lis (ul oswa ol) pasa yo
- Bay chak eleman estil diferan ak CSS aliy
- Itilize omwen 3 pwopriyete CSS diferan

[Modèl Devwa 1](assignment1-template.md) | [Solisyon Devwa 1](assignment1-solution.md)

### Devwa 2: Paj Resèt
Kreye yon paj resèt lè w itilize **sèlman CSS entèn**.

**Kondisyon:**
- Itilize bon estrikti HTML (header, main, footer)
- Mete tit resèt (h1), engredyan (ul) ak enstriksyon (ol)
- Bay tout tit yo menm estil
- Bay tout paragraf yo menm estil
- Itilize omwen 5 pwopriyete CSS diferan

[Modèl Devwa 2](assignment2-template.md) | [Solisyon Devwa 2](assignment2-solution.md)

### Devwa 3: Sit Entènèt Plizyè Paj
Kreye yon sit entènèt 3 paj lè w itilize **CSS ekstèn**.

**Kondisyon:**
- Kreye home.html, about.html, ak contact.html
- Kreye yon fichye styles.css
- Konekte tout paj yo ak menm fichye CSS
- Mete lyen navigasyon ant paj yo
- Bay antèt, paragraf ak lyen estil konsistan

[Modèl Devwa 3](Assignment/Assignment.md) | [Solisyon Devwa 3](assignment3-solution.md)

---

## Rezime

[⬆ Retounen Anwo](#tab-matyè)

### Pwen Kle yo

1. **CSS fè sit entènèt vin bèl** - Li kontwole koulè, polis, espas ak aranjman
2. **Twa fason pou ajoute CSS**:
   - **Aliy**: Rapid men pa ka reutilize
   - **Entèn**: Bon pou paj endividyèl
   - **Ekstèn**: Pi bon pou sit entènèt plizyè paj
3. **Sentaks CSS konsistan**: `selektè { pwopriyete: valè; }`
4. **Separasyon pwoblèm** - Kenbe estrikti (HTML) separe ak estil (CSS)
5. **CSS ekstèn jeneralman pi bon** pou vrè sit entènèt paske li:
   - Ka reutilize sou paj yo
   - Fasil pou kenbe
   - Kenbe HTML pwòp

### Priyorite CSS (Kaskad)
Lè plizyè règ CSS aplike sou menm eleman:
1. **CSS aliy** (priyorite pi wo)
2. **CSS entèn**
3. **CSS ekstèn** (priyorite pi ba)

### Pi Bon Pratik
- Kòmanse ak CSS ekstèn pou konsistans
- Itilize CSS entèn pou estil espesifik paj
- Itilize CSS aliy avèk modèr (sèlman pou tès oswa ranplasman)
- Kenbe CSS ou òganize ak kòmantè
- Itilize non ki gen sans pou fichye CSS ou

---

## Resous

[⬆ Retounen Anwo](#tab-matyè)

### Dokimantasyon
- [Dokimantasyon CSS MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [Tutorial CSS W3Schools](https://www.w3schools.com/css/)
- [Referans CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

### Referans Pwopriyete CSS
- [Pwopriyete CSS W3Schools](https://www.w3schools.com/cssref/)
- [Endèks Pwopriyete CSS MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)

### Zouti
- **WebStorm**: IDE ou pou ekri HTML ak CSS
- **Git**: Kontwòl vèsyon pou swiv chanjman
- **GitHub**: Ebèje ak pataje kòd ou

### Resous Pratik
- [Egzèsis CSS W3Schools](https://www.w3schools.com/css/exercise.asp)
- [Baz CSS sou MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics)

### Pwochèn Etap
Apre ou metrize baz sa yo, w ap aprann sou:
- Selektè klas ak ID
- Modèl bwat
- Aranjman Flexbox ak Grid
- Konsèpsyon reponsiv
- Animasyon CSS

---

*Sonje: Pi bon fason pou aprann CSS se pratike! Kòmanse ak estil senp epi piti piti ajoute plis konplikasyon pandan w vin alèz.*