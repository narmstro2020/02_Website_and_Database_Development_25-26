# Koulè, Inite ak Polis CSS - Nòt Kou

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

## Tab Matyè

| Sijè | Deskripsyon |
|------|-------------|
| [Entwodiksyon](#entwodiksyon) | Apèsi koulè, inite ak polis CSS |
| [Koulè CSS](#koulè-css) | RGB, RGBA, HSL, HSLA, Egzadesimal ak Koulè ki gen Non |
| [Inite CSS](#inite-css) | Inite Absoli ak Relatif |
| [Polis CSS](#polis-css) | Pwopriyete Polis ak Tipografi Entènèt |
| [Vokabilè](#vokabilè) | Tèm kle ak definisyon |
| [Devwa](#devwa) | Egzèsis pratik |
| [Rezime](#rezime) | Pwen enpòtan pou sonje |
| [Resous](#resous) | Materyèl aprantisaj adisyonèl |

---

## Entwodiksyon

Nan leson sa a, nou pral eksplore twa aspè fondamantal estil CSS ki pral transfòme paj entènèt ou yo soti nan tèks senp pou vin desen ki atiran vizyèlman. W ap aprann kijan pou ajoute koulè, kontwole gwosè ak diferan inite epi estilize tèks ak plizyè pwopriyete polis.

### Kondisyon Anvan
- Estrikti dokiman HTML (DOCTYPE, html, head, body)
- Baliz HTML debaz (h1-h6, p, em, strong)
- HTML semantik (header, footer, main, section, article)
- Lis (ul, ol, li)
- Lyen ak imaj
- Sentaks CSS debaz ak selektè nan leson anvan yo

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

---

## Koulè CSS

CSS bay plizyè fason pou espesifye koulè. Chak metòd gen avantaj ak ka itilizasyon li.

### 1. Koulè ki gen Non

CSS sipòte 140 non koulè estanda ke ou ka itilize dirèkteman.

```css
/* Itilize koulè ki gen non */
p {
    color: red;
    background-color: lightblue;
}

h1 {
    color: darkgreen;
    background-color: gold;
}
```

**Koulè ki gen Non Komen:**
- Primè: red, blue, green, yellow
- Net: black, white, gray, silver
- Pwolonje: coral, salmon, turquoise, violet

### 2. Koulè Egzadesimal

Koulè egzadesimal (hex) itilize yon # swivi pa 6 karaktè (0-9 ak A-F).

```css
/* Fòma koulè egzadesimal: #RRVVBB */
p {
    color: #FF0000;      /* Wouj pi */
    background-color: #00FF00;  /* Vèt pi */
}

h1 {
    color: #0000FF;      /* Ble pi */
    background-color: #FFFFFF;  /* Blan */
}

/* Hex abreje (lè pè yo matche) */
h2 {
    color: #F00;        /* Menm jan ak #FF0000 */
    background-color: #0F0;     /* Menm jan ak #00FF00 */
}
```

**Konprann Koulè Hex:**
- De premye karaktè: Valè wouj (00-FF)
- De karaktè nan mitan: Valè vèt (00-FF)
- De dènye karaktè: Valè ble (00-FF)
- 00 = pa gen koulè, FF = maksimòm koulè

### 3. Koulè RGB

RGB itilize valè desimal de 0-255 pou Wouj, Vèt ak Ble.

```css
/* Fòma koulè RGB: rgb(wouj, vèt, ble) */
p {
    color: rgb(255, 0, 0);      /* Wouj pi */
    background-color: rgb(0, 255, 0);   /* Vèt pi */
}

h1 {
    color: rgb(0, 0, 255);      /* Ble pi */
    background-color: rgb(128, 128, 128); /* Gri */
}

/* Melanje koulè */
h2 {
    color: rgb(255, 165, 0);    /* Zoranj */
    background-color: rgb(128, 0, 128);  /* Mov */
}
```

### 4. Koulè RGBA

RGBA ajoute yon chanèl alfa pou transparans (0 = konplètman transparan, 1 = konplètman opak).

```css
/* Fòma RGBA: rgba(wouj, vèt, ble, alfa) */
p {
    background-color: rgba(255, 0, 0, 0.5);   /* Wouj 50% transparan */
}

section {
    background-color: rgba(0, 0, 255, 0.3);   /* Ble 30% opak */
}

/* Kouch ak transparans */
header {
    background-color: rgba(0, 0, 0, 0.8);     /* Nwa 80% opak */
    color: rgba(255, 255, 255, 1);            /* Blan konplètman opak */
}
```

### 5. Koulè HSL

HSL vle di Tèn, Satiasyon ak Limyè - yon modèl koulè ki pi entwitif.

```css
/* Fòma HSL: hsl(tèn, satiasyon%, limyè%) */
p {
    color: hsl(0, 100%, 50%);      /* Wouj */
    background-color: hsl(120, 100%, 50%);  /* Vèt */
}

h1 {
    color: hsl(240, 100%, 50%);    /* Ble */
}

/* Kreye varyasyon koulè */
section {
    background-color: hsl(200, 50%, 70%);   /* Ble klè */
}
```

**Konprann HSL:**
- Tèn: 0-360 degre sou wou koulè a (0=wouj, 120=vèt, 240=ble)
- Satiasyon: 0% = gri, 100% = koulè konplè
- Limyè: 0% = nwa, 50% = nòmal, 100% = blan

### 6. Koulè HSLA

HSLA ajoute transparans ak koulè HSL.

```css
/* Fòma HSLA: hsla(tèn, satiasyon%, limyè%, alfa) */
article {
    background-color: hsla(60, 100%, 50%, 0.5);  /* Jòn 50% transparan */
}

footer {
    background-color: hsla(0, 0%, 0%, 0.9);      /* Nwa 90% opak */
}
```

### Gid Vizyèl Koulè

```css
/* Egzanp konplè koulè */
body {
    background-color: #f0f0f0;  /* Fon gri klè */
}

header {
    background-color: rgb(51, 51, 51);  /* Gri fonse */
    color: white;
}

main {
    background-color: rgba(255, 255, 255, 0.95);  /* Blan yon ti kras transparan */
}

footer {
    background-color: hsl(210, 50%, 30%);  /* Ble fonse */
    color: hsla(0, 0%, 100%, 0.9);  /* Blan yon ti kras transparan */
}
```

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

---

## Inite CSS

Inite CSS detèmine gwosè eleman yo. Yo divize an de kategori: absoli ak relatif.

### Inite Absoli

Inite absoli gen yon gwosè fiks kèlkeswa lòt paramèt yo.

#### Piksèl (px)
Inite absoli ki pi komen pou ekran.

```css
p {
    font-size: 16px;
    margin: 20px;
    padding: 10px;
}

h1 {
    font-size: 32px;
    margin-bottom: 24px;
}

img {
    width: 300px;
    height: 200px;
}
```

#### Lòt Inite Absoli
Yo pa itilize yo souvan men yo disponib:

```css
/* Inite absoli yo raman itilize */
p {
    margin: 0.5in;    /* pous */
    padding: 1cm;     /* santimèt */
    border: 2mm;      /* milimèt */
    width: 12pt;      /* pwen (1pt = 1/72 pous) */
    height: 1pc;      /* pika (1pc = 12pt) */
}
```

### Inite Relatif

Inite relatif adapte selon lòt valè, sa fè desen yo pi fleksib.

#### Pousantaj (%)
Relatif ak gwosè eleman paran an.

```css
/* Inite pousantaj */
section {
    width: 80%;           /* 80% lajè paran an */
    margin: 0 auto;       /* Santre seksyon an */
}

article {
    width: 50%;           /* Mwatye lajè paran an */
    padding: 5%;          /* 5% lajè paran an */
}

img {
    width: 100%;          /* Lajè konplè veso a */
    height: auto;         /* Kenbe rapò aspè */
}
```

#### Inite Em (em)
Relatif ak gwosè polis eleman an (oswa gwosè polis paran an pou lòt pwopriyete).

```css
/* Inite em */
p {
    font-size: 1em;       /* Menm jan ak gwosè polis paran an */
    margin: 1.5em;        /* 1.5 fwa gwosè polis la */
    padding: 0.5em;       /* Mwatye gwosè polis la */
}

h1 {
    font-size: 2em;       /* De fwa gwosè polis paran an */
    margin-bottom: 0.5em; /* Mwatye gwosè polis h1 */
}

/* Valè em an kaskad */
body {
    font-size: 16px;
}

article {
    font-size: 1.2em;     /* 19.2px (16px × 1.2) */
}

article p {
    font-size: 1.1em;     /* 21.12px (19.2px × 1.1) */
}
```

#### Inite Rem (rem)
Relatif ak gwosè polis eleman rasin lan (anjeneral html).

```css
/* Inite rem - pi previzib pase em */
html {
    font-size: 16px;      /* Gwosè debaz */
}

p {
    font-size: 1rem;      /* 16px */
    margin: 1.5rem;       /* 24px */
}

h1 {
    font-size: 2.5rem;    /* 40px */
    margin-bottom: 1rem;  /* 16px */
}

h2 {
    font-size: 2rem;      /* 32px */
}
```

#### Inite Viewport
Relatif ak gwosè viewport navigatè a.

```css
/* Inite viewport */
header {
    width: 100vw;         /* 100% lajè viewport */
    height: 10vh;         /* 10% wotè viewport */
}

h1 {
    font-size: 5vw;       /* 5% lajè viewport */
}

section {
    min-height: 100vh;    /* Wotè minimòm viewport konplè */
    padding: 5vw;         /* Padding responsif */
}

/* vmin ak vmax */
article {
    width: 80vmin;        /* 80% pi piti dimansyon viewport */
    font-size: 2vmax;     /* 2% pi gwo dimansyon viewport */
}
```

### Chwazi Bon Inite a

```css
/* Pi bon pratik pou diferan ka itilizasyon */

/* Gwosè fiks - itilize px */
img {
    border: 2px solid black;
}

/* Tipografi - itilize rem pou konsistans */
body {
    font-size: 1rem;
}

h1 {
    font-size: 2.5rem;
}

/* Aranjman - itilize % oswa inite viewport */
main {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

/* Espas - itilize em oswa rem */
p {
    margin-bottom: 1em;
    padding: 1rem;
}
```

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

---

## Polis CSS

Tipografi enpòtan anpil pou desen entènèt. CSS bay kontwòl konplè sou aparans tèks.

### Fanmi Polis

Espesifye ki polis pou itilize. Toujou bay polis rezèv.

```css
/* Fanmi polis ak polis rezèv */
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1 {
    font-family: Georgia, 'Times New Roman', serif;
}

p {
    font-family: 'Courier New', Courier, monospace;
}

/* Itilize kòt pou non polis ki gen espas */
article {
    font-family: 'Segoe UI', Tahoma, sans-serif;
}
```

#### Fanmi Polis Jenerik
Toujou fini ak yon fanmi jenerik kòm dènye rezèv:
- **serif**: Times New Roman, Georgia (trete dekoratif)
- **sans-serif**: Arial, Helvetica (san trete dekoratif)
- **monospace**: Courier New, Consolas (lajè karaktè egal)
- **cursive**: Comic Sans MS (estil ekriti)
- **fantasy**: Impact (dekoratif)

### Gwosè Polis

Kontwole gwosè tèks lè w itilize nenpòt inite CSS.

```css
/* Diferan inite gwosè polis */
p {
    font-size: 16px;      /* Gwosè absoli */
}

h1 {
    font-size: 2.5rem;    /* Relatif ak rasin */
}

h2 {
    font-size: 2em;       /* Relatif ak paran */
}

/* Gwosè mo kle */
small {
    font-size: small;     /* Gwosè predefini */
}

h3 {
    font-size: larger;    /* Mo kle relatif */
}
```

### Pwa Polis

Kontwole epesè karaktè yo.

```css
/* Valè pwa polis */
p {
    font-weight: normal;  /* Menm jan ak 400 */
}

strong {
    font-weight: bold;    /* Menm jan ak 700 */
}

h1 {
    font-weight: 900;     /* Ekstra fonse */
}

h2 {
    font-weight: 300;     /* Lejè */
}

/* Valè nimerik: 100-900 */
h3 {
    font-weight: 600;     /* Semi-fonse */
}
```

### Estil Polis

Kontwole tèks italik oswa oblik.

```css
/* Opsyon estil polis */
p {
    font-style: normal;
}

em {
    font-style: italic;
}

footer {
    font-style: oblique;  /* Tèks panche */
}
```

### Dekorasyon Tèks

Ajoute liy nan tèks.

```css
/* Dekorasyon tèks */
a {
    text-decoration: underline;
}

h1 {
    text-decoration: none;
}

/* Plizyè dekorasyon */
h2 {
    text-decoration: underline overline;
}

/* Estil dekorasyon */
p {
    text-decoration: underline wavy red;
}
```

### Transfòmasyon Tèks

Chanje kapitalizasyon tèks.

```css
/* Transfòmasyon tèks */
h1 {
    text-transform: uppercase;   /* TOUT AN MAJISKIL */
}

h2 {
    text-transform: lowercase;   /* tout an miniskil */
}

h3 {
    text-transform: capitalize;  /* Premye Lèt Chak Mo */
}

p {
    text-transform: none;        /* Tèks nòmal */
}
```

### Wotè Liy

Kontwole espas ant liy tèks yo.

```css
/* Wotè liy */
p {
    line-height: 1.5;     /* 1.5 fwa gwosè polis */
}

body {
    line-height: 1.6;     /* Bon pou li fasil */
}

h1 {
    line-height: 1.2;     /* Pi sere pou tit */
}

/* Itilize inite */
article {
    line-height: 24px;    /* Wotè fiks */
}
```

### Espas Lèt ak Mo

Kontwole espas ant lèt ak mo.

```css
/* Espas lèt */
h1 {
    letter-spacing: 2px;
}

p {
    letter-spacing: 0.5px;
}

/* Espas mo */
p {
    word-spacing: 5px;
}

h2 {
    word-spacing: -2px;  /* Negatif fè mo yo vin pi pre */
}
```

### Aliyman Tèks

Kontwole aliyman orizontal tèks.

```css
/* Aliyman tèks */
h1 {
    text-align: center;
}

p {
    text-align: left;     /* Pa defo pou lang LTR */
}

footer {
    text-align: right;
}

article {
    text-align: justify;  /* Etann liy yo nan lajè konplè */
}
```

### Egzanp Konplè Polis

```css
/* Estil polis konplè */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 16px;
    line-height: 1.6;
    color: #333333;
}

h1 {
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 2.5rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
    text-align: center;
    color: #2c3e50;
    line-height: 1.2;
}

h2 {
    font-family: inherit;  /* Pran nan paran */
    font-size: 2rem;
    font-weight: 600;
    color: #34495e;
    margin-bottom: 1rem;
}

p {
    font-size: 1rem;
    line-height: 1.8;
    text-align: justify;
    margin-bottom: 1em;
}

em {
    font-style: italic;
    color: #e74c3c;
}

strong {
    font-weight: bold;
    color: #c0392b;
}

a {
    color: #3498db;
    text-decoration: none;
    font-weight: 500;
}

/* Efè hover pou lyen */
a:hover {
    text-decoration: underline;
    color: #2980b9;
}
```

### Polis Entènèt

Menmsi nou pa itilize sèvis ekstèn, ou ka itilize polis sistèm lan yon fason kreyatif:

```css
/* Pil polis sistèm pou diferan sistèm operasyon */
body {
    /* Polis sistèm modèn */
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 
                 Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 
                 'Helvetica Neue', sans-serif;
}

/* Polis sistèm monospace */
pre {
    font-family: 'SF Mono', Monaco, 'Cascadia Code', 
                 'Roboto Mono', Consolas, 'Courier New', 
                 monospace;
}
```

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

---

## Vokabilè

### Tèm Koulè
- **RGB**: Modèl koulè Wouj, Vèt, Ble itilize valè 0-255
- **RGBA**: RGB ak chanèl Alfa (transparans)
- **HSL**: Modèl koulè Tèn, Satiasyon, Limyè
- **HSLA**: HSL ak chanèl Alfa
- **Egzadesimal**: Sistèm nimerik baz 16 itilize 0-9 ak A-F
- **Chanèl Alfa**: Kontwole transparans (0 = transparan, 1 = opak)
- **Tèn**: Koulè a menm sou yon wou koulè 360 degre
- **Satiasyon**: Entansite koulè a (0% = gri, 100% = vif)
- **Limyè**: Konbyen koulè a klè oswa fonse

### Tèm Inite
- **Inite Absoli**: Mezi fiks (px, in, cm, mm, pt, pc)
- **Inite Relatif**: Mezi relatif ak yon lòt bagay (%, em, rem, vw, vh)
- **Piksèl (px)**: Yon sèl pwen sou yon ekran
- **Em (em)**: Relatif ak gwosè polis eleman an
- **Rem (rem)**: Relatif ak gwosè polis eleman rasin lan
- **Viewport**: Zòn vizib yon paj entènèt
- **Lajè Viewport (vw)**: 1% lajè viewport
- **Wotè Viewport (vh)**: 1% wotè viewport

### Tèm Polis
- **Fanmi Polis**: Polis pou itilize
- **Pwa Polis**: Epesè karaktè yo (100-900)
- **Estil Polis**: Nòmal, italik oswa oblik
- **Wotè Liy**: Espas ant liy tèks yo
- **Espas Lèt**: Espas ant karaktè yo
- **Espas Mo**: Espas ant mo yo
- **Transfòmasyon Tèks**: Kontwòl kapitalizasyon
- **Dekorasyon Tèks**: Liy ki ajoute nan tèks (souliye, souliye anwo, bare)
- **Serif**: Polis ak trete dekoratif
- **Sans-serif**: Polis san trete dekoratif
- **Monospace**: Polis kote tout karaktè gen menm lajè
- **Polis Rezèv**: Polis altènatif si premye chwa a pa disponib

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

---

## Devwa

### Devwa 1: Kreyatè Palèt Koulè
Kreye yon paj entènèt ki montre tout fòma koulè lè w konstwi yon ekspozisyon palèt koulè.
[Gade Devwa 1](assignment1.md)

### Devwa 2: Tipografi Responsif
Konstwi yon paj espesimen tipografi lè w itilize diferan pwopriyete polis ak inite.
[Gade Devwa 2](assignment2.md)

### Devwa 3: Gid Estil Konplè
Kreye yon gid estil konplè ki konbine koulè, inite ak polis.
[Gade Devwa 3](assignment3.md)

### Solisyon
- [Solisyon Devwa 1](assignment1-solution.md)
- [Solisyon Devwa 2](assignment2-solution.md)
- [Solisyon Devwa 3](assignment3-solution.md)

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

---

## Rezime

### Pwen Kle pou Sonje

1. **Koulè CSS**
   - Plizyè fòma disponib: ki gen non, hex, RGB, RGBA, HSL, HSLA
   - Itilize RGBA/HSLA pou efè transparans
   - HSL entwitif pou kreye varyasyon koulè
   - Toujou konsidere kontras pou aksesibilite

2. **Inite CSS**
   - Inite absoli (px) pou gwosè fiks
   - Inite relatif (%, em, rem) pou desen fleksib
   - Inite viewport (vw, vh) pou aranjman responsif
   - Chwazi inite selon kontèks ak bezwen

3. **Polis CSS**
   - Toujou bay polis rezèv
   - Itilize rem pou gwosè konsistan
   - Konbine pwopriyete pou kontwòl tipografik konplè
   - Konsidere li fasil ak wotè liy apwopriye

### Pi Bon Pratik
- Itilize non koulè semantik nan CSS ou pou ka kenbe li fasil
- Prefere rem olye em pou gwosè ki pi previzib
- Toujou mete fanmi polis jenerik kòm rezèv
- Teste desen ou nan diferan gwosè ekran
- Kenbe bon rapò kontras pou aksesibilite

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)

---

## Resous

### Dokimantasyon
- [MDN Koulè CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
- [MDN Inite CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)
- [MDN Polis CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/font)

### Referans W3Schools
- [W3Schools Koulè CSS](https://www.w3schools.com/css/css_colors.asp)
- [W3Schools Inite CSS](https://www.w3schools.com/css/css_units.asp)
- [W3Schools Polis CSS](https://www.w3schools.com/css/css_font.asp)

### Zouti
- WebStorm IDE pou edite kòd
- Git pou kontwòl vèsyon
- GitHub pou depo kòd

### Zouti Koulè
- Selektè koulè DevTools navigatè a
- Itilite selektè koulè sistèm lan

[Tounen Anwo](#koulè-inite-ak-polis-css---nòt-kou)