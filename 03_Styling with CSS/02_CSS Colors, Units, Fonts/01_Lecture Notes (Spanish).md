# Colores, Unidades y Fuentes CSS - Notas de Clase

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

## Tabla de Contenidos

| Tema | Descripción |
|------|-------------|
| [Introducción](#introducción) | Descripción general de colores, unidades y fuentes CSS |
| [Colores CSS](#colores-css) | RGB, RGBA, HSL, HSLA, Hexadecimal y Colores Nombrados |
| [Unidades CSS](#unidades-css) | Unidades Absolutas y Relativas |
| [Fuentes CSS](#fuentes-css) | Propiedades de Fuente y Tipografía Web |
| [Vocabulario](#vocabulario) | Términos clave y definiciones |
| [Tareas](#tareas) | Ejercicios prácticos |
| [Resumen](#resumen) | Puntos clave para recordar |
| [Recursos](#recursos) | Material de aprendizaje adicional |

---

## Introducción

En esta lección, exploraremos tres aspectos fundamentales del estilo CSS que transformarán sus páginas web de texto simple a diseños visualmente atractivos. Aprenderá cómo agregar colores, controlar el tamaño con diferentes unidades y estilizar texto con varias propiedades de fuente.

### Prerrequisitos
- Estructura de documento HTML (DOCTYPE, html, head, body)
- Etiquetas HTML básicas (h1-h6, p, em, strong)
- HTML semántico (header, footer, main, section, article)
- Listas (ul, ol, li)
- Enlaces e imágenes
- Sintaxis CSS básica y selectores de lecciones anteriores

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

---

## Colores CSS

CSS proporciona múltiples formas de especificar colores. Cada método tiene sus ventajas y casos de uso.

### 1. Colores Nombrados

CSS admite 140 nombres de colores estándar que puede usar directamente.

```css
/* Usando colores nombrados */
p {
    color: red;
    background-color: lightblue;
}

h1 {
    color: darkgreen;
    background-color: gold;
}
```

**Colores Nombrados Comunes:**
- Primarios: red, blue, green, yellow
- Neutrales: black, white, gray, silver
- Extendidos: coral, salmon, turquoise, violet

### 2. Colores Hexadecimales

Los colores hexadecimales (hex) usan un # seguido de 6 caracteres (0-9 y A-F).

```css
/* Formato de color hexadecimal: #RRVVAA */
p {
    color: #FF0000;      /* Rojo puro */
    background-color: #00FF00;  /* Verde puro */
}

h1 {
    color: #0000FF;      /* Azul puro */
    background-color: #FFFFFF;  /* Blanco */
}

/* Hex abreviado (cuando los pares coinciden) */
h2 {
    color: #F00;        /* Igual que #FF0000 */
    background-color: #0F0;     /* Igual que #00FF00 */
}
```

**Entendiendo los Colores Hex:**
- Primeros dos caracteres: Valor rojo (00-FF)
- Dos caracteres del medio: Valor verde (00-FF)
- Últimos dos caracteres: Valor azul (00-FF)
- 00 = sin color, FF = color máximo

### 3. Colores RGB

RGB usa valores decimales de 0-255 para Rojo, Verde y Azul.

```css
/* Formato de color RGB: rgb(rojo, verde, azul) */
p {
    color: rgb(255, 0, 0);      /* Rojo puro */
    background-color: rgb(0, 255, 0);   /* Verde puro */
}

h1 {
    color: rgb(0, 0, 255);      /* Azul puro */
    background-color: rgb(128, 128, 128); /* Gris */
}

/* Mezclando colores */
h2 {
    color: rgb(255, 165, 0);    /* Naranja */
    background-color: rgb(128, 0, 128);  /* Púrpura */
}
```

### 4. Colores RGBA

RGBA añade un canal alfa para transparencia (0 = completamente transparente, 1 = completamente opaco).

```css
/* Formato RGBA: rgba(rojo, verde, azul, alfa) */
p {
    background-color: rgba(255, 0, 0, 0.5);   /* Rojo 50% transparente */
}

section {
    background-color: rgba(0, 0, 255, 0.3);   /* Azul 30% opaco */
}

/* Capas con transparencia */
header {
    background-color: rgba(0, 0, 0, 0.8);     /* Negro 80% opaco */
    color: rgba(255, 255, 255, 1);            /* Blanco completamente opaco */
}
```

### 5. Colores HSL

HSL significa Matiz, Saturación y Luminosidad - un modelo de color más intuitivo.

```css
/* Formato HSL: hsl(matiz, saturación%, luminosidad%) */
p {
    color: hsl(0, 100%, 50%);      /* Rojo */
    background-color: hsl(120, 100%, 50%);  /* Verde */
}

h1 {
    color: hsl(240, 100%, 50%);    /* Azul */
}

/* Creando variaciones de color */
section {
    background-color: hsl(200, 50%, 70%);   /* Azul claro */
}
```

**Entendiendo HSL:**
- Matiz: 0-360 grados en la rueda de color (0=rojo, 120=verde, 240=azul)
- Saturación: 0% = gris, 100% = color completo
- Luminosidad: 0% = negro, 50% = normal, 100% = blanco

### 6. Colores HSLA

HSLA añade transparencia a los colores HSL.

```css
/* Formato HSLA: hsla(matiz, saturación%, luminosidad%, alfa) */
article {
    background-color: hsla(60, 100%, 50%, 0.5);  /* Amarillo 50% transparente */
}

footer {
    background-color: hsla(0, 0%, 0%, 0.9);      /* Negro 90% opaco */
}
```

### Guía Visual de Colores

```css
/* Ejemplo completo de colores */
body {
    background-color: #f0f0f0;  /* Fondo gris claro */
}

header {
    background-color: rgb(51, 51, 51);  /* Gris oscuro */
    color: white;
}

main {
    background-color: rgba(255, 255, 255, 0.95);  /* Blanco ligeramente transparente */
}

footer {
    background-color: hsl(210, 50%, 30%);  /* Azul oscuro */
    color: hsla(0, 0%, 100%, 0.9);  /* Blanco ligeramente transparente */
}
```

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

---

## Unidades CSS

Las unidades CSS determinan el tamaño de los elementos. Se dividen en dos categorías: absolutas y relativas.

### Unidades Absolutas

Las unidades absolutas tienen un tamaño fijo independientemente de otras configuraciones.

#### Píxeles (px)
La unidad absoluta más común para pantalla.

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

#### Otras Unidades Absolutas
Menos utilizadas pero disponibles:

```css
/* Unidades absolutas raramente usadas */
p {
    margin: 0.5in;    /* pulgadas */
    padding: 1cm;     /* centímetros */
    border: 2mm;      /* milímetros */
    width: 12pt;      /* puntos (1pt = 1/72 pulgada) */
    height: 1pc;      /* picas (1pc = 12pt) */
}
```

### Unidades Relativas

Las unidades relativas escalan basándose en otros valores, haciendo los diseños más flexibles.

#### Porcentajes (%)
Relativo al tamaño del elemento padre.

```css
/* Unidades porcentuales */
section {
    width: 80%;           /* 80% del ancho del padre */
    margin: 0 auto;       /* Centrar la sección */
}

article {
    width: 50%;           /* Mitad del ancho del padre */
    padding: 5%;          /* 5% del ancho del padre */
}

img {
    width: 100%;          /* Ancho completo del contenedor */
    height: auto;         /* Mantener relación de aspecto */
}
```

#### Unidades Em (em)
Relativo al tamaño de fuente del elemento (o el tamaño de fuente del padre para otras propiedades).

```css
/* Unidades em */
p {
    font-size: 1em;       /* Igual al tamaño de fuente del padre */
    margin: 1.5em;        /* 1.5 veces el tamaño de fuente */
    padding: 0.5em;       /* Mitad del tamaño de fuente */
}

h1 {
    font-size: 2em;       /* Dos veces el tamaño de fuente del padre */
    margin-bottom: 0.5em; /* Mitad del tamaño de fuente de h1 */
}

/* Valores em en cascada */
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

#### Unidades Rem (rem)
Relativo al tamaño de fuente del elemento raíz (generalmente html).

```css
/* Unidades rem - más predecibles que em */
html {
    font-size: 16px;      /* Tamaño base */
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

#### Unidades de Viewport
Relativo al tamaño del viewport del navegador.

```css
/* Unidades de viewport */
header {
    width: 100vw;         /* 100% del ancho del viewport */
    height: 10vh;         /* 10% de la altura del viewport */
}

h1 {
    font-size: 5vw;       /* 5% del ancho del viewport */
}

section {
    min-height: 100vh;    /* Altura mínima del viewport completo */
    padding: 5vw;         /* Padding responsivo */
}

/* vmin y vmax */
article {
    width: 80vmin;        /* 80% de la dimensión menor del viewport */
    font-size: 2vmax;     /* 2% de la dimensión mayor del viewport */
}
```

### Eligiendo la Unidad Correcta

```css
/* Mejores prácticas para diferentes casos de uso */

/* Tamaños fijos - usar px */
img {
    border: 2px solid black;
}

/* Tipografía - usar rem para consistencia */
body {
    font-size: 1rem;
}

h1 {
    font-size: 2.5rem;
}

/* Diseños - usar % o unidades de viewport */
main {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}

/* Espaciado - usar em o rem */
p {
    margin-bottom: 1em;
    padding: 1rem;
}
```

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

---

## Fuentes CSS

La tipografía es crucial para el diseño web. CSS proporciona control extenso sobre la apariencia del texto.

### Familia de Fuente

Especifica qué fuente usar. Siempre proporcione fuentes alternativas.

```css
/* Familia de fuente con alternativas */
body {
    font-family: Arial, Helvetica, sans-serif;
}

h1 {
    font-family: Georgia, 'Times New Roman', serif;
}

p {
    font-family: 'Courier New', Courier, monospace;
}

/* Usando comillas para nombres de fuente con espacios */
article {
    font-family: 'Segoe UI', Tahoma, sans-serif;
}
```

#### Familias de Fuentes Genéricas
Siempre termine con una familia genérica como alternativa final:
- **serif**: Times New Roman, Georgia (trazos decorativos)
- **sans-serif**: Arial, Helvetica (sin trazos decorativos)
- **monospace**: Courier New, Consolas (ancho de carácter igual)
- **cursive**: Comic Sans MS (estilo manuscrito)
- **fantasy**: Impact (decorativo)

### Tamaño de Fuente

Controla el tamaño del texto usando cualquier unidad CSS.

```css
/* Diferentes unidades de tamaño de fuente */
p {
    font-size: 16px;      /* Tamaño absoluto */
}

h1 {
    font-size: 2.5rem;    /* Relativo a la raíz */
}

h2 {
    font-size: 2em;       /* Relativo al padre */
}

/* Tamaños por palabras clave */
small {
    font-size: small;     /* Tamaño predefinido */
}

h3 {
    font-size: larger;    /* Palabra clave relativa */
}
```

### Peso de Fuente

Controla el grosor de los caracteres.

```css
/* Valores de peso de fuente */
p {
    font-weight: normal;  /* Igual que 400 */
}

strong {
    font-weight: bold;    /* Igual que 700 */
}

h1 {
    font-weight: 900;     /* Extra negrita */
}

h2 {
    font-weight: 300;     /* Ligero */
}

/* Valores numéricos: 100-900 */
h3 {
    font-weight: 600;     /* Semi-negrita */
}
```

### Estilo de Fuente

Controla el texto cursivo u oblicuo.

```css
/* Opciones de estilo de fuente */
p {
    font-style: normal;
}

em {
    font-style: italic;
}

footer {
    font-style: oblique;  /* Texto inclinado */
}
```

### Decoración de Texto

Añade líneas al texto.

```css
/* Decoración de texto */
a {
    text-decoration: underline;
}

h1 {
    text-decoration: none;
}

/* Decoraciones múltiples */
h2 {
    text-decoration: underline overline;
}

/* Estilos de decoración */
p {
    text-decoration: underline wavy red;
}
```

### Transformación de Texto

Cambia la capitalización del texto.

```css
/* Transformación de texto */
h1 {
    text-transform: uppercase;   /* TODO EN MAYÚSCULAS */
}

h2 {
    text-transform: lowercase;   /* todo en minúsculas */
}

h3 {
    text-transform: capitalize;  /* Primera Letra De Cada Palabra */
}

p {
    text-transform: none;        /* Texto normal */
}
```

### Altura de Línea

Controla el espaciado entre líneas de texto.

```css
/* Altura de línea */
p {
    line-height: 1.5;     /* 1.5 veces el tamaño de fuente */
}

body {
    line-height: 1.6;     /* Bueno para legibilidad */
}

h1 {
    line-height: 1.2;     /* Más ajustado para títulos */
}

/* Usando unidades */
article {
    line-height: 24px;    /* Altura fija */
}
```

### Espaciado de Letras y Palabras

Controla el espacio entre letras y palabras.

```css
/* Espaciado de letras */
h1 {
    letter-spacing: 2px;
}

p {
    letter-spacing: 0.5px;
}

/* Espaciado de palabras */
p {
    word-spacing: 5px;
}

h2 {
    word-spacing: -2px;  /* Negativo acerca las palabras */
}
```

### Alineación de Texto

Controla la alineación horizontal del texto.

```css
/* Alineación de texto */
h1 {
    text-align: center;
}

p {
    text-align: left;     /* Por defecto para idiomas LTR */
}

footer {
    text-align: right;
}

article {
    text-align: justify;  /* Estira las líneas al ancho completo */
}
```

### Ejemplo Completo de Fuente

```css
/* Estilo de fuente completo */
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
    font-family: inherit;  /* Hereda del padre */
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

/* Efecto hover para enlaces */
a:hover {
    text-decoration: underline;
    color: #2980b9;
}
```

### Fuentes Web

Aunque no se usan servicios externos, puede usar fuentes del sistema creativamente:

```css
/* Pilas de fuentes del sistema para diferentes sistemas operativos */
body {
    /* Fuentes del sistema modernas */
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 
                 Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 
                 'Helvetica Neue', sans-serif;
}

/* Fuentes monoespaciadas del sistema */
pre {
    font-family: 'SF Mono', Monaco, 'Cascadia Code', 
                 'Roboto Mono', Consolas, 'Courier New', 
                 monospace;
}
```

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

---

## Vocabulario

### Términos de Color
- **RGB**: Modelo de color Rojo, Verde, Azul usando valores 0-255
- **RGBA**: RGB con canal Alfa (transparencia)
- **HSL**: Modelo de color Matiz, Saturación, Luminosidad
- **HSLA**: HSL con canal Alfa
- **Hexadecimal**: Sistema numérico base 16 usando 0-9 y A-F
- **Canal Alfa**: Controla la transparencia (0 = transparente, 1 = opaco)
- **Matiz**: El color mismo en una rueda de color de 360 grados
- **Saturación**: Intensidad del color (0% = gris, 100% = vivo)
- **Luminosidad**: Qué tan claro u oscuro es el color

### Términos de Unidad
- **Unidades Absolutas**: Medidas fijas (px, in, cm, mm, pt, pc)
- **Unidades Relativas**: Medidas relativas a algo más (%, em, rem, vw, vh)
- **Píxel (px)**: Punto único en una pantalla
- **Em (em)**: Relativo al tamaño de fuente del elemento
- **Rem (rem)**: Relativo al tamaño de fuente del elemento raíz
- **Viewport**: El área visible de una página web
- **Ancho del Viewport (vw)**: 1% del ancho del viewport
- **Altura del Viewport (vh)**: 1% de la altura del viewport

### Términos de Fuente
- **Familia de Fuente**: La tipografía a usar
- **Peso de Fuente**: Grosor de los caracteres (100-900)
- **Estilo de Fuente**: Normal, cursivo u oblicuo
- **Altura de Línea**: Espacio entre líneas de texto
- **Espaciado de Letras**: Espacio entre caracteres
- **Espaciado de Palabras**: Espacio entre palabras
- **Transformación de Texto**: Control de capitalización
- **Decoración de Texto**: Líneas añadidas al texto (subrayado, sobrelineado, tachado)
- **Serif**: Fuentes con trazos decorativos
- **Sans-serif**: Fuentes sin trazos decorativos
- **Monospace**: Fuentes donde todos los caracteres tienen ancho igual
- **Fuentes Alternativas**: Fuentes alternativas si la primera opción no está disponible

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

---

## Tareas

### Tarea 1: Creador de Paleta de Colores
Cree una página web que demuestre todos los formatos de color construyendo una muestra de paleta de colores.
[Ver Tarea 1](assignment1.md)

### Tarea 2: Tipografía Responsiva
Construya una página de muestra tipográfica usando varias propiedades de fuente y unidades.
[Ver Tarea 2](assignment2.md)

### Tarea 3: Guía de Estilo Completa
Cree una guía de estilo completa combinando colores, unidades y fuentes.
[Ver Tarea 3](assignment3.md)

### Soluciones
- [Solución Tarea 1](assignment1-solution.md)
- [Solución Tarea 2](assignment2-solution.md)
- [Solución Tarea 3](assignment3-solution.md)

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

---

## Resumen

### Puntos Clave para Recordar

1. **Colores CSS**
   - Múltiples formatos disponibles: nombrados, hex, RGB, RGBA, HSL, HSLA
   - Use RGBA/HSLA para efectos de transparencia
   - HSL es intuitivo para crear variaciones de color
   - Siempre considere el contraste para accesibilidad

2. **Unidades CSS**
   - Unidades absolutas (px) para tamaños fijos
   - Unidades relativas (%, em, rem) para diseños flexibles
   - Unidades de viewport (vw, vh) para diseños responsivos
   - Elija unidades basándose en el contexto y necesidades

3. **Fuentes CSS**
   - Siempre proporcione fuentes alternativas
   - Use rem para tamaño consistente
   - Combine propiedades para control tipográfico completo
   - Considere la legibilidad con altura de línea apropiada

### Mejores Prácticas
- Use nombres de colores semánticos en su CSS para mantenibilidad
- Prefiera rem sobre em para un tamaño más predecible
- Siempre incluya familias de fuentes genéricas como alternativas
- Pruebe sus diseños en diferentes tamaños de pantalla
- Mantenga buenos ratios de contraste para accesibilidad

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)

---

## Recursos

### Documentación
- [MDN Colores CSS](https://developer.mozilla.org/es/docs/Web/CSS/color)
- [MDN Unidades CSS](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Values_and_units)
- [MDN Fuentes CSS](https://developer.mozilla.org/es/docs/Web/CSS/font)

### Referencias W3Schools
- [W3Schools Colores CSS](https://www.w3schools.com/css/css_colors.asp)
- [W3Schools Unidades CSS](https://www.w3schools.com/css/css_units.asp)
- [W3Schools Fuentes CSS](https://www.w3schools.com/css/css_font.asp)

### Herramientas
- IDE WebStorm para edición de código
- Git para control de versiones
- GitHub para repositorio de código

### Herramientas de Color
- Selector de colores de DevTools del navegador
- Utilidades de selector de colores del sistema

[Volver arriba](#colores-unidades-y-fuentes-css---notas-de-clase)