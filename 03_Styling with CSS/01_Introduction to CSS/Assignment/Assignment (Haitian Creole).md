# Devwa 3: Sit Entènèt Plizyè Paj - Modèl

## Enstriksyon
Kreye yon sit entènèt 3 paj lè w itilize **CSS ekstèn**. Tout paj yo dwe konekte ak menm fichye CSS la.

## Lis Kondisyon
- [ ] Kreye twa fichye HTML: home.html, about.html, contact.html
- [ ] Kreye yon fichye styles.css
- [ ] Konekte tout paj HTML yo ak menm fichye CSS la
- [ ] Mete lyen navigasyon ant tout paj yo
- [ ] Bay menm estil pou tit, paragraf, ak lyen yo
- [ ] Itilize bon estrikti HTML sou tout paj yo

## Estrikti Fichye
```
assignment3/
│
├── home.html
├── about.html
├── contact.html
└── styles.css
```

## Modèl HTML

### home.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Akèy - Sit Entènèt Mwen</title>
    <meta charset="UTF-8">
    <!-- Lyen pou fichye CSS ekstèn -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Byenveni sou Sit Entènèt Mwen</h1>
        <nav>
            <ul>
                <li><a href="home.html">Akèy</a></li>
                <li><a href="about.html">Konsènan</a></li>
                <li><a href="contact.html">Kontak</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Paj Akèy</h2>
            <p>Byenveni sou sit entènèt mwen! Sa se paj akèy la.</p>
            <p>Ajoute plis kontni sou sa sit entènèt ou a ofri.</p>
        </section>
        
        <section>
            <h3>Kontni Enpòtan</h3>
            <p>Ajoute kèk kontni enteresan isit la.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Sit Entènèt Mwen. Tout dwa rezève.</p>
    </footer>
</body>
</html>
```

### about.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Konsènan - Sit Entènèt Mwen</title>
    <meta charset="UTF-8">
    <!-- Lyen pou fichye CSS ekstèn -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Konsènan Nou</h1>
        <nav>
            <ul>
                <li><a href="home.html">Akèy</a></li>
                <li><a href="about.html">Konsènan</a></li>
                <li><a href="contact.html">Kontak</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Istwa Nou</h2>
            <p>Rakonte istwa ou isit la.</p>
            <p>Ajoute enfòmasyon sou bak plan ou.</p>
        </section>
        
        <section>
            <h3>Misyon Nou</h3>
            <p>Dekri misyon ou oswa objektif ou yo.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Sit Entènèt Mwen. Tout dwa rezève.</p>
    </footer>
</body>
</html>
```

### contact.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Kontak - Sit Entènèt Mwen</title>
    <meta charset="UTF-8">
    <!-- Lyen pou fichye CSS ekstèn -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Kontakte Nou</h1>
        <nav>
            <ul>
                <li><a href="home.html">Akèy</a></li>
                <li><a href="about.html">Konsènan</a></li>
                <li><a href="contact.html">Kontak</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Antre an Kontak</h2>
            <p>Nou ta renmen tande ou!</p>
            
            <h3>Enfòmasyon Kontak</h3>
            <p><strong>Imèl:</strong> info@sitweb.com</p>
            <p><strong>Telefòn:</strong> (555) 123-4567</p>
            <p><strong>Adrès:</strong> 123 Ri Web, Vil Entènèt, WWW 12345</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Sit Entènèt Mwen. Tout dwa rezève.</p>
    </footer>
</body>
</html>
```

### styles.css (Modèl)
```css
/* Reyinisyalize estil pa defo */
body {
    /* Ajoute estil pou body */
}

/* Estil antèt */
header {
    /* Ajoute estil antèt */
}

/* Estil tit */
h1 {
    /* Ajoute estil h1 */
}

h2 {
    /* Ajoute estil h2 */
}

h3 {
    /* Ajoute estil h3 */
}

/* Estil navigasyon */
nav {
    /* Ajoute estil nav */
}

nav ul {
    /* Ajoute estil pou lis navigasyon */
}

nav li {
    /* Ajoute estil pou eleman lis */
}

/* Estil lyen */
a {
    /* Ajoute estil lyen */
}

a:hover {
    /* Ajoute efè hover pou lyen */
}

/* Estil kontni prensipal */
main {
    /* Ajoute estil main */
}

/* Estil seksyon */
section {
    /* Ajoute estil seksyon */
}

/* Estil paragraf */
p {
    /* Ajoute estil paragraf */
}

/* Estil pye paj */
footer {
    /* Ajoute estil pye paj */
}
```

## Pwopriyete CSS pou Konsidere
- Koulè background ak tèks
- Fanmi ak gwosè polis
- Ranpli ak maj
- Aliyman tèks
- Bòdi
- Pwopriyete dispozisyon pou navigasyon
- Efè hover pou lyen

## Konsèy
1. Kenbe CSS ou òganize ak kòmantè
2. Teste tout lyen navigasyon yo
3. Asire w ke chemen fichye CSS la kòrèk nan tout fichye HTML yo
4. Itilize espas ak koulè ki konsistan sou tout paj yo
5. Konsidere ajoute yon efè hover sou lyen navigasyon yo

## Enstriksyon pou Soumèt
1. Kreye yon katab ki rele `assignment3`
2. Mete kat fichye yo nan katab sa a
3. Teste tout paj ak navigasyon nan navigatè ou
4. Konfime nan Git ak mesaj: "Fini Devwa 3: Sit Entènèt Plizyè Paj ak CSS Ekstèn"
5. Pouse sou GitHub