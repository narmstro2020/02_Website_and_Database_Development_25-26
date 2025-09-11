# Estilize Fòm ak Tab yo ak CSS

## Tab Matye yo

| Sijè | Deskripsyon |
|------|-------------|
| [Entwodiksyon](#entwodiksyon) | Apèsi sou estil fòm ak tab yo |
| [Vokabilè](#vokabilè) | Tèm yo ak definisyon yo |
| [1. Estilize Tab yo ak CSS](#1-estilize-tab-yo-ak-css) | Aprann estilize tab HTML yo |
| [2. Estilize Fòm yo ak CSS](#2-estilize-fòm-yo-ak-css) | Aprann estilize fòm HTML yo |
| [Egzanp Vizyèl yo](#egzanp-vizyèl-yo) | Egzanp konplè k ap fonksyone |
| [Devwa yo](#devwa-yo) | Egzèsis pratik yo |
| [Rezime](#rezime) | Pwen enpòtan yo pou sonje |
| [Resous yo](#resous-yo) | Matèl pou aprann pi plis |

---

## Entwodiksyon

Byenveni nan leson nou an sou estilize fòm ak tab yo ak CSS! Fòm ak tab yo se eleman enpòtan nan devlopman wèb la. Tab yo ede nou òganize done yo nan ranje ak kolòn yo, pandan fòm yo pèmèt itilizatè yo antre ak soumèt enfòmasyon. Nan leson sa a, nou pral aprann ki jan pou nou fè eleman sa yo vin pi atiran ak pi fasil pou itilize lè w ap sèvi ak CSS.

### Sa W Pral Aprann:
- Ki jan pou estilize fwontyè, espas ak background tab yo
- Ki jan pou kreye fòm ki atiran ak ki aksesib
- Pi bon pratik yo pou konsèy fòm ak tab yo
- Pwopriyete CSS yo ki espesifik pou fòm ak tab yo

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

## Vokabilè

### Tèm ki gen Rapò ak Tab yo
- **border-collapse**: Pwopriyete CSS ki detèmine si fwontyè tab yo separe oswa yo kolapse nan yon sèl fwontyè
- **border-spacing**: Pwopriyete CSS ki mete distans lan ant fwontyè selil tab yo ki kote kote
- **caption-side**: Pwopriyete CSS ki pozisyone yon tit tab
- **thead**: Eleman HTML ki gwupe kontni tèt la nan yon tab
- **tbody**: Eleman HTML ki gwupe kontni kò a nan yon tab
- **tfoot**: Eleman HTML ki gwupe kontni pye a nan yon tab
- **nth-child()**: Selektè pseudo-class CSS ki matche ak eleman yo ki baze sou pozisyon yo

### Tèm ki gen Rapò ak Fòm yo
- **fieldset**: Eleman HTML ki gwupe kontwòl fòm yo ki gen rapò
- **legend**: Eleman HTML ki bay yon tit pou yon fieldset
- **placeholder**: Atribi HTML ki bay tèks konsèy nan antre fòm yo
- **focus**: Eta a lè yon eleman fòm chwazi/aktif
- **:focus**: Pseudo-class CSS ki estilize yon eleman lè li gen focus
- **:hover**: Pseudo-class CSS ki estilize yon eleman lè sourit la pase sou li
- **:disabled**: Pseudo-class CSS ki estilize eleman fòm yo ki dezaktive
- **outline**: Pwopriyete CSS ki fè yon liy nan alantou eleman yo (yo souvan wè li sou focus)

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

## 1. Estilize Tab yo ak CSS

Tab yo se zouti pwisan yo pou montre done ki gen estrikti. Ann aprann ki jan pou nou fè yo bèl ak fonksyonèl.

### Revizyon Estrikti De Baz Tab yo

```html
<table>
    <caption>Nòt Elèv yo</caption>
    <thead>
        <tr>
            <th>Non</th>
            <th>Nòt</th>
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

### Pwopriyete Esansyèl Estil Tab yo

#### 1. Kolaps Fwontyè

Pwopriyete `border-collapse` kontwole ki jan fwontyè tab yo konpòte yo:

```css
/* Fwontyè yo separe (defo) */
table {
    border-collapse: separate;
    border-spacing: 2px;
}

/* Fwontyè yo kolapse (rekòmande) */
table {
    border-collapse: collapse;
}
```

#### 2. Ajoute Fwontyè yo

```css
table {
    border: 2px solid #333;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
}
```

#### 3. Estilize Tèt Tab yo

```css
th {
    background-color: #4CAF50;
    color: white;
    font-weight: bold;
    text-align: left;
    padding: 12px;
}
```

#### 4. Koulè Ranje ki Alène (Ret Zèb yo)

```css
/* Ranje ki gen nimewo pa */
tbody tr:nth-child(even) {
    background-color: #f2f2f2;
}

/* Ranje ki gen nimewo enpè */
tbody tr:nth-child(odd) {
    background-color: white;
}
```

#### 5. Efè Hover yo

```css
tbody tr:hover {
    background-color: #ddd;
    cursor: pointer;
}
```

### Egzanp Tab Konplè

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tab ki Estilize</title>
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
        <caption>Enventè Pwodwi yo</caption>
        <thead>
            <tr>
                <th>Pwodwi</th>
                <th>Kantite</th>
                <th>Pri</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Òdinatè Potab</td>
                <td>15</td>
                <td>$999</td>
            </tr>
            <tr>
                <td>Sourit</td>
                <td>50</td>
                <td>$25</td>
            </tr>
            <tr>
                <td>Klavye</td>
                <td>30</td>
                <td>$75</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### Tab Responsive yo

Pou pi bon jan gade sou mobil:

```css
/* Kontenyè pou woule orizontal sou ti ekran yo */
.table-container {
    overflow-x: auto;
}

table {
    min-width: 600px;
}
```

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

## 2. Estilize Fòm yo ak CSS

Fòm yo se ki jan itilizatè yo kominike ak sit wèb ou a. Yon bon konsèy fòm amelyore ekspèryans itilizatè a ak ogmante to a yo ki konplete.

### Revizyon Estrikti De Baz Fòm yo

```html
<form>
    <label for="non">Non:</label>
    <input type="text" id="non" name="non">
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    
    <input type="submit" value="Voye">
</form>
```

### Teknik Esansyèl Estil Fòm yo

#### 1. Estil De Baz Antre yo

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

#### 2. Estil Etikèt yo

```css
label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}
```

#### 3. Eta Focus yo

```css
input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
    outline: none;
    border-color: #4CAF50;
    box-shadow: 0 0 5px rgba(76, 175, 80, 0.3);
}
```

#### 4. Estil Bouton yo

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

#### 5. Fieldset ak Legend

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

### Egzanp Fòm Konplè

```html
<!DOCTYPE html>
<html>
<head>
    <title>Fòm ki Estilize</title>
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
        <h2>Fòm Enskripsyon</h2>
        
        <label for="non">Non:</label>
        <input type="text" id="non" name="non" placeholder="Antre non ou">
        
        <label for="fanmi">Non Fanmi:</label>
        <input type="text" id="fanmi" name="fanmi" placeholder="Antre non fanmi ou">
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" placeholder="ou@email.com">
        
        <label for="peyi">Peyi:</label>
        <select id="peyi" name="peyi">
            <option value="">Chwazi peyi ou</option>
            <option value="haiti">Ayiti</option>
            <option value="usa">Etazini</option>
            <option value="canada">Kanada</option>
        </select>
        
        <button type="submit">Enskri</button>
    </form>
</body>
</html>
```

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

## Egzanp Vizyèl yo

### Egzanp 1: Tab Done Pwofesyonèl

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tab Pwofesyonèl</title>
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
        
        .status-aktif {
            background-color: #d4edda;
            color: #155724;
        }
        
        .status-ap-tann {
            background-color: #fff3cd;
            color: #856404;
        }
    </style>
</head>
<body>
    <div class="table-container">
        <table>
            <caption>Lis Anplwaye yo</caption>
            <thead>
                <tr>
                    <th>Non</th>
                    <th>Depatman</th>
                    <th>Email</th>
                    <th>Estatik</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Jean Pierre</td>
                    <td>Enjenyè</td>
                    <td>jean@konpani.com</td>
                    <td><span class="status status-aktif">Aktif</span></td>
                </tr>
                <tr>
                    <td>Marie Joseph</td>
                    <td>Maketing</td>
                    <td>marie@konpani.com</td>
                    <td><span class="status status-aktif">Aktif</span></td>
                </tr>
                <tr>
                    <td>Paul Moïse</td>
                    <td>Lavant</td>
                    <td>paul@konpani.com</td>
                    <td><span class="status status-ap-tann">Ap Tann</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

## Devwa yo

### Devwa 1: Estilize yon Tab Pwodwi yo
Kreye ak estilize yon tab ki montre omwen 5 pwodwi yo ak kolòn pou Non Pwodwi a, Kategori, Pri ak Eta Stock la.

**Egzijans yo:**
- Itilize koulè ranje ki alène
- Ajoute efè hover yo
- Estilize tèt la ak yon koulè background ki diferan
- Mete yon tit tab
- Fè fwontyè yo kolapse
- Ajoute espas ki apwopriye

### Devwa 2: Kreye yon Fòm Enskripsyon ki Estilize
Konstwi yon fòm enskripsyon ak divès tip antre ak estil pwofesyonèl.

**Egzijans yo:**
- Mete chan tèks, email, mo pase, select ak textarea
- Itilize fieldset yo pou gwupe chan yo ki gen rapò
- Ajoute eta focus nan tout antre yo
- Estilize bouton soumèt la ak efè hover
- Mete tèks placeholder
- Fè fòm lan responsive

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

## Rezime

### Pwen Enpòtan yo pou Sonje

#### Tab yo
- Itilize `border-collapse: collapse` pou konsèy tab yo ki pi pwòp
- Aplike selektè `:nth-child()` yo pou koulè ranje ki alène
- Toujou mete estrikti tab ki apwopriye (thead, tbody, tfoot)
- Ajoute efè hover yo pou amelyore entèraksyon itilizatè a
- Itilize padding pou kreye espas nan selil yo

#### Fòm yo
- Estilize tout eta fòm yo: defo, hover, focus ak dezaktive
- Gwupe chan yo ki gen rapò ak fieldset yo
- Itilize espas ak aliyman ki konsèkan
- Bay retou vizyèl ki klè pou entèraksyon itilizatè yo
- Toujou mete etikèt yo pou aksesibilite
- Itilize tèks placeholder pou gide itilizatè yo

### Pwopriyete CSS yo ki Aprann

**Pwopriyete Tab yo:**
- `border-collapse`
- `border-spacing`
- `caption-side`
- `:nth-child()`

**Pwopriyete Fòm yo:**
- `:focus`
- `:hover`
- `:disabled`
- `:valid` / `:invalid`
- `outline`
- `box-shadow`
- `transition`

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

## Resous yo

### Dokimantasyon
- [MDN - Estilize Tab yo](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Styling_tables)
- [MDN - Estilize Fòm yo](https://developer.mozilla.org/en-US/docs/Learn/Forms/Styling_web_forms)
- [W3Schools - Tab CSS yo](https://www.w3schools.com/css/css_table.asp)
- [W3Schools - Fòm CSS yo](https://www.w3schools.com/css/css_form.asp)

### Referans CSS yo
- [MDN - border-collapse](https://developer.mozilla.org/en-US/docs/Web/CSS/border-collapse)
- [MDN - :nth-child()](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-child)
- [MDN - :focus](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus)
- [MDN - fieldset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset)

[↑ Retounen nan Tab la](#estilize-fòm-ak-tab-yo-ak-css)

---

*Fen Nòt Klas yo - Estilize Fòm ak Tab yo ak CSS*