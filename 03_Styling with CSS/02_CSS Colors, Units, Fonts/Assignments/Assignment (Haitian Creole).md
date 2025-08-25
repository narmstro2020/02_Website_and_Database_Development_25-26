# Devwa 1: Kreyatè Palèt Koulè

## Objektif
Kreye yon paj entènèt ki montre konpreyansyon ou sou fòma koulè CSS lè w konstwi yon ekspozisyon palèt koulè. W ap kreye echantiyon koulè lè w itilize diferan fòma koulè epi aplike yo sou plizyè eleman HTML.

## Kondisyon

### Estrikti HTML
Kreye yon fichye HTML ak:
1. Yon tit prensipal (h1) pou tit paj la
2. Sis seksyon, chak gen ladan l:
   - Yon sou-tit (h2) pou non fòma koulè a
   - Omwen 3 eleman paragraf ki montre diferan koulè
   - Yon eleman article ak yon fon kolore

### Kondisyon CSS
Ou dwe montre TOUT fòma koulè sa yo:
1. **Seksyon Koulè ki gen Non**: Itilize omwen 5 koulè diferan ki gen non
2. **Seksyon Egzadesimal**: Itilize koulè hex konplè (#RRVVBB) ak abreje (#RVB)
3. **Seksyon RGB**: Kreye koulè lè w itilize valè rgb()
4. **Seksyon RGBA**: Montre transparans ak omwen 3 valè alfa diferan
5. **Seksyon HSL**: Kreye yon chema koulè lè w itilize hsl()
6. **Seksyon HSLA**: Konbine HSL ak transparans

### Travay Espesifik
1. Kreye yon efè "lakansyèl" lè w itilize omwen 7 koulè diferan nan nenpòt fòma
2. Montre transparans lè w mete eleman youn sou lòt ak RGBA oswa HSLA
3. Kreye yon chema koulè monokwomatik (diferan ton menm koulè a)
4. Estilize koulè tèks la AK koulè fon an pou chak seksyon
5. Ajoute yon pye paj ak yon efè tankou degrade lè w itilize transparans

## Kòd Pou Kòmanse

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ekspozisyon Palèt Koulè</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Ekspozisyon Palèt Koulè CSS</h1>
    </header>
    
    <main>
        <section>
            <h2>Koulè ki gen Non</h2>
            <p>Tèks sa a itilize yon koulè ki gen non.</p>
            <p>Sa a gen yon koulè ki gen non diferan.</p>
            <p>Sa a konbine koulè tèks ak koulè fon ki gen non.</p>
            <article>
                Atik sa a gen yon fon koulè ki gen non.
            </article>
        </section>
        
        <!-- Ajoute plis seksyon pou chak fòma koulè -->
        
    </main>
    
    <footer>
        <p>Pye paj ak efè koulè kreyatif</p>
    </footer>
</body>
</html>
```

styles.css
```css
        body {
            /* Ajoute yon koulè fon klè */
        }
        
        h1 {
            /* Santre epi estilize tit prensipal la */
        }
        
        section {
            /* Ajoute espas ant seksyon yo */
        }
        
        /* Ajoute estil koulè ou yo anba a */


```

## Konsèy
- Itilize kòmantè nan CSS ou pou etikèt chak seksyon fòma koulè
- Teste transparans lè w mete eleman youn sou lòt
- Sonje valè tèn HSL ale de 0-360 degre
- Pou lakansyèl la, panse sou wou koulè a
- Yon chema monokwomatik ka itilize diferan valè limyè oswa satiasyon

## Soumèt
Voye de fichye:
1. `palèt-koulè.html` - Fichye HTML konplè ou a ak CSS entegre
2. Yon kaptire ekran paj entènèt ou a

## Defi Anplis (Si w vle)
Kreye yon desen "kat koulè" kote chak echantiyon koulè sanble ak yon kat fizik ak:
- Yon efè lonbraj lè w itilize RGBA
- Valè koulè a montre kòm tèks sou kat la
- Kwen awondi lè w itilize CSS ou chèche ou menm