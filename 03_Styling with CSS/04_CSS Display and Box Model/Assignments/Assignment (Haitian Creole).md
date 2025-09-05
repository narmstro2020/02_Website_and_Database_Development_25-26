# Travay 2: Espas Modèl Bwat la

## Objektif
Kreye yon aranjman kat ki montre ou konnen Modèl Bwat CSS la byen. W ap konstwi twa kat enfòmasyon ak espas ki kòrèk lè w ap itilize margin, padding ak borders.

## Kondisyon yo
1. Kreye twa kat ki montre diferan kalite kontni
2. Itilize padding pou kreye espas anndan chak kat
3. Itilize margins pou separe kat yo youn ak lòt
4. Ajoute borders pou defini lizyè kat yo
5. Santre kontènè kat yo sou paj la
6. Fè kat yo gen menm wotè kèlkeswa kontni an

## Estrikti HTML Kòmanse
styles.css
```css
        /* Remet estil yo pa defo */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            /* TODO: Ajoute padding nan body */
        }
        
        .container {
            /* TODO: Mete max-width */
            /* TODO: Santre kontènè a ak margin */
            /* TODO: Ajoute koulè fon */
            /* TODO: Ajoute padding */
        }
        
        h1 {
            /* TODO: Ajoute margin bottom */
            /* TODO: Santre tèks la */
            /* TODO: Ajoute koulè */
        }
        
        .cards {
            /* TODO: Konfigire kontènè pou kat yo */
        }
        
        .card {
            /* TODO: Mete lajè (konsidere itilize pousantaj) */
            /* TODO: Ajoute padding pou espas anndan */
            /* TODO: Ajoute margin pou espas deyò */
            /* TODO: Ajoute border */
            /* TODO: Mete koulè fon */
            /* TODO: Mete wotè minimòm */
        }
        
        .card h2 {
            /* TODO: Ajoute margin bottom */
            /* TODO: Ajoute padding bottom */
            /* TODO: Ajoute border anba */
            /* TODO: Mete koulè */
        }
        
        .card p {
            /* TODO: Ajoute margin bottom pou espas paragraf */
            /* TODO: Mete wotè liy */
        }
        
        .card-footer {
            /* TODO: Ajoute margin top */
            /* TODO: Ajoute padding top */
            /* TODO: Ajoute border anlè */
            /* TODO: Mete aranjman tèks */
        }
        
        .button {
            /* TODO: Retire estil defo bouton an */
            /* TODO: Ajoute padding */
            /* TODO: Ajoute margin */
            /* TODO: Ajoute border */
            /* TODO: Mete koulè fon */
            /* TODO: Mete koulè tèks */
            /* TODO: Ajoute cursor pointer */
        }
        
        .button:hover {
            /* TODO: Ajoute efè hover */
        }
        
        /* Estil kat espesyal yo */
        .featured {
            /* TODO: Ajoute estil espesyal pou kat ki parèt yo */
            /* TODO: Konsidere border oswa fon diferan */
        }
```

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Aranjman Kat Modèl Bwat</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Sèvis Nou yo</h1>
        
        <div class="cards">
            <div class="card">
                <h2>Konsèpsyon Web</h2>
                <p>Kreye sit entènèt bèl ak reponsif ki fonksyone sou tout aparèy yo. Konsèpsyon nou yo modèn, pwòp ak fasil pou itilize.</p>
                <p>Nou itilize teknoloji ki pi nouvo yo ki gen ladan HTML5, CSS3 ak frameworks modèn yo.</p>
                <div class="card-footer">
                    <button class="button">Aprann Plis</button>
                </div>
            </div>
            
            <div class="card featured">
                <h2>Devlopman</h2>
                <p>Konstwi aplikasyon web solid ak kòd pwòp ak maintnable. Depi sit senp rive nan aplikasyon konplèks yo.</p>
                <p>Sèvis devlopman full-stack ak yon focus sou pèfòmans ak sekirite.</p>
                <p>Òf espesyal: Jwenn 20% rabè sou premye pwojè ou a!</p>
                <div class="card-footer">
                    <button class="button">Kòmanse</button>
                </div>
            </div>
            
            <div class="card">
                <h2>Konsèy</h2>
                <p>Konsèy ekspè pou ede biznis ou reyisi sou entènèt. Nou analize bezwen ou yo epi nou bay solisyon ki fèt pou ou.</p>
                <div class="card-footer">
                    <button class="button">Kontakte Nou</button>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

## Travay yo pou Fè

### Travay 1: Konfigirasyon Kontènè a
1. Mete yon max-width pou kontènè a (sijesyon: 1200px)
2. Santre kontènè a lè w ap itilize margin auto
3. Ajoute padding pou kreye espas anndan kontènè a

### Travay 2: Estil Kat yo
1. Ajoute padding anndan chak kat (eseye 20px)
2. Ajoute margins ant kat yo (sijesyon: 15px)
3. Ajoute yon border pou defini rebò kat yo
4. Mete yon wotè minimòm pou tout kat yo egal

### Travay 3: Espas Kontni an
1. Ajoute margin nan tèt ak paragraf yo
2. Kreye separasyon vizyèl ant tèt kat la ak kontni an
3. Estilize pye kat la ak borders ak espas

### Travay 4: Kat ki Parèt la
1. Bay kat ki parèt la yon koulè oswa estil border diferan
2. Konsidere ajoute yon koulè fon diferan
3. Petèt ogmante padding an oswa ajoute yon lonbraj bwat

### Travay 5: Estil Bouton yo
1. Retire aparans defo bouton an
2. Ajoute padding pou yon pi bon zòn klike
3. Estilize ak koulè ak borders
4. Ajoute efè hover yo

## Rezèlta ki Atann nan
- Twa kat ki espase menm jan nan yon ranje
- Espas anndan konsèkan nan chak kat
- Yerachi vizyèl klè ak tèt, kontni ak pye yo
- Kat ki parèt la diferan ak lòt yo
- Bouton yo estilize ak entèraktif