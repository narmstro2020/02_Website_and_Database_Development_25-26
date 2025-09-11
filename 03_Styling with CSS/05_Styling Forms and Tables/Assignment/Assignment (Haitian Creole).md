# Devwa 1: Estilize yon Tab Pwodwi yo

## Objektif
Estilize yon tab ki montre omwen 5 pwodwi yo ak yon estil pwofesyonèl.

## Egzijans yo
- [ ] Itilize koulè ranje ki alène (ret zèb yo)
- [ ] Ajoute efè hover nan ranje tab yo
- [ ] Estilize tèt la ak yon koulè background ki diferan
- [ ] Mete yon tit tab ki eksplike
- [ ] Sèvi ak fwontyè ki kole ansanm
- [ ] Ajoute espas ki apwopriye nan tout selil yo
- [ ] Fè tab la responsive ak ki gen bèl aparans

## Kòd Kòmanse

### styles.css 

```css
/* Reset ak estil debaz yo */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    /* Ajoute estil body ou yo isit la */
}

/* Estil tab yo */
table {
    /* Ajoute estil tab ou yo isit la */
}

caption {
    /* Estilize tit tab la */
}

/* Estil tèt yo */
thead {
    /* Ajoute estil thead yo si ou bezwen */
}

th {
    /* Estilize tèt tab yo */
}

/* Estil kò yo */
tbody {
    /* Ajoute estil tbody yo si ou bezwen */
}

td {
    /* Estilize selil tab yo */
}

/* Ret zèb yo - koulè ranje ki alène */
/* Ajoute selektè nth-child ou yo isit la */

/* Efè hover */
/* Ajoute estil hover ou yo isit la */
```

### index.html ki deja konstwi

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tab Enventè Pwodwi yo</title>
    <style>

        
    </style>
</head>
<body>
    <div class="table-wrapper">
        <table>
            <caption>Enventè Pwodwi yo - Boutik Elektwonik</caption>
            <thead>
                <tr>
                    <th>Non Pwodwi a</th>
                    <th>Kategori</th>
                    <th>Pri</th>
                    <th>Eta Stock la</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>MacBook Pro 14"</td>
                    <td>Òdinatè Potab yo</td>
                    <td>$1,999.00</td>
                    <td><span class="stock-status in-stock">Gen nan Stock</span></td>
                </tr>
                <tr>
                    <td>iPhone 15 Pro</td>
                    <td>Telefòn Entèlijàn yo</td>
                    <td>$999.00</td>
                    <td><span class="stock-status in-stock">Gen nan Stock</span></td>
                </tr>
                <tr>
                    <td>iPad Air</td>
                    <td>Tablèt yo</td>
                    <td>$599.00</td>
                    <td><span class="stock-status low-stock">Stock Ki Ba</span></td>
                </tr>
                <tr>
                    <td>AirPods Pro</td>
                    <td>Odyo</td>
                    <td>$249.00</td>
                    <td><span class="stock-status in-stock">Gen nan Stock</span></td>
                </tr>
                <tr>
                    <td>Apple Watch Series 9</td>
                    <td>Bagay yo Mete sou Kò</td>
                    <td>$399.00</td>
                    <td><span class="stock-status out-of-stock">Pa gen nan Stock</span></td>
                </tr>
                <tr>
                    <td>Magic Keyboard</td>
                    <td>Akseswa yo</td>
                    <td>$299.00</td>
                    <td><span class="stock-status in-stock">Gen nan Stock</span></td>
                </tr>
                <tr>
                    <td>Studio Display</td>
                    <td>Monitè yo</td>
                    <td>$1,599.00</td>
                    <td><span class="stock-status low-stock">Stock Ki Ba</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

## Konsèy yo
1. Itilize `border-collapse: collapse` sou tab la pou fwontyè yo pi pwòp
2. Konsidere itilize koulè yo ki matche ak yon sistèm koulè ki konsèkan
3. Pou ret zèb yo, itilize `tbody tr:nth-child(even)` ak `tbody tr:nth-child(odd)`
4. Ajoute yon tranzisyon yo ki dou pou efè hover a pou fè li sèlman
5. Konsidere ajoute koulè diferan oswa mak yo pou eta stock la (Gen nan Stock, Stock Ki Ba, Pa gen nan Stock)

## Defi Bonus yo
- Ajoute yon seksyon tfoot ak total yo
- Estilize eta stock la ak mak ki gen koulè
- Aliyen kolòn pri a sou dwat la
- Ajoute yon lonbraj yo ki dou nan tab la

## Soumèt
Konsève dosye ou a kòm `tab-pwodwi.html` ak teste li nan navigatè ou a. Asire w ke tout egzijans yo satisfè anvan ou soumèt li nan GitHub.