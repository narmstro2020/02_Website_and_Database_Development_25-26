# Pwopyete Afichaj CSS ak Modèl Bwat CSS la

## Tab Matye yo

| Sijè | Deskripsyon |
|-------|-------------|
| [Entwodiksyon](#entwodiksyon) | Apèsi pwopyete afichaj ak modèl bwat la |
| [Vokabilè](#vokabilè) | Mo kle ak definisyon yo |
| [Pwopyete Afichaj CSS](#pwopyete-afichaj-css) | Konprann block, inline, inline-block ak none |
| [Modèl Bwat CSS la](#modèl-bwat-css-la) | Margin, padding, border ak content |
| [Egzanp Vizyèl yo](#egzanp-vizyèl-yo) | Demonstrasyon entèraktif yo |
| [Rezime](#rezime) | Pwen yo pi enpòtan |
| [Resous yo](#resous-yo) | Materyèl aprann yo ajoute |

---

## Entwodiksyon

Byenvini nan leson nou an sou Pwopyete Afichaj CSS ak Modèl Bwat CSS la! Sa yo se konsèp fondamantal yo ki kontwole ki jan eleman yo parèt ak ki jan yo pran espas sou yon paj entènèt. Nan fen leson an, w ap konprann ki jan pou kontwole aranjman ak espas eleman yo tankou yon devlopè entènèt pwofesyonèl.

### Sa w ap Aprann
- Ki jan diferan pwopyete afichaj yo afekte konpòtman eleman yo
- Konpozan yo nan Modèl Bwat CSS la
- Ki jan pou kontwole espas anndan ak deyò eleman yo
- Teknik pratik yo pou kreye aranjman yo

[⬆ Tounen nan Kòmanse](#tab-matye-yo)

---

## Vokabilè

### Mo yo sou Pwopyete Afichaj
- **Pwopyete Display**: Pwopyete CSS ki detèmine ki jan yon eleman montre nan kouran dokiman an
- **Eleman Block**: Yon eleman ki kòmanse sou yon liy nouvo epi pran tout lajè ki disponib la
- **Eleman Inline**: Yon eleman ki koule ak tèks la epi sèlman pran lajè ki nesesè a
- **Eleman Inline-Block**: Konbine karakteristik eleman inline ak block yo
- **Kouran Dokiman**: Lòd kote eleman yo parèt nan HTML la ak ki jan yo anpile sou paj la

### Mo yo sou Modèl Bwat
- **Content**: Kontni reyèl eleman an (tèks, imaj, elatriye)
- **Padding**: Espas ant kontni an ak fwontyè a
- **Border**: Yon liy ki antoure padding ak kontni an
- **Margin**: Espas deyò fwontyè a ki separe eleman an ak lòt eleman yo
- **Outline**: Yon liy yo desine deyò fwontyè a ki pa afekte aranjman an
- **Box-Sizing**: Pwopyete ki detèmine ki jan yo kalkile lajè ak wotè a

[⬆ Tounen nan Kòmanse](#tab-matye-yo)

---

## Pwopyete Afichaj CSS

### Konprann Kalite Afichaj yo

Pwopyete `display` la se youn nan pwopyete CSS yo ki pi enpòtan pou kontwole aranjman an. Li detèmine ki jan yon eleman konpòte nan kouran dokiman an.

### 1. Eleman Block (`display: block`)

Eleman block yo tankou paragraf nan yon liv - yo kòmanse sou yon liy nouvo epi yo etann sou tout lajè ki disponib la.

**Karakteristik yo:**
- Kòmanse sou yon liy nouvo
- Pran tout lajè ki disponib la
- Ka gen lajè ak wotè etabli
- Respekte tout valè margin ak padding yo

**Eleman Block pa Defo:**
- `<div>`, `<p>`, `<h1>` rive nan `<h6>`
- `<header>`, `<footer>`, `<main>`, `<section>`, `<article>`
- `<ul>`, `<ol>`, `<li>`

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Eleman Block</title>
    <style>
        .block-example {
            display: block;
            background-color: lightblue;
            padding: 10px;
            margin: 10px 0;
            border: 2px solid darkblue;
        }
    </style>
</head>
<body>
    <div class="block-example">Mwen se yon eleman block</div>
    <div class="block-example">Mwen kòmanse sou yon liy nouvo</div>
    <p class="block-example">Paragraf yo se block pa defo</p>
</body>
</html>
```

### 2. Eleman Inline (`display: inline`)

Eleman inline yo tankou mo nan yon fraz - yo koule ak tèks la epi yo sèlman pran espas ki nesesè a.

**Karakteristik yo:**
- Pa kòmanse sou yon liy nouvo
- Sèlman pran lajè ki nesesè a
- Pa ka gen lajè ak wotè etabli
- Margin ak padding vètikal pa afekte eleman yo ki antoure yo
- Margin ak padding orizontal fonksyone nòmalman

**Eleman Inline pa Defo:**
- `<span>`, `<a>`, `<strong>`, `<em>`
- `<img>` (ka espesyal - aksepte lajè/wotè)

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Eleman Inline</title>
    <style>
        .inline-example {
            display: inline;
            background-color: yellow;
            padding: 5px;
            margin: 5px;
            border: 1px solid orange;
        }
    </style>
</head>
<body>
    <p>
        Sa a se yon paragraf ak 
        <span class="inline-example">eleman</span> 
        inline ki 
        <span class="inline-example">koule</span> 
        ak tèks la.
    </p>
</body>
</html>
```

### 3. Eleman Inline-Block (`display: inline-block`)

Eleman inline-block yo konbine pi bon nan tou de mond yo - yo koule tankou eleman inline men yo aksepte dimansyon tankou eleman block.

**Karakteristik yo:**
- Koule ak tèks la tankou eleman inline
- Aksepte lajè ak wotè tankou eleman block
- Respekte tout valè margin ak padding yo
- Pa fòse yon sote liy

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Inline-Block</title>
    <style>
        .inline-block-example {
            display: inline-block;
            width: 100px;
            height: 100px;
            background-color: lightgreen;
            margin: 10px;
            padding: 10px;
            border: 2px solid darkgreen;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="inline-block-example">Bwat 1</div>
    <div class="inline-block-example">Bwat 2</div>
    <div class="inline-block-example">Bwat 3</div>
</body>
</html>
```

### 4. None (`display: none`)

Eleman yo ak `display: none` yo retire konplètman nan kouran dokiman an.

**Karakteristik yo:**
- Eleman an pa vizib
- Pa pran okenn espas sou paj la
- Diferan ak `visibility: hidden` (ki kache men prezève espas la)

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Display None</title>
    <style>
        .hidden {
            display: none;
        }
        .visible {
            background-color: lightcoral;
            padding: 10px;
            margin: 5px;
        }
    </style>
</head>
<body>
    <div class="visible">Mwen vizib</div>
    <div class="hidden">Mwen konplètman kache epi pa pran okenn espas</div>
    <div class="visible">Mwen parèt jis apre premye div la</div>
</body>
</html>
```

[⬆ Tounen nan Kòmanse](#tab-matye-yo)

---

## Modèl Bwat CSS la

Chak eleman HTML se yon bwat rektangulè. Modèl Bwat CSS la dekri ki jan bwat sa yo estriktire ak ki jan yo kalkile dimansyon yo.

### Konpozan Modèl Bwat la (nan anndan rive nan deyò)

1. **Content**: Kontni reyèl eleman an
2. **Padding**: Espas ant kontni an ak fwontyè a
3. **Border**: Rebò bwat eleman an
4. **Margin**: Espas deyò fwontyè a

### Reprezantasyon Vizyèl

```
+------------------------------------------+
|              MARGIN (transparan)         |
|  +------------------------------------+  |
|  |          BORDER                    |  |
|  |  +------------------------------+  |  |
|  |  |        PADDING               |  |  |
|  |  |  +------------------------+  |  |  |
|  |  |  |                        |  |  |  |
|  |  |  |       CONTENT          |  |  |  |
|  |  |  |                        |  |  |  |
|  |  |  +------------------------+  |  |  |
|  |  |                              |  |  |
|  |  +------------------------------+  |  |
|  |                                    |  |
|  +------------------------------------+  |
|                                          |
+------------------------------------------+
```

### 1. Zòn Kontni

Zòn kontni an gen kontni reyèl la - tèks, imaj oswa lòt eleman yo.

**Pwopyete yo:**
- `width`: Etabli lajè zòn kontni an
- `height`: Etabli wotè zòn kontni an

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Zòn Kontni</title>
    <style>
        .content-box {
            width: 200px;
            height: 100px;
            background-color: #e8f4f8;
        }
    </style>
</head>
<body>
    <div class="content-box">
        Sa a se zòn kontni an. Lajè: 200px, Wotè: 100px
    </div>
</body>
</html>
```

### 2. Padding

Padding kreye espas ant kontni an ak fwontyè a. Li transparan epi li montre koulè fon eleman an.

**Pwopyete yo:**
- `padding-top`, `padding-right`, `padding-bottom`, `padding-left`
- Abrevye: `padding: 10px;` (tout kote yo)
- Abrevye: `padding: 10px 20px;` (anlè/anba, gòch/dwat)
- Abrevye: `padding: 10px 20px 30px 40px;` (anlè, dwat, anba, gòch - sans orèy)

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Padding</title>
    <style>
        .padding-demo {
            background-color: lightblue;
            border: 2px solid navy;
            padding: 20px;
            margin-bottom: 10px;
        }
        
        .padding-varied {
            background-color: lightgreen;
            border: 2px solid darkgreen;
            padding-top: 10px;
            padding-right: 20px;
            padding-bottom: 30px;
            padding-left: 40px;
        }
    </style>
</head>
<body>
    <div class="padding-demo">
        Padding inifòm 20px sou tout kote yo
    </div>
    <div class="padding-varied">
        Padding diferan sou chak kote
    </div>
</body>
</html>
```

### 3. Border

Fwontyè a antoure padding ak kontni an. Li ka gen diferan estil, lajè ak koulè.

**Pwopyete yo:**
- `border-width`: Epesè fwontyè a
- `border-style`: solid, dashed, dotted, double, elatriye
- `border-color`: Koulè fwontyè a
- Abrevye: `border: 2px solid black;`

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Border</title>
    <style>
        .border-solid {
            border: 3px solid #333;
            padding: 10px;
            margin: 10px;
        }
        
        .border-dashed {
            border: 2px dashed red;
            padding: 10px;
            margin: 10px;
        }
        
        .border-mixed {
            border-top: 5px solid blue;
            border-right: 3px dotted green;
            border-bottom: 2px dashed orange;
            border-left: 4px double purple;
            padding: 10px;
            margin: 10px;
        }
    </style>
</head>
<body>
    <div class="border-solid">Fwontyè solid</div>
    <div class="border-dashed">Fwontyè tiret</div>
    <div class="border-mixed">Estil fwontyè melanje</div>
</body>
</html>
```

### 4. Margin

Margin kreye espas deyò fwontyè a, k ap separe eleman an ak lòt eleman yo.

**Pwopyete yo:**
- `margin-top`, `margin-right`, `margin-bottom`, `margin-left`
- Abrevye fonksyone tankou padding
- Valè espesyal: `margin: 0 auto;` (santre eleman block yo orizontalman)
- Margin yo ka negatif (rapwoche eleman yo)

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Margin</title>
    <style>
        .margin-demo {
            background-color: #ffeb3b;
            border: 2px solid #f57c00;
            padding: 10px;
            margin: 20px;
        }
        
        .centered {
            width: 300px;
            background-color: #e1bee7;
            border: 2px solid #7b1fa2;
            padding: 20px;
            margin: 20px auto;
        }
        
        .margin-collapse-1 {
            background-color: #c8e6c9;
            padding: 10px;
            margin-bottom: 30px;
        }
        
        .margin-collapse-2 {
            background-color: #ffccbc;
            padding: 10px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="margin-demo">Margin 20px sou tout kote yo</div>
    <div class="centered">Santre ak margin: 20px auto</div>
    <div class="margin-collapse-1">Margin anba: 30px</div>
    <div class="margin-collapse-2">Margin anlè: 20px (kolapse nan 30px espas total)</div>
</body>
</html>
```

### 5. Outline (Ka Espesyal)

Outline yo desine deyò fwontyè a men li pa afekte aranjman an ni li pa pran espas.

**Pwopyete yo:**
- `outline-width`: Epesè
- `outline-style`: Estil (tankou border-style)
- `outline-color`: Koulè
- `outline-offset`: Espas ant fwontyè ak outline
- Abrevye: `outline: 2px solid red;`

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Outline</title>
    <style>
        .outline-demo {
            border: 2px solid blue;
            outline: 3px dashed red;
            outline-offset: 5px;
            padding: 10px;
            margin: 20px;
        }
    </style>
</head>
<body>
    <div class="outline-demo">
        Sa a gen tou de yon fwontyè (ble) ak yon outline (wouj tiret)
    </div>
</body>
</html>
```

### Pwopyete Box-Sizing

Pa defo, lajè ak wotè sèlman etabli gwosè zòn kontni an. Pwopyete `box-sizing` la ka chanje konpòtman sa a.

**Valè yo:**
- `content-box` (pa defo): Lajè/wotè aplike nan kontni sèlman
- `border-box`: Lajè/wotè gen ladan padding ak border

**Egzanp Kòd:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Egzanp Box-Sizing</title>
    <style>
        .content-box {
            box-sizing: content-box;
            width: 200px;
            padding: 20px;
            border: 5px solid black;
            background-color: lightblue;
            margin-bottom: 10px;
        }
        
        .border-box {
            box-sizing: border-box;
            width: 200px;
            padding: 20px;
            border: 5px solid black;
            background-color: lightgreen;
        }
    </style>
</head>
<body>
    <div class="content-box">
        content-box: Lajè total = 200 + 40 + 10 = 250px
    </div>
    <div class="border-box">
        border-box: Lajè total = 200px
    </div>
</body>
</html>
```

[⬆ Tounen nan Kòmanse](#tab-matye-yo)

---

## Kolaps Margin: Yon Apèndis Enpòtan

### Ki sa ki Kolaps Margin?

Kolaps margin se yon konpòtman CSS kote margin vètikal eleman block-level ki kote yo konbine (oswa "kolapse") nan yon sèl margin. Sa a sèlman rive ak **margin vètikal** yo (anlè ak anba), jamè ak margin orizontal yo (gòch ak dwat).

### Kilè Kolaps Margin Rive?

Kolaps margin rive nan twa sitiyasyon prensipal:

#### 1. Frè ak Sè ki Kote
Lè de eleman block yo anpile vètikalman, margin yo ki touche kolapse.

**Egzanp:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Kolaps Margin ant Frè ak Sè ki Kote</title>
    <style>
        .box1 {
            background-color: lightblue;
            padding: 20px;
            margin-bottom: 30px;
        }
        
        .box2 {
            background-color: lightgreen;
            padding: 20px;
            margin-top: 20px;
        }
        
        /* Rezèlta: Sèlman 30px espas ant bwat yo, pa 50px! */
    </style>
</head>
<body>
    <div class="box1">Bwat 1 gen margin-bottom: 30px</div>
    <div class="box2">Bwat 2 gen margin-top: 20px</div>
    <p>Espas ant bwat yo se 30px (margin ki pi gwo a), pa 50px!</p>
</body>
</html>
```

#### 2. Papa ak Premye/Dènye Pitit
Si yon papa pa gen padding oswa border, margin li yo ka kolapse ak margin premye oswa dènye pitit li yo.

**Egzanp:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Kolaps Margin Papa-Pitit</title>
    <style>
        .parent {
            background-color: #ffeb3b;
            margin-top: 40px;
            /* Pa gen padding oswa border anlè */
        }
        
        .child {
            background-color: #ff9800;
            padding: 20px;
            margin-top: 30px;
        }
        
        /* Anlè papa a parèt nan 40px nan eleman anvan an,
           pa 70px (40px + 30px) */
    </style>
</head>
<body>
    <div style="background: #ccc; padding: 10px;">Eleman Anvan</div>
    <div class="parent">
        <div class="child">
            Pitit ak margin-top: 30px anndan papa ak margin-top: 40px
        </div>
    </div>
</body>
</html>
```

#### 3. Blòk Vid yo
Si yon eleman block pa gen kontni, padding, border oswa height, margin anlè ak anba li yo kolapse.

**Egzanp:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Kolaps Margin Blòk Vid</title>
    <style>
        .before {
            background-color: lightcoral;
            padding: 20px;
            margin-bottom: 30px;
        }
        
        .empty {
            margin-top: 20px;
            margin-bottom: 40px;
            /* Pa gen kontni, padding oswa border */
        }
        
        .after {
            background-color: lightseagreen;
            padding: 20px;
            margin-top: 25px;
        }
        
        /* Espas la ap 40px (pi gwo nan tout margin yo) */
    </style>
</head>
<body>
    <div class="before">Eleman anvan</div>
    <div class="empty"></div>
    <div class="after">Eleman apre</div>
</body>
</html>
```

### Règ Kolaps Margin yo

1. **Sèlman Margin Vètikal yo Kolapse**
   - Margin anlè ak anba yo ka kolapse
   - Margin gòch ak dwat JAMÈ kolapse

2. **Margin ki Pi Gwo a Genyen**
   - Lè margin yo kolapse, yo itilize valè margin ki pi gwo a
   - Margin ki pi piti a yo ignore

3. **Margin Negatif yo**
   - Si yon margin negatif, retire li nan margin pozitif la
   - Si tou de yo negatif, itilize valè ki pi negatif la

### Kilè Margin yo PA Kolapse

Margin yo PA ap kolapse lè:

1. **Eleman yo flotant** - Eleman flotant yo jamè kolapse margin
2. **Eleman inline-block** - Sèlman eleman block yo kolapse margin
3. **Eleman yo pozisyone absoliman** - Position: absolute/fixed anpeche kolaps
4. **Overflow etabli** - Eleman ak overflow ki diferan ak visible pa kolapse
5. **Padding oswa border separe yo** - Nenpòt padding/border anpeche kolaps
6. **Eleman yo nan diferan konnèks fòmasyon** - Tankou kontènè flexbox oswa grid

### Anpeche Kolaps Margin

Men teknik yo ki komen pou anpeche kolaps margin ki pa vle:

**Metòd 1: Ajoute Padding oswa Border**
```css
.parent {
    padding-top: 1px; /* Anpeche kolaps ak premye pitit */
    padding-bottom: 1px; /* Anpeche kolaps ak dènye pitit */
}
/* OSWA */
.parent {
    border-top: 1px solid transparent;
    border-bottom: 1px solid transparent;
}
```

**Metòd 2: Itilize Overflow**
```css
.parent {
    overflow: auto; /* oswa hidden, scroll */
}
```

**Metòd 3: Itilize Pwopyete Display**
```css
.element {
    display: inline-block; /* Anpeche kolaps margin */
}
```

**Metòd 4: Itilize Pseudo-eleman**
```css
.parent::before,
.parent::after {
    content: "";
    display: table;
}
```

### Egzanp Pratik: Aranjman Kat ak Kolaps Margin

```html
<!DOCTYPE html>
<html>
<head>
    <title>Kolaps Margin nan Pratik</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
            background: #f0f0f0;
        }
        
        .container {
            background: white;
            border-radius: 8px;
            /* Pa gen padding - margin yo ka kolapse */
        }
        
        .container-fixed {
            background: white;
            border-radius: 8px;
            padding: 1px 20px; /* Padding anpeche kolaps */
            margin-top: 30px;
        }
        
        .card {
            background: #e3f2fd;
            padding: 20px;
            margin: 30px 20px; /* Margin vètikal yo ka kolapse */
        }
        
        h2 {
            background: #1976d2;
            color: white;
            padding: 10px;
            margin: 0 0 20px 0;
        }
        
        .demo-info {
            background: #fff3e0;
            padding: 10px;
            margin: 15px 0;
            border-left: 4px solid #ff9800;
        }
    </style>
</head>
<body>
    <h1>Demonstrasyon Kolaps Margin</h1>
    
    <div class="demo-info">
        <strong>Pwoblèm:</strong> San padding, margin anlè premye kat la kolapse ak kontènè a
    </div>
    
    <div class="container">
        <div class="card">
            Premye kat - margin anlè mwen an (30px) chape nan kontènè a!
        </div>
        <div class="card">
            Dezyèm kat - margin yo ant kat yo kolapse nan 30px, pa 60px
        </div>
        <div class="card">
            Twazyèm kat - margin anba mwen an (30px) chape tou!
        </div>
    </div>
    
    <div class="demo-info">
        <strong>Solisyon:</strong> Ajoute 1px padding anpeche kolaps margin
    </div>
    
    <div class="container-fixed">
        <div class="card">
            Premye kat - kounye a ki gen kòrèkteman nan papa a
        </div>
        <div class="card">
            Dezyèm kat - margin yo toujou kolapse ant kat yo (sa a souvan vle)
        </div>
        <div class="card">
            Twazyèm kat - margin anba tou gen
        </div>
    </div>
</body>
</html>
```

### Poukisa Kolaps Margin Egziste?

Kolaps margin ka sanble konfèz, men li egziste pou bon rezon yo:

1. **Tipografi**: Nan dokiman tèks, ou vle espas konsèkan ant paragraf yo kèlkeswa konfigirasyon margin endividyèl yo
2. **Fleksibilite**: Pèmèt eleman yo defini espas yo vle san double
3. **Istorik**: Konpòtman sa a soti nan tipografi enpresyon tradisyonèl

### Pi Bon Pratik yo

1. **Konnen**: Toujou sonje margin vètikal yo ka kolapse
2. **Itilize Padding**: Lè ou bezwen espas garanti, itilize padding nan plas la
3. **Yon sèl Direksyon**: Konsidere itilize sèlman `margin-bottom` OSWA `margin-top`, pa tou de
4. **Teste Aranjman ou yo**: Verifye espas ant eleman yo pandan devlopman
5. **Dokimante Entansyon**: Kòmante lè w ap konte sou oswa anpeche kolaps

### Pwoblèm ki Komen yo

1. **Premye eleman nan yon kontènè** k ap pouse desann kontènè a li menm
2. **Espas inatann** ki pi piti pase sa yo atann
3. **Margin yo "k ap chape"** nan kontènè yo
4. **Eleman vid yo** ki pa kreye espas yo atann

Konprann kolaps margin ede ou:
- Korije pwoblèm espas inatann yo
- Kreye aranjman ki pi ka prèdi
- Ekri CSS ki pi pwòp ak pi fasil pou kenbe
- Evite pwoblèm aranjman ki fristran

[⬆ Tounen nan Kòmanse](#tab-matye-yo)

---

## Egzanp Vizyèl yo

### Demonstrasyon Konplè Modèl Bwat

```html
<!DOCTYPE html>
<html>
<head>
    <title>Demo Konplè Modèl Bwat</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        
        .box-model-demo {
            width: 300px;
            height: 150px;
            margin: 50px auto;
            padding: 30px;
            border: 10px solid #2196F3;
            background-color: #E3F2FD;
            position: relative;
        }
        
        .label {
            position: absolute;
            background: white;
            padding: 2px 5px;
            font-size: 12px;
            border: 1px solid #ccc;
        }
        
        .margin-label {
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .border-label {
            top: 5px;
            left: 5px;
        }
        
        .padding-label {
            top: 20px;
            left: 20px;
        }
        
        .content-label {
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    </style>
</head>
<body>
    <div class="box-model-demo">
        <span class="label margin-label">MARGIN: 50px</span>
        <span class="label border-label">BORDER: 10px</span>
        <span class="label padding-label">PADDING: 30px</span>
        <span class="label content-label">CONTENT: 300x150px</span>
    </div>
</body>
</html>
```

### Konparezon Pwopyete Display

```html
<!DOCTYPE html>
<html>
<head>
    <title>Konparezon Pwopyete Display</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        
        .container {
            background-color: #f5f5f5;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
        }
        
        .block-item {
            display: block;
            background-color: #ff9800;
            color: white;
            padding: 10px;
            margin: 5px 0;
        }
        
        .inline-item {
            display: inline;
            background-color: #4caf50;
            color: white;
            padding: 10px;
            margin: 5px;
        }
        
        .inline-block-item {
            display: inline-block;
            background-color: #2196f3;
            color: white;
            padding: 10px;
            margin: 5px;
            width: 100px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="container">
        <h3>Eleman Block yo</h3>
        <div class="block-item">Block 1</div>
        <div class="block-item">Block 2</div>
        <div class="block-item">Block 3</div>
    </div>
    
    <div class="container">
        <h3>Eleman Inline yo</h3>
        <span class="inline-item">Inline 1</span>
        <span class="inline-item">Inline 2</span>
        <span class="inline-item">Inline 3</span>
    </div>
    
    <div class="container">
        <h3>Eleman Inline-Block yo</h3>
        <div class="inline-block-item">IB 1</div>
        <div class="inline-block-item">IB 2</div>
        <div class="inline-block-item">IB 3</div>
    </div>
</body>
</html>
```

[⬆ Tounen nan Kòmanse](#tab-matye-yo)

---

## Rezime

### Pwen yo pi Enpòtan

1. **Pwopyete Display yo Kontwole Kouran Aranjman**
   - Eleman block yo anpile vètikalman epi pran tout lajè a
   - Eleman inline yo koule orizontalman epi yo adapte ak tèks la
   - Inline-block konbine avantaj tou de yo
   - Display: none retire eleman yo konplètman

2. **Modèl Bwat la gen Kat Pati Prensipal**
   - Content: Kontni reyèl eleman an
   - Padding: Espas anndan fwontyè a
   - Border: Rebò eleman an
   - Margin: Espas deyò fwontyè a

3. **Box-Sizing Chanje Kalkil yo**
   - content-box: Lajè/wotè aplike nan kontni sèlman
   - border-box: Lajè/wotè gen ladan padding ak border

4. **Margin yo Ka Kolapse**
   - Margin vètikal yo ant eleman yo kolapse nan valè ki pi gwo a
   - Margin orizontal yo jamè kolapse

5. **Outline yo Pa Afekte Aranjman**
   - Itil pou fè parèt san deplase lòt eleman yo

### Ka Itilizasyon ki Komen yo

- **Meni Navigasyon**: Itilize inline oswa inline-block pou meni orizontal yo
- **Aranjman Kat**: Konbine padding pou espas anndan ak margin pou separasyon
- **Santre**: Itilize `margin: 0 auto` pou santre orizontal eleman block yo
- **Design Responsif**: Box-sizing: border-box fè kalkil lajè yo ka prèdi

[⬆ Tounen nan Kòmanse](#tab-matye-yo)

---

## Resous yo

### Dokimantasyon
- [MDN Web Docs - CSS Display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- [MDN Web Docs - CSS Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
- [W3Schools - CSS Display Property](https://www.w3schools.com/css/css_display_visibility.asp)
- [W3Schools - CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp)

### Zouti Pratik yo
- [Vizyalizè Modèl Bwat CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_box_model_and_inline_boxes)
- Itilize DevTools navigatè a (F12) pou enspekte ak modifye pwopyete modèl bwat yo

### Etap k ap Vini yo
Apre ou metrize konsèp sa yo, w ap pare pou aprann:
- Pozisyonman CSS (static, relative, absolute, fixed)
- Aranjman Flexbox
- CSS Grid
- Teknik design responsif yo

[⬆ Tounen nan Kòmanse](#tab-matye-yo)