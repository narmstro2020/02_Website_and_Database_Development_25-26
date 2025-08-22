# Introducción a CSS - Notas de Clase

## Tabla de Contenidos

| Tema | Descripción |
|-------|-------------|
| [1. ¿Qué es CSS?](#1-qué-es-css) | Entendiendo CSS y su rol en el desarrollo web |
| [2. Breve Historia de CSS](#2-breve-historia-de-css) | Evolución y versiones de CSS |
| [3. Formato del Selector CSS](#3-formato-del-selector-css) | Sintaxis y estructura básica |
| [4. CSS en Línea](#4-css-en-línea) | Estilización directa en elementos HTML |
| [5. CSS Interno](#5-css-interno) | Estilización dentro del documento HTML |
| [6. CSS Externo](#6-css-externo) | Vinculación de archivos CSS separados |
| [Vocabulario](#vocabulario) | Términos y definiciones clave |
| [Resumen](#resumen) | Puntos clave |
| [Recursos](#recursos) | Materiales de aprendizaje adicionales |

---

## 1. ¿Qué es CSS?

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Definición
**CSS** significa **Hojas de Estilo en Cascada** (Cascading Style Sheets). Es un lenguaje de estilización usado para describir cómo deben mostrarse los elementos HTML en una página web.

### Propósito
Piensa en HTML como el esqueleto de una página web - proporciona estructura. ¡CSS es como la ropa y el maquillaje - hace que todo se vea bien!

### La Relación Entre HTML y CSS

```
HTML = Estructura (Qué contenido aparece)
CSS = Presentación (Cómo se ve el contenido)
```

### Analogía Visual
Imagina construir una casa:
- **HTML** = El marco, paredes y habitaciones (estructura)
- **CSS** = La pintura, decoraciones y muebles (estilo)

### ¿Por Qué Usar CSS?
1. **Separación de Responsabilidades**: Mantener la estructura (HTML) separada de la presentación (CSS)
2. **Reutilización**: Una regla CSS puede estilizar múltiples elementos HTML
3. **Consistencia**: Mantener estilización uniforme en todo tu sitio web
4. **Eficiencia**: Cambiar el aspecto de cientos de páginas editando un archivo CSS

---

## 2. Breve Historia de CSS

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Línea de Tiempo

| Año | Versión | Características Clave |
|------|---------|--------------|
| 1996 | CSS1 | Estilización básica: fuentes, colores, espaciado |
| 1998 | CSS2 | Posicionamiento, tipos de medios |
| 2011 | CSS3 | Animaciones, gradientes, sombras, diseño responsivo |
| Presente | CSS3+ | Actualizaciones modulares continuas |

### Antes de CSS
En los primeros días de la web, toda la estilización se hacía directamente en HTML usando atributos como:
```html
<font color="red">Este es texto rojo</font>
```
¡Esto hacía que los sitios web fueran difíciles de mantener y actualizar!

### Por Qué Se Creó CSS
- Para resolver el problema de mezclar contenido con presentación
- Para dar a los diseñadores web más control sobre el diseño
- Para reducir el código repetitivo

---

## 3. Formato del Selector CSS

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Sintaxis Básica de CSS

Cada regla CSS consiste en dos partes principales:

```css
selector {
    propiedad: valor;
}
```

### Componentes Explicados

1. **Selector**: Qué elemento(s) HTML estilizar
2. **Propiedad**: Qué aspecto cambiar (color, tamaño, etc.)
3. **Valor**: A qué cambiarlo
4. **Declaración**: Un par propiedad-valor
5. **Bloque de Declaración**: Todo dentro de las llaves `{}`

### Diagrama Visual

```
    selector
       ↓
    h1 {
        color: blue;     ← declaración
        ↑       ↑
    propiedad  valor
        
        font-size: 24px; ← otra declaración
    }
    ↑                 ↑
    llave           llave
    apertura        cierre
```

### Declaraciones Múltiples
Puedes tener múltiples declaraciones en una regla:

```css
p {
    color: navy;
    font-size: 16px;
    line-height: 1.5;
}
```

### Comentarios en CSS
Usa `/* */` para agregar comentarios:

```css
/* Esto es un comentario en CSS */
h1 {
    color: green; /* Esto hace los encabezados verdes */
}
```

---

## 4. CSS en Línea

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Definición
CSS en línea es CSS escrito directamente en un elemento HTML usando el atributo `style`.

### Sintaxis
```html
<etiqueta style="propiedad: valor;">Contenido</etiqueta>
```

### Ejemplos

#### Ejemplo 1: Estilizando un Párrafo
```html
<p style="color: red;">¡Este texto es rojo!</p>
```

#### Ejemplo 2: Múltiples Propiedades
```html
<h1 style="color: blue; font-size: 36px;">Encabezado Azul Grande</h1>
```

#### Ejemplo 3: Estilizando Diferentes Elementos
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de CSS en Línea</title>
</head>
<body>
    <h1 style="color: purple;">¡Bienvenido!</h1>
    <p style="color: green; font-size: 18px;">Este es un párrafo verde.</p>
    <p style="background-color: yellow;">Este tiene un fondo amarillo.</p>
</body>
</html>
```

### Propiedades Comunes para CSS en Línea

| Propiedad | Descripción | Valores de Ejemplo |
|----------|-------------|----------------|
| `color` | Color del texto | `red`, `#FF0000`, `rgb(255,0,0)` |
| `background-color` | Color de fondo | `yellow`, `#FFFF00` |
| `font-size` | Tamaño del texto | `16px`, `1.5em`, `large` |
| `text-align` | Alineación del texto | `left`, `center`, `right` |
| `font-family` | Tipo de fuente | `Arial`, `"Times New Roman"` |

### Ventajas y Desventajas

**Ventajas:**
- Rápido para pruebas
- Sobrescribe otro CSS (especificidad más alta)
- No necesita archivos externos

**Desventajas:**
- No reutilizable
- Mezcla presentación con contenido
- Difícil de mantener
- Hace el HTML desordenado

---

## 5. CSS Interno

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Definición
CSS interno (también llamado CSS embebido) se escribe en la sección `<head>` de un documento HTML usando la etiqueta `<style>`.

### Sintaxis
```html
<head>
    <style>
        selector {
            propiedad: valor;
        }
    </style>
</head>
```

### Ejemplo Completo
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de CSS Interno</title>
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
    <h1>Bienvenido a Mi Sitio Web</h1>
    <p>Este es un párrafo con texto <strong>importante</strong>.</p>
    <p>¡Todos los párrafos tendrán el mismo estilo!</p>
</body>
</html>
```

### Selectores de Elementos
Selecciona elementos HTML por su nombre de etiqueta:

```css
h1 { color: blue; }
p { font-size: 14px; }
em { font-style: italic; }
strong { font-weight: bold; }
```

### Estilizando Múltiples Elementos
Aplica el mismo estilo a múltiples elementos:

```css
h1, h2, h3 {
    font-family: Arial;
    color: darkblue;
}
```

### Ventajas y Desventajas

**Ventajas:**
- Los estilos se aplican a toda la página
- Mantiene los estilos separados del contenido HTML
- Puede reutilizar estilos para múltiples elementos

**Desventajas:**
- Solo funciona para una página HTML
- No reutilizable en diferentes páginas
- Aumenta el tamaño del archivo de la página

---

## 6. CSS Externo

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Definición
CSS externo se escribe en un archivo `.css` separado y se vincula a documentos HTML.

### Creando el Enlace
Usa la etiqueta `<link>` en la sección `<head>`:

```html
<link rel="stylesheet" href="styles.css">
```

### Ejemplo de Estructura de Archivos
```
mi-sitio-web/
│
├── index.html
├── about.html
├── contact.html
└── styles.css
```

### Archivo HTML (index.html)
```html
<!DOCTYPE html>
<html>
<head>
    <title>Mi Sitio Web</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenido a Mi Sitio</h1>
    </header>
    <main>
        <section>
            <h2>Sobre Nosotros</h2>
            <p>¡Creamos sitios web increíbles!</p>
        </section>
    </main>
    <footer>
        <p>© 2024 Mi Sitio Web</p>
    </footer>
</body>
</html>
```

### Archivo CSS (styles.css)
```css
/* Restablecer márgenes predeterminados */
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

/* Estilos del encabezado */
header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

h1 {
    margin: 0;
}

/* Estilos del contenido principal */
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

/* Estilos del pie de página */
footer {
    background-color: #f0f0f0;
    text-align: center;
    padding: 10px;
    color: #666;
}
```

### Vinculando CSS desde Diferentes Directorios

#### CSS en una subcarpeta:
```
mi-sitio-web/
│
├── index.html
└── css/
    └── styles.css
```

Enlace: `<link rel="stylesheet" href="css/styles.css">`

#### CSS en carpeta padre:
```
mi-sitio-web/
│
├── styles.css
└── pages/
    └── about.html
```

Enlace desde about.html: `<link rel="stylesheet" href="../styles.css">`

### Múltiples Archivos CSS
Puedes vincular múltiples archivos CSS:

```html
<link rel="stylesheet" href="css/reset.css">
<link rel="stylesheet" href="css/layout.css">
<link rel="stylesheet" href="css/colors.css">
```

### Ventajas y Desventajas

**Ventajas:**
- Separación completa de contenido y presentación
- Reutilizable en múltiples páginas HTML
- Archivos HTML más pequeños
- Puede ser almacenado en caché por navegadores (carga más rápida)
- Fácil de mantener y actualizar

**Desventajas:**
- Requiere una solicitud HTTP adicional
- Podría causar un destello de contenido sin estilo (FOUC)

---

## Vocabulario

[⬆ Volver al Inicio](#tabla-de-contenidos)

| Término | Definición |
|------|------------|
| **CSS** | Hojas de Estilo en Cascada - lenguaje para estilizar HTML |
| **Selector** | Identifica qué elementos HTML estilizar |
| **Propiedad** | El aspecto de un elemento que quieres cambiar |
| **Valor** | A qué quieres cambiar la propiedad |
| **Declaración** | Un par propiedad-valor (ej., `color: blue;`) |
| **Bloque de Declaración** | Grupo de declaraciones dentro de llaves |
| **CSS en Línea** | CSS escrito directamente en elementos HTML usando atributo `style` |
| **CSS Interno** | CSS escrito en la etiqueta `<style>` dentro del `<head>` HTML |
| **CSS Externo** | CSS escrito en archivos `.css` separados |
| **Cascada** | El orden en que se aplican las reglas CSS |
| **Hoja de Estilo** | Una colección de reglas CSS |
| **Etiqueta Link** | Elemento HTML usado para conectar archivos CSS externos |
| **Especificidad** | Reglas que determinan qué regla CSS se aplica cuando múltiples reglas apuntan al mismo elemento |

---

## Resumen

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Puntos Clave

1. **CSS hace que los sitios web sean hermosos** - Controla colores, fuentes, espaciado y diseño
2. **Tres formas de agregar CSS**:
   - **En línea**: Rápido pero no reutilizable
   - **Interno**: Bueno para páginas individuales
   - **Externo**: Mejor para sitios web de múltiples páginas
3. **La sintaxis CSS es consistente**: `selector { propiedad: valor; }`
4. **Separación de responsabilidades** - Mantener la estructura (HTML) separada del estilo (CSS)
5. **CSS externo es generalmente mejor** para sitios web reales porque es:
   - Reutilizable en páginas
   - Fácil de mantener
   - Mantiene el HTML limpio

### Prioridad CSS (Cascada)
Cuando múltiples reglas CSS se aplican al mismo elemento:
1. **CSS en línea** (prioridad más alta)
2. **CSS interno**
3. **CSS externo** (prioridad más baja)

### Mejores Prácticas
- Comienza con CSS externo para consistencia
- Usa CSS interno para estilos específicos de página
- Usa CSS en línea con moderación (solo pruebas o sobrescrituras)
- Mantén tu CSS organizado con comentarios
- Usa nombres significativos para tus archivos CSS

---

## Recursos

[⬆ Volver al Inicio](#tabla-de-contenidos)

### Documentación
- [Documentación CSS de MDN](https://developer.mozilla.org/es/docs/Web/CSS)
- [Tutorial CSS de W3Schools](https://www.w3schools.com/css/)
- [Referencia CSS](https://developer.mozilla.org/es/docs/Web/CSS/Reference)

### Referencia de Propiedades CSS
- [Propiedades CSS de W3Schools](https://www.w3schools.com/cssref/)
- [Índice de Propiedades CSS de MDN](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Properties_Reference)

### Herramientas
- **WebStorm**: Tu IDE para escribir HTML y CSS
- **Git**: Control de versiones para rastrear cambios
- **GitHub**: Aloja y comparte tu código

### Recursos de Práctica
- [Ejercicios CSS de W3Schools](https://www.w3schools.com/css/exercise.asp)
- [Fundamentos CSS en MDN](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/CSS_basics)

### Próximos Pasos
Después de dominar estos conceptos básicos, aprenderás sobre:
- Selectores de clase e ID
- El modelo de caja
- Diseños Flexbox y Grid
- Diseño responsivo
- Animaciones CSS

---

*Recuerda: ¡La mejor manera de aprender CSS es practicando! Comienza con estilos simples y gradualmente agrega más complejidad a medida que te sientas cómodo.*