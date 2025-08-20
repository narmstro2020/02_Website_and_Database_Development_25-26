# Fòm HTML - Nòt Kou

## Tab Matyè

| Sijè | Deskripsyon |
|------|-------------|
| [Entwodiksyon](#entwodiksyon) | Apèsi jeneral fòm HTML |
| [Vokabilè](#vokabilè) | Mo kle ak definisyon |
| [Baz Fòm yo](#baz-fòm-yo) | Konprann eleman fòm lan |
| [Tip Input yo](#tip-input-yo) | Diferan tip antre fòm |
| [Kontwòl Fòm](#kontwòl-fòm) | Bouton, textarea, ak eleman select |
| [Atribi Fòm](#atribi-fòm) | Atribi enpòtan pou fòm yo |
| [Etikèt ak Aksesibilite](#etikèt-ak-aksesibilite) | Fè fòm yo fasil pou itilize |
| [Soumèt Fòm](#soumèt-fòm) | Kijan fòm yo voye done |
| [Egzanp Kòd](#egzanp-kòd) | Egzanp fòm konplè |
| [Èd Vizyèl](#èd-vizyèl) | Dyagram ak ilistrasyon |
| [Rezime](#rezime) | Pwen kle pou sonje |
| [Resous](#resous) | Materyèl pou aprann plis |

---

## Entwodiksyon
[↑ Retounen Anlè](#tab-matyè)

Fòm HTML se youn nan fason ki pi enpòtan pou itilizatè yo entèraji ak sit entènèt. Yo pèmèt itilizatè yo antre done ki ka voye bay yon sèvè pou trete. Panse fòm yo tankou fason sit entènèt kolekte enfòmasyon nan men vizitè yo - tankou lè w enskri pou yon kont, kite yon kòmantè, oswa chèche yon bagay.

Fòm yo toupatou sou entènèt:
- Paj koneksyon
- Fòm enskripsyon
- Fòm kontak
- Bwat rechèch
- Seksyon kòmantè
- Peye nan magazen sou entènèt

Nan leson sa a, nou pral aprann kijan pou kreye fòm lè nou sèvi ak eleman HTML ou poko wè, epi bati sou konesans ou genyen deja sou estrikti HTML.

---

## Vokabilè
[↑ Retounen Anlè](#tab-matyè)

| Tèm | Definisyon |
|-----|------------|
| **Form** | Yon eleman HTML ki gen kontwòl entèaktif pou soumèt enfòmasyon |
| **Input** | Yon kontwòl entèaktif ki aksepte done nan men itilizatè a |
| **Field** | Yon sèl zòn antre done nan yon fòm (tankou yon bwat tèks) |
| **Label** | Tèks ki dekri ki enfòmasyon ta dwe antre nan yon chan fòm |
| **Submit** | Aksyon voye done fòm bay yon sèvè |
| **Action** | URL kote done fòm yo voye lè yo soumèt |
| **Method** | Kijan done fòm yo voye (GET oswa POST) |
| **Placeholder** | Tèks endikas ki montre andedan yon chan antre anvan itilizatè a tape |
| **Required** | Yon atribi ki fè yon chan obligatwa |
| **Value** | Done ki nan yon chan fòm |
| **Name** | Yon atribi ki idantifye done fòm lè yo soumèt |
| **Textarea** | Yon chan antre tèks plizyè liy |
| **Select** | Yon meni deroulan pou chwazi opsyon |
| **Option** | Yon chwa nan yon meni deroulan select |
| **Radio Button** | Yon bouton sikilè pou chwazi yon opsyon nan yon gwoup |
| **Checkbox** | Yon bwat kare ki ka tcheke oswa pa tcheke |
| **Fieldset** | Yon fason pou gwope eleman fòm ki gen rapò |
| **Legend** | Yon lejand pou yon fieldset |

---

## Baz Fòm yo
[↑ Retounen Anlè](#tab-matyè)

### Eleman Form

Chak fòm HTML kòmanse ak eleman `<form>`. Eleman sa a se yon veso pou tout kontwòl entèaktif ki kolekte antre itilizatè.

```html
<form>
    <!-- Kontwòl fòm yo ale isit la -->
</form>
```

Eleman form lan tankou yon `<section>` oswa `<article>` - se yon veso ki gwope kontni ki gen rapò ansanm. Nan ka sa a, li gwope tout chan antre ak bouton ki travay ansanm pou kolekte enfòmasyon.

### Estrikti Debaz Fòm

Yon fòm tipik gen twa pati prensipal:
1. **Veso fòm lan** - Eleman `<form>` lan menm
2. **Chan antre** - Kote itilizatè yo antre done
3. **Bouton soumèt** - Deklanche soumisyon fòm lan

```html
<form>
    <label for="username">Non itilizatè:</label>
    <input type="text" id="username" name="username">
    
    <button type="submit">Soumèt</button>
</form>
```

---

## Tip Input yo
[↑ Retounen Anlè](#tab-matyè)

Eleman `<input>` se kontwòl fòm ki pi polyvalant. Lè w chanje atribi `type` li, ou ka kreye anpil diferan kalite chan antre.

### Input Tèks
Tip input ki pi debaz pou tèks sou yon sèl liy:

```html
<input type="text" name="premyenon" placeholder="Antre premye non ou">
```

### Input Imèl
Espesyalman pou adrès imèl (navigatè yo ka valide fòma a):

```html
<input type="email" name="useremail" placeholder="itilizatè@egzanp.com">
```

### Input Modpas
Kache tèks la pandan itilizatè a ap tape:

```html
<input type="password" name="userpassword" placeholder="Antre modpas">
```

### Input Nimewo
Aksepte sèlman valè nimerik:

```html
<input type="number" name="laj" min="1" max="120" placeholder="Laj ou">
```

### Input Dat
Bay yon selektè dat:

```html
<input type="date" name="dat_nesans">
```

### Bouton Radyo
Pou chwazi yon opsyon nan yon gwoup (sèvi ak menm `name` pou radyo gwope):

```html
<input type="radio" id="piti" name="gwosè" value="piti">
<label for="piti">Piti</label>

<input type="radio" id="mwayen" name="gwosè" value="mwayen">
<label for="mwayen">Mwayen</label>

<input type="radio" id="gwo" name="gwosè" value="gwo">
<label for="gwo">Gwo</label>
```

### Bwat pou Tcheke
Pou chwazi plizyè opsyon:

```html
<input type="checkbox" id="opsyon1" name="karakteristik" value="karakteristik1">
<label for="opsyon1">Karakteristik 1</label>

<input type="checkbox" id="opsyon2" name="karakteristik" value="karakteristik2">
<label for="opsyon2">Karakteristik 2</label>
```

### Lòt Tip Input

| Tip | Objektif |
|-----|----------|
| `tel` | Nimewo telefòn |
| `url` | Adrès entènèt |
| `time` | Seleksyon lè |
| `color` | Selektè koulè |
| `range` | Kontwòl glise |
| `file` | Telechaje fichye |
| `hidden` | Done kache |

---

## Kontwòl Fòm
[↑ Retounen Anlè](#tab-matyè)

### Textarea
Pou antre tèks plizyè liy:

```html
<label for="mesaj">Mesaj Ou:</label>
<textarea id="mesaj" name="mesaj" rows="4" cols="50">
    Tèks pa defo ka ale isit la
</textarea>
```

Atribi `rows` defini wotè vizib, epi `cols` defini lajè vizib.

### Select (Meni Deroulan)
Pou chwazi nan yon lis opsyon:

```html
<label for="peyi">Peyi:</label>
<select id="peyi" name="peyi">
    <option value="">--Tanpri chwazi--</option>
    <option value="ayiti">Ayiti</option>
    <option value="etazini">Etazini</option>
    <option value="kanada">Kanada</option>
</select>
```

Ou ka gwope opsyon tou:

```html
<select name="manje">
    <optgroup label="Fwi">
        <option value="pòm">Pòm</option>
        <option value="bannann">Bannann</option>
    </optgroup>
    <optgroup label="Legim">
        <option value="kawòt">Kawòt</option>
        <option value="bwokoli">Bwokoli</option>
    </optgroup>
</select>
```

### Bouton yo
Twa tip bouton nan fòm:

```html
<!-- Bouton soumèt - soumèt fòm lan -->
<button type="submit">Soumèt Fòm</button>

<!-- Bouton reyinisyalize - efase tout chan fòm -->
<button type="reset">Efase Fòm</button>

<!-- Bouton regilye - pa fè anyen pa defo -->
<button type="button">Klike Mwen</button>
```

Ou ka sèvi ak `<input>` pou bouton tou:

```html
<input type="submit" value="Soumèt">
<input type="reset" value="Reyinisyalize">
<input type="button" value="Klike">
```

---

## Atribi Fòm
[↑ Retounen Anlè](#tab-matyè)

### Atribi Fòm Enpòtan

| Atribi | Eleman | Objektif |
|--------|--------|----------|
| `action` | `<form>` | URL kote done fòm voye |
| `method` | `<form>` | Metòd HTTP (GET oswa POST) |
| `name` | Tout input | Idantifye done lè soumèt |
| `id` | Tout eleman | Idantifyan inik pou konekte label |
| `value` | Input | Valè pa defo oswa aktyèl |
| `placeholder` | Input tèks | Tèks endikas ki montre lè vid |
| `required` | Input | Fè chan obligatwa |
| `disabled` | Tout kontwòl | Anpeche entèraksyon itilizatè |
| `readonly` | Input tèks | Anpeche modifye men pèmèt seleksyon |
| `maxlength` | Input tèks | Kantite maksimòm karaktè |
| `min`/`max` | Nimewo/dat | Valè minimòm/maksimòm |
| `pattern` | Input tèks | Modèl regex pou validasyon |
| `autocomplete` | Input | Aktive/dezaktive otokòmplete |

### Egzanp ak Atribi

```html
<form action="/soumèt" method="post">
    <label for="imèl">Imèl (obligatwa):</label>
    <input type="email" 
           id="imèl" 
           name="imèl" 
           required 
           placeholder="ou@imèl.com"
           maxlength="100">
    
    <label for="laj">Laj:</label>
    <input type="number" 
           id="laj" 
           name="laj" 
           min="18" 
           max="100" 
           value="25">
    
    <button type="submit">Enskri</button>
</form>
```

---

## Etikèt ak Aksesibilite
[↑ Retounen Anlè](#tab-matyè)

### Enpòtans Label yo

Label yo enpòtan pou:
1. **Itilizabilite** - Itilizatè yo konnen kisa pou antre
2. **Aksesibilite** - Lektè ekran ka dekri chan yo
3. **Klikabilite** - Klike sou label la fokis input la

### De Fason pou Asosye Label

**Metòd 1: Sèvi ak atribi `for` (Rekòmande)**
```html
<label for="username">Non itilizatè:</label>
<input type="text" id="username" name="username">
```

**Metòd 2: Vlope input la**
```html
<label>
    Non itilizatè:
    <input type="text" name="username">
</label>
```

### Fieldset ak Legend

Gwope eleman fòm ki gen rapò ansanm:

```html
<fieldset>
    <legend>Enfòmasyon Pèsonèl</legend>
    
    <label for="pnon">Premye Non:</label>
    <input type="text" id="pnon" name="pnon">
    
    <label for="dnon">Dènye Non:</label>
    <input type="text" id="dnon" name="dnon">
</fieldset>

<fieldset>
    <legend>Preferans</legend>
    
    <input type="checkbox" id="bilten" name="bilten">
    <label for="bilten">Abòne nan bilten</label>
</fieldset>
```

### Pi Bon Pratik pou Fòm Aksesib

1. **Toujou sèvi ak label** - Chak input bezwen yon label
2. **Sèvi ak fieldset** - Gwope chan ki gen rapò
3. **Bay enstriksyon klè** - Sèvi ak tèks endikas ak tèks èd
4. **Make chan obligatwa** - Sèvi ak atribi `required` ak endikatè vizyèl
5. **Lòd tab lojik** - Ranje chan yo nan yon sekans lojik
6. **Mesaj erè klè** - Menm si sa mande JavaScript, planifye pou li

---

## Soumèt Fòm
[↑ Retounen Anlè](#tab-matyè)

### Kijan Fòm yo Travay

Lè yon itilizatè klike bouton soumèt la:
1. Navigatè a kolekte tout done fòm lan
2. Li pake done yo lè l sèvi ak atribi `name` yo kòm kle
3. Li voye done yo nan URL ki espesifye nan atribi `action` an
4. Sèvè a trete done yo epi reponn

### Metòd GET kont POST

**Metòd GET:**
- Ajoute done yo nan URL
- Vizib nan ba adrès la
- Gwosè done limite
- Bon pou rechèch ak filtè
- Ka mete nan favori

```html
<form action="/rechèch" method="get">
    <input type="text" name="keksyon">
    <button type="submit">Chèche</button>
</form>
<!-- Bay URL tankou: /rechèch?keksyon=fòm+html -->
```

**Metòd POST:**
- Voye done nan kò demann lan
- Pa vizib nan URL
- Pa gen limit gwosè
- Bon pou done sansib
- Pa ka mete nan favori

```html
<form action="/enskri" method="post">
    <input type="password" name="modpas">
    <button type="submit">Enskri</button>
</form>
```

### Simile Soumisyon Fòm ak JavaScript

Kòm nou poko aprann sèvè, nou ka sèvi ak JavaScript pou wè ki done fòm nou an ta voye:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Demo Fòm</title>
</head>
<body>
    <form id="fòmMwen">
        <label for="non">Non:</label>
        <input type="text" id="non" name="non" required>
        
        <label for="imèl">Imèl:</label>
        <input type="email" id="imèl" name="imèl" required>
        
        <button type="submit">Soumèt</button>
    </form>
    
    <script>
        document.getElementById('fòmMwen').addEventListener('submit', function(e) {
            e.preventDefault(); // Anpeche fòm lan vrèman soumèt
            
            // Jwenn tout done fòm lan
            const formData = new FormData(this);
            
            // Montre chak chan nan konsòl
            console.log('Fòm soumèt ak done sa yo:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

---

## Egzanp Kòd
[↑ Retounen Anlè](#tab-matyè)

### Egzanp 1: Fòm Kontak Senp

```html
<!DOCTYPE html>
<html>
<head>
    <title>Fòm Kontak</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Kontakte Nou</h1>
    </header>
    
    <main>
        <form id="fòmKontak">
            <p>
                <label for="nonkonplè">Non Konplè:</label><br>
                <input type="text" id="nonkonplè" name="nonkonplè" required>
            </p>
            
            <p>
                <label for="imèl">Adrès Imèl:</label><br>
                <input type="email" id="imèl" name="imèl" required>
            </p>
            
            <p>
                <label for="sijè">Sijè:</label><br>
                <input type="text" id="sijè" name="sijè" placeholder="Kisa li ye?">
            </p>
            
            <p>
                <label for="mesaj">Mesaj:</label><br>
                <textarea id="mesaj" name="mesaj" rows="5" cols="40" required></textarea>
            </p>
            
            <p>
                <button type="submit">Voye Mesaj</button>
                <button type="reset">Efase Fòm</button>
            </p>
        </form>
    </main>
    
    <script>
        document.getElementById('fòmKontak').addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(this);
            console.log('Fòm kontak soumèt:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

### Egzanp 2: Fòm Enskripsyon ak Divès Tip Input

```html
<!DOCTYPE html>
<html>
<head>
    <title>Fòm Enskripsyon</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Kreye Kont Ou</h1>
    </header>
    
    <main>
        <form id="fòmEnskripsyon">
            <fieldset>
                <legend>Enfòmasyon Pèsonèl</legend>
                
                <p>
                    <label for="premyenon">Premye Non:</label><br>
                    <input type="text" id="premyenon" name="premyenon" required>
                </p>
                
                <p>
                    <label for="dènyenon">Dènye Non:</label><br>
                    <input type="text" id="dènyenon" name="dènyenon" required>
                </p>
                
                <p>
                    <label for="datnesans">Dat Nesans:</label><br>
                    <input type="date" id="datnesans" name="datnesans" required>
                </p>
                
                <p>
                    <label for="sèks">Sèks:</label><br>
                    <input type="radio" id="gason" name="sèks" value="gason">
                    <label for="gason">Gason</label><br>
                    <input type="radio" id="fanm" name="sèks" value="fanm">
                    <label for="fanm">Fanm</label><br>
                    <input type="radio" id="lòt" name="sèks" value="lòt">
                    <label for="lòt">Lòt</label>
                </p>
            </fieldset>
            
            <fieldset>
                <legend>Detay Kont</legend>
                
                <p>
                    <label for="username">Non itilizatè:</label><br>
                    <input type="text" id="username" name="username" required maxlength="20">
                </p>
                
                <p>
                    <label for="userimèl">Imèl:</label><br>
                    <input type="email" id="userimèl" name="userimèl" required>
                </p>
                
                <p>
                    <label for="modpas">Modpas:</label><br>
                    <input type="password" id="modpas" name="modpas" required>
                </p>
                
                <p>
                    <label for="peyi">Peyi:</label><br>
                    <select id="peyi" name="peyi" required>
                        <option value="">--Chwazi Peyi--</option>
                        <option value="ayiti">Ayiti</option>
                        <option value="etazini">Etazini</option>
                        <option value="kanada">Kanada</option>
                        <option value="lafrans">Lafrans</option>
                        <option value="lòt">Lòt</option>
                    </select>
                </p>
            </fieldset>
            
            <fieldset>
                <legend>Preferans</legend>
                
                <p>
                    <input type="checkbox" id="bilten" name="preferans" value="bilten">
                    <label for="bilten">Abòne nan bilten</label><br>
                    
                    <input type="checkbox" id="mizajou" name="preferans" value="mizajou">
                    <label for="mizajou">Resevwa mizajou pwodwi</label><br>
                    
                    <input type="checkbox" id="òf" name="preferans" value="òf">
                    <label for="òf">Resevwa òf espesyal</label>
                </p>
            </fieldset>
            
            <p>
                <input type="checkbox" id="kondisyon" name="kondisyon" required>
                <label for="kondisyon">Mwen dakò ak tèm ak kondisyon yo</label>
            </p>
            
            <p>
                <button type="submit">Kreye Kont</button>
                <button type="reset">Efase Fòm</button>
            </p>
        </form>
    </main>
    
    <script>
        document.getElementById('fòmEnskripsyon').addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(this);
            console.log('Fòm enskripsyon soumèt:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

### Egzanp 3: Fòm Sondaj

```html
<!DOCTYPE html>
<html>
<head>
    <title>Sondaj Kliyan</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Sondaj Satisfaksyon Kliyan</h1>
    </header>
    
    <main>
        <form id="fòmSondaj">
            <p>
                <label for="nonkliyan">Non Ou:</label><br>
                <input type="text" id="nonkliyan" name="nonkliyan" placeholder="Jan Jak">
            </p>
            
            <fieldset>
                <legend>Ki jan ou satisfè ak sèvis nou an?</legend>
                
                <input type="radio" id="trè-satisfè" name="satisfaksyon" value="5">
                <label for="trè-satisfè">Trè Satisfè</label><br>
                
                <input type="radio" id="satisfè" name="satisfaksyon" value="4">
                <label for="satisfè">Satisfè</label><br>
                
                <input type="radio" id="nèt" name="satisfaksyon" value="3">
                <label for="nèt">Nèt</label><br>
                
                <input type="radio" id="pa-satisfè" name="satisfaksyon" value="2">
                <label for="pa-satisfè">Pa Satisfè</label><br>
                
                <input type="radio" id="pa-satisfè-ditou" name="satisfaksyon" value="1">
                <label for="pa-satisfè-ditou">Pa Satisfè Ditou</label>
            </fieldset>
            
            <p>
                <label for="nòt">Bay nou nòt sou 1-10:</label><br>
                <input type="number" id="nòt" name="nòt" min="1" max="10" value="5">
            </p>
            
            <p>
                <label for="dat-vizit">Dat vizit ou:</label><br>
                <input type="date" id="dat-vizit" name="datvizit">
            </p>
            
            <p>
                <label for="amelyorasyon">Kisa nou ka amelyore?</label><br>
                <textarea id="amelyorasyon" name="amelyorasyon" rows="4" cols="50" 
                          placeholder="Di nou sa w panse..."></textarea>
            </p>
            
            <p>
                <button type="submit">Soumèt Sondaj</button>
            </p>
        </form>
    </main>
    
    <script>
        document.getElementById('fòmSondaj').addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(this);
            console.log('Sondaj soumèt:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

---

## Èd Vizyèl
[↑ Retounen Anlè](#tab-matyè)

### Dyagram Estrikti Fòm

```
┌──────────────────────────────────────┐
│            <form>                    │
│  ┌──────────────────────────────┐   │
│  │        <fieldset>            │   │
│  │  ┌────────────────────┐      │   │
│  │  │     <legend>       │      │   │
│  │  └────────────────────┘      │   │
│  │  ┌────────────────────┐      │   │
│  │  │     <label>        │      │   │
│  │  └────────────────────┘      │   │
│  │  ┌────────────────────┐      │   │
│  │  │     <input>        │      │   │
│  │  └────────────────────┘      │   │
│  └──────────────────────────────┘   │
│  ┌──────────────────────────────┐   │
│  │    <button type="submit">    │   │
│  └──────────────────────────────┘   │
└──────────────────────────────────────┘
```

### Referans Vizyèl Tip Input

```
Input Tèks:        [________________]
Input Imèl:        [user@egzanp.com ]
Input Modpas:      [••••••••••••••••]
Input Nimewo:      [  42  ][↑][↓]
Input Dat:         [12/25/2024  ][📅]
Bouton Radyo:      ( ) Opsyon 1
                   (●) Opsyon 2
                   ( ) Opsyon 3
Bwat pou tcheke:   ☐ Opsyon A
                   ☑ Opsyon B
                   ☐ Opsyon C
Meni Deroulan:     [Chwazi youn    ▼]
Textarea:          ┌─────────────────┐
                   │ Tèks plizyè     │
                   │ liy isit la...  │
                   └─────────────────┘
Bouton Soumèt:     [ Soumèt Fòm ]
```

### Koule Done Fòm

```
Itilizatè ranpli fòm
     ↓
Klike Soumèt
     ↓
Navigatè kolekte done
     ↓
Kreye pè non=valè
     ↓
Voye nan URL action
     ↓
Sèvè trete
     ↓
Repons voye tounen
```

---

## Rezime
[↑ Retounen Anlè](#tab-matyè)

### Pwen Kle pou Sonje

1. **Fòm se veso** - Eleman `<form>` vlope tout kontwòl fòm
2. **Chak input bezwen yon name** - Atribi `name` idantifye done lè soumèt
3. **Label yo esansyèl** - Yo fè fòm aksesib ak fasil pou itilize
4. **Tip input enpòtan** - Chwazi bon tip pou pi bon eksperyans itilizatè
5. **Òganize ak fieldset** - Gwope chan ki gen rapò ansanm lojikman
6. **Validasyon entegre** - HTML5 bay validasyon debaz san JavaScript
7. **Metòd enpòtan** - Sèvi ak GET pou rechèch, POST pou soumisyon
8. **Aksesibilite dabò** - Toujou konsidere itilizatè ki gen andikap

### Sa Ou Ka Fè Kounye a

Apre leson sa a, ou ka:
- Kreye fòm ak divès tip input
- Òganize fòm ak fieldset ak legend
- Ajoute label pou aksesibilite
- Sèvi ak bon tip input pou diferan done
- Kreye seleksyon plizyè opsyon ak bouton radyo ak bwat pou tcheke
- Konstwi meni deroulan ak eleman select
- Ajoute zòn tèks pou antre pi long
- Gen tèks endikas ak chan obligatwa
- Òganize fòm semantikman ak bon HTML

### Modèl Komen pou Sonje

```html
<!-- Toujou asosye label ak input -->
<label for="nonchan">Label Chan:</label>
<input type="text" id="nonchan" name="nonchan">

<!-- Gwope bouton radyo ak menm name -->
<input type="radio" name="chwa" value="opsyon1">
<input type="radio" name="chwa" value="opsyon2">

<!-- Fè chan obligatwa -->
<input type="email" required>

<!-- Bay placeholder itil -->
<input type="text" placeholder="Antre non ou">

<!-- Sèvi ak fieldset pou òganizasyon -->
<fieldset>
    <legend>Tit Seksyon</legend>
    <!-- input ki gen rapò isit la -->
</fieldset>
```

---

## Resous
[↑ Retounen Anlè](#tab-matyè)

### Dokimantasyon ak Referans

- **MDN Web Docs - Fòm HTML**: 
  https://developer.mozilla.org/en-US/docs/Learn/Forms
  
- **W3Schools - Fòm HTML**: 
  https://www.w3schools.com/html/html_forms.asp
  
- **MDN - Eleman Form**: 
  https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form
  
- **MDN - Eleman Input**: 
  https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input
  
- **W3Schools - Tip Input**: 
  https://www.w3schools.com/html/html_form_input_types.asp
  
- **MDN - Validasyon Fòm**: 
  https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation

### Zouti ak Tès

- **WebStorm** - IDE ou pou ekri HTML
- **Zouti Devlopè Navigatè** - Peze F12 pou wè konsòl pou teste soumisyon fòm
- **Git & GitHub** - Kontwòl vèsyon pou pwojè fòm ou yo

### Pwochèn Etap

Apre ou metrize fòm HTML, w ap pare pou:
1. Bay estil fòm ak CSS (pwochèn inite)
2. Ajoute konpòtman dinamik ak JavaScript
3. Konekte fòm ak vrè sèvè
4. Konstwi aplikasyon entènèt entèaktif

Sonje: Fòm se pòtay entèraksyon itilizatè sou entènèt. Pratike kreye diferan kalite fòm pou vin alèz ak tout eleman ak atribi yo!

---

*Fen Nòt Kou - Fòm HTML*