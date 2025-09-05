# Propiedades de Visualización CSS y el Modelo de Caja CSS

## Tabla de Contenidos

| Tema | Descripción |
|-------|-------------|
| [Introducción](#introducción) | Visión general de las propiedades de visualización y el modelo de caja |
| [Vocabulario](#vocabulario) | Términos clave y definiciones |
| [Propiedades de Visualización CSS](#propiedades-de-visualización-css) | Entendiendo block, inline, inline-block y none |
| [El Modelo de Caja CSS](#el-modelo-de-caja-css) | Margin, padding, border y content |
| [Ejemplos Visuales](#ejemplos-visuales) | Demostraciones interactivas |
| [Resumen](#resumen) | Puntos clave |
| [Recursos](#recursos) | Materiales de aprendizaje adicionales |

---

## Introducción

¡Bienvenidos a nuestra lección sobre Propiedades de Visualización CSS y el Modelo de Caja CSS! Estos son conceptos fundamentales que controlan cómo aparecen los elementos y ocupan espacio en una página web. Al final de esta lección, entenderás cómo controlar el diseño y espaciado de elementos como un desarrollador web profesional.

### Lo que Aprenderás
- Cómo diferentes propiedades de visualización afectan el comportamiento de los elementos
- Los componentes del Modelo de Caja CSS
- Cómo controlar el espaciado dentro y fuera de los elementos
- Técnicas prácticas para crear diseños

[↑ Volver al Inicio](#tabla-de-contenidos)

---

## Vocabulario

### Términos de Propiedades de Visualización
- **Propiedad Display**: Propiedad CSS que determina cómo se muestra un elemento en el flujo del documento
- **Elemento de Bloque**: Un elemento que comienza en una nueva línea y ocupa todo el ancho disponible
- **Elemento en Línea**: Un elemento que fluye dentro del texto y solo ocupa el ancho necesario
- **Elemento Inline-Block**: Combina características de elementos inline y block
- **Flujo del Documento**: El orden en que aparecen los elementos en el HTML y cómo se apilan en la página

### Términos del Modelo de Caja
- **Contenido**: El contenido real del elemento (texto, imágenes, etc.)
- **Padding**: Espacio entre el contenido y el borde
- **Border**: Una línea que rodea el padding y el contenido
- **Margin**: Espacio fuera del borde que separa el elemento de otros elementos
- **Outline**: Una línea dibujada fuera del borde que no afecta el diseño
- **Box-Sizing**: Propiedad que determina cómo se calculan el ancho y alto

[↑ Volver al Inicio](#tabla-de-contenidos)

---

## Propiedades de Visualización CSS

### Entendiendo los Tipos de Visualización

La propiedad `display` es una de las propiedades CSS más importantes para controlar el diseño. Determina cómo se comporta un elemento en el flujo del documento.

### 1. Elementos de Bloque (`display: block`)

Los elementos de bloque son como párrafos en un libro - comienzan en una nueva línea y se extienden por todo el ancho disponible.

**Características:**
- Comienzan en una nueva línea
- Ocupan todo el ancho disponible
- Pueden tener ancho y alto establecidos
- Respetan todos los valores de margin y padding

**Elementos Block por Defecto:**
- `<div>`, `<p>`, `<h1>` hasta `<h6>`
- `<header>`, `<footer>`, `<main>`, `<section>`, `<article>`
- `<ul>`, `<ol>`, `<li>`

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Elementos de Bloque</title>
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
    <div class="block-example">Soy un elemento de bloque</div>
    <div class="block-example">Comienzo en una nueva línea</div>
    <p class="block-example">Los párrafos son bloques por defecto</p>
</body>
</html>
```

### 2. Elementos en Línea (`display: inline`)

Los elementos en línea son como palabras en una oración - fluyen junto con el texto y solo ocupan el espacio necesario.

**Características:**
- No comienzan en una nueva línea
- Solo ocupan el ancho necesario
- No pueden tener ancho y alto establecidos
- El margin y padding vertical no afectan los elementos circundantes
- El margin y padding horizontal funcionan normalmente

**Elementos Inline por Defecto:**
- `<span>`, `<a>`, `<strong>`, `<em>`
- `<img>` (caso especial - acepta ancho/alto)

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Elementos en Línea</title>
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
        Este es un párrafo con 
        <span class="inline-example">elementos</span> 
        en línea que 
        <span class="inline-example">fluyen</span> 
        con el texto.
    </p>
</body>
</html>
```

### 3. Elementos Inline-Block (`display: inline-block`)

Los elementos inline-block combinan lo mejor de ambos mundos - fluyen como elementos inline pero aceptan dimensiones como elementos block.

**Características:**
- Fluyen con el texto como elementos inline
- Aceptan ancho y alto como elementos block
- Respetan todos los valores de margin y padding
- No fuerzan un salto de línea

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo Inline-Block</title>
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
    <div class="inline-block-example">Caja 1</div>
    <div class="inline-block-example">Caja 2</div>
    <div class="inline-block-example">Caja 3</div>
</body>
</html>
```

### 4. None (`display: none`)

Los elementos con `display: none` se eliminan completamente del flujo del documento.

**Características:**
- El elemento no es visible
- No ocupa espacio en la página
- Diferente de `visibility: hidden` (que oculta pero preserva el espacio)

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo Display None</title>
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
    <div class="visible">Soy visible</div>
    <div class="hidden">Estoy completamente oculto y no ocupo espacio</div>
    <div class="visible">Aparezco justo después del primer div</div>
</body>
</html>
```

[↑ Volver al Inicio](#tabla-de-contenidos)

---

## El Modelo de Caja CSS

Cada elemento HTML es esencialmente una caja rectangular. El Modelo de Caja CSS describe cómo están estructuradas estas cajas y cómo se calculan sus dimensiones.

### Componentes del Modelo de Caja (de adentro hacia afuera)

1. **Contenido**: El contenido real del elemento
2. **Padding**: Espacio entre el contenido y el borde
3. **Border**: El borde de la caja del elemento
4. **Margin**: Espacio fuera del borde

### Representación Visual

```
+------------------------------------------+
|              MARGIN (transparente)       |
|  +------------------------------------+  |
|  |          BORDER                    |  |
|  |  +------------------------------+  |  |
|  |  |        PADDING               |  |  |
|  |  |  +------------------------+  |  |  |
|  |  |  |                        |  |  |  |
|  |  |  |       CONTENIDO        |  |  |  |
|  |  |  |                        |  |  |  |
|  |  |  +------------------------+  |  |  |
|  |  |                              |  |  |
|  |  +------------------------------+  |  |
|  |                                    |  |
|  +------------------------------------+  |
|                                          |
+------------------------------------------+
```

### 1. Área de Contenido

El área de contenido contiene el contenido real - texto, imágenes u otros elementos.

**Propiedades:**
- `width`: Establece el ancho del área de contenido
- `height`: Establece el alto del área de contenido

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Área de Contenido</title>
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
        Esta es el área de contenido. Ancho: 200px, Alto: 100px
    </div>
</body>
</html>
```

### 2. Padding

El padding crea espacio entre el contenido y el borde. Es transparente y muestra el color de fondo del elemento.

**Propiedades:**
- `padding-top`, `padding-right`, `padding-bottom`, `padding-left`
- Abreviado: `padding: 10px;` (todos los lados)
- Abreviado: `padding: 10px 20px;` (arriba/abajo, izquierda/derecha)
- Abreviado: `padding: 10px 20px 30px 40px;` (arriba, derecha, abajo, izquierda - sentido horario)

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Padding</title>
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
        Padding uniforme de 20px en todos los lados
    </div>
    <div class="padding-varied">
        Padding diferente en cada lado
    </div>
</body>
</html>
```

### 3. Border

El borde rodea el padding y el contenido. Puede tener diferentes estilos, anchos y colores.

**Propiedades:**
- `border-width`: Grosor del borde
- `border-style`: solid, dashed, dotted, double, etc.
- `border-color`: Color del borde
- Abreviado: `border: 2px solid black;`

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Border</title>
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
    <div class="border-solid">Borde sólido</div>
    <div class="border-dashed">Borde punteado</div>
    <div class="border-mixed">Estilos de borde mixtos</div>
</body>
</html>
```

### 4. Margin

El margin crea espacio fuera del borde, separando el elemento de otros elementos.

**Propiedades:**
- `margin-top`, `margin-right`, `margin-bottom`, `margin-left`
- El abreviado funciona como padding
- Valor especial: `margin: 0 auto;` (centra elementos block horizontalmente)
- Los margins pueden ser negativos (acerca los elementos)

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Margin</title>
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
    <div class="margin-demo">Margin de 20px en todos los lados</div>
    <div class="centered">Centrado con margin: 20px auto</div>
    <div class="margin-collapse-1">Margin inferior: 30px</div>
    <div class="margin-collapse-2">Margin superior: 20px (colapsado a 30px de espacio total)</div>
</body>
</html>
```

### 5. Outline (Caso Especial)

El outline se dibuja fuera del borde pero no afecta el diseño ni ocupa espacio.

**Propiedades:**
- `outline-width`: Grosor
- `outline-style`: Estilo (como border-style)
- `outline-color`: Color
- `outline-offset`: Espacio entre borde y outline
- Abreviado: `outline: 2px solid red;`

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Outline</title>
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
        Esto tiene tanto un borde (azul) como un outline (rojo punteado)
    </div>
</body>
</html>
```

### Propiedad Box-Sizing

Por defecto, el ancho y alto solo establecen el tamaño del área de contenido. La propiedad `box-sizing` puede cambiar este comportamiento.

**Valores:**
- `content-box` (por defecto): Ancho/alto se aplica solo al contenido
- `border-box`: Ancho/alto incluye padding y border

**Ejemplo de Código:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Ejemplo de Box-Sizing</title>
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
        content-box: Ancho total = 200 + 40 + 10 = 250px
    </div>
    <div class="border-box">
        border-box: Ancho total = 200px
    </div>
</body>
</html>
```

[↑ Volver al Inicio](#tabla-de-contenidos)

---

## Colapso de Márgenes: Un Apéndice Importante

### ¿Qué es el Colapso de Márgenes?

El colapso de márgenes es un comportamiento CSS donde los márgenes verticales de elementos block-level adyacentes se combinan (o "colapsan") en un solo margen. Esto solo ocurre con **márgenes verticales** (arriba y abajo), nunca con márgenes horizontales (izquierda y derecha).

### ¿Cuándo Ocurre el Colapso de Márgenes?

El colapso de márgenes ocurre en tres situaciones principales:

#### 1. Hermanos Adyacentes
Cuando dos elementos block están apilados verticalmente, sus márgenes que se tocan colapsan.

**Ejemplo:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Colapso de Márgenes entre Hermanos Adyacentes</title>
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
        
        /* Resultado: Solo 30px de espacio entre cajas, ¡no 50px! */
    </style>
</head>
<body>
    <div class="box1">Caja 1 tiene margin-bottom: 30px</div>
    <div class="box2">Caja 2 tiene margin-top: 20px</div>
    <p>¡El espacio entre cajas es 30px (el margen mayor), no 50px!</p>
</body>
</html>
```

#### 2. Padre e Hijo Primero/Último
Si un padre no tiene padding o border, sus márgenes pueden colapsar con los márgenes de su primer o último hijo.

**Ejemplo:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Colapso de Márgenes Padre-Hijo</title>
    <style>
        .parent {
            background-color: #ffeb3b;
            margin-top: 40px;
            /* Sin padding o border en la parte superior */
        }
        
        .child {
            background-color: #ff9800;
            padding: 20px;
            margin-top: 30px;
        }
        
        /* La parte superior del padre aparece a 40px del elemento anterior,
           no 70px (40px + 30px) */
    </style>
</head>
<body>
    <div style="background: #ccc; padding: 10px;">Elemento Anterior</div>
    <div class="parent">
        <div class="child">
            Hijo con margin-top: 30px dentro del padre con margin-top: 40px
        </div>
    </div>
</body>
</html>
```

#### 3. Bloques Vacíos
Si un elemento block no tiene contenido, padding, border o height, sus márgenes superior e inferior colapsan.

**Ejemplo:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Colapso de Márgenes en Bloque Vacío</title>
    <style>
        .before {
            background-color: lightcoral;
            padding: 20px;
            margin-bottom: 30px;
        }
        
        .empty {
            margin-top: 20px;
            margin-bottom: 40px;
            /* Sin contenido, padding o border */
        }
        
        .after {
            background-color: lightseagreen;
            padding: 20px;
            margin-top: 25px;
        }
        
        /* El espacio será 40px (el mayor de todos los márgenes) */
    </style>
</head>
<body>
    <div class="before">Elemento anterior</div>
    <div class="empty"></div>
    <div class="after">Elemento posterior</div>
</body>
</html>
```

### Reglas del Colapso de Márgenes

1. **Solo los Márgenes Verticales Colapsan**
   - Los márgenes superior e inferior pueden colapsar
   - Los márgenes izquierdo y derecho NUNCA colapsan

2. **Gana el Margen Más Grande**
   - Cuando los márgenes colapsan, se usa el valor de margen mayor
   - El margen menor se ignora

3. **Márgenes Negativos**
   - Si un margen es negativo, se resta del margen positivo
   - Si ambos son negativos, se usa el valor más negativo

### Cuándo los Márgenes NO Colapsan

Los márgenes NO colapsarán cuando:

1. **Los elementos están flotados** - Los elementos flotados nunca colapsan márgenes
2. **Elementos inline-block** - Solo los elementos block colapsan márgenes
3. **Elementos posicionados absolutamente** - Position: absolute/fixed previene el colapso
4. **Overflow está establecido** - Elementos con overflow diferente a visible no colapsan
5. **Padding o border los separa** - Cualquier padding/border previene el colapso
6. **Los elementos están en diferentes contextos de formato** - Como contenedores flexbox o grid

### Previniendo el Colapso de Márgenes

Aquí hay técnicas comunes para prevenir el colapso de márgenes no deseado:

**Método 1: Agregar Padding o Border**
```css
.parent {
    padding-top: 1px; /* Previene colapso con primer hijo */
    padding-bottom: 1px; /* Previene colapso con último hijo */
}
/* O */
.parent {
    border-top: 1px solid transparent;
    border-bottom: 1px solid transparent;
}
```

**Método 2: Usar Overflow**
```css
.parent {
    overflow: auto; /* o hidden, scroll */
}
```

**Método 3: Usar Propiedades Display**
```css
.element {
    display: inline-block; /* Previene colapso de márgenes */
}
```

**Método 4: Usar Pseudo-elementos**
```css
.parent::before,
.parent::after {
    content: "";
    display: table;
}
```

### Ejemplo Práctico: Diseño de Tarjetas con Colapso de Márgenes

```html
<!DOCTYPE html>
<html>
<head>
    <title>Colapso de Márgenes en la Práctica</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
            background: #f0f0f0;
        }
        
        .container {
            background: white;
            border-radius: 8px;
            /* Sin padding - los márgenes pueden colapsar */
        }
        
        .container-fixed {
            background: white;
            border-radius: 8px;
            padding: 1px 20px; /* El padding previene el colapso */
            margin-top: 30px;
        }
        
        .card {
            background: #e3f2fd;
            padding: 20px;
            margin: 30px 20px; /* Los márgenes verticales pueden colapsar */
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
    <h1>Demostración del Colapso de Márgenes</h1>
    
    <div class="demo-info">
        <strong>Problema:</strong> Sin padding, el margen superior de la primera tarjeta colapsa con el contenedor
    </div>
    
    <div class="container">
        <div class="card">
            Primera tarjeta - ¡mi margen superior (30px) escapa del contenedor!
        </div>
        <div class="card">
            Segunda tarjeta - los márgenes entre tarjetas colapsan a 30px, no 60px
        </div>
        <div class="card">
            Tercera tarjeta - ¡mi margen inferior (30px) también escapa!
        </div>
    </div>
    
    <div class="demo-info">
        <strong>Solución:</strong> Agregar 1px de padding previene el colapso de márgenes
    </div>
    
    <div class="container-fixed">
        <div class="card">
            Primera tarjeta - ahora contenida apropiadamente dentro del padre
        </div>
        <div class="card">
            Segunda tarjeta - los márgenes aún colapsan entre tarjetas (esto a menudo es deseado)
        </div>
        <div class="card">
            Tercera tarjeta - margen inferior también contenido
        </div>
    </div>
</body>
</html>
```

### ¿Por Qué Existe el Colapso de Márgenes?

El colapso de márgenes puede parecer confuso, pero existe por buenas razones:

1. **Tipografía**: En documentos de texto, quieres espaciado consistente entre párrafos independientemente de la configuración individual de márgenes
2. **Flexibilidad**: Permite a los elementos definir su espaciado deseado sin duplicarse
3. **Histórico**: Este comportamiento viene de la tipografía tradicional de impresión

### Mejores Prácticas

1. **Estar Consciente**: Siempre recuerda que los márgenes verticales pueden colapsar
2. **Usar Padding**: Cuando necesites espacio garantizado, usa padding en su lugar
3. **Dirección Única**: Considera usar solo `margin-bottom` O `margin-top`, no ambos
4. **Probar Tus Diseños**: Verifica el espaciado entre elementos durante el desarrollo
5. **Documentar Intención**: Comenta cuando dependas de o prevengas el colapso

### Problemas Comunes

1. **Primer elemento en un contenedor** empujando hacia abajo el contenedor mismo
2. **Espacios inesperados** que son menores de lo esperado
3. **Márgenes "escapando"** de sus contenedores
4. **Elementos vacíos** no creando el espacio esperado

Entender el colapso de márgenes te ayuda a:
- Depurar problemas de espaciado inesperados
- Crear diseños más predecibles
- Escribir CSS más limpio y mantenible
- Evitar problemas frustrantes de diseño

[↑ Volver al Inicio](#tabla-de-contenidos)

---

## Ejemplos Visuales

### Demostración Completa del Modelo de Caja

```html
<!DOCTYPE html>
<html>
<head>
    <title>Demo Completa del Modelo de Caja</title>
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
        <span class="label content-label">CONTENIDO: 300x150px</span>
    </div>
</body>
</html>
```

### Comparación de Propiedades Display

```html
<!DOCTYPE html>
<html>
<head>
    <title>Comparación de Propiedades Display</title>
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
        <h3>Elementos de Bloque</h3>
        <div class="block-item">Bloque 1</div>
        <div class="block-item">Bloque 2</div>
        <div class="block-item">Bloque 3</div>
    </div>
    
    <div class="container">
        <h3>Elementos en Línea</h3>
        <span class="inline-item">Línea 1</span>
        <span class="inline-item">Línea 2</span>
        <span class="inline-item">Línea 3</span>
    </div>
    
    <div class="container">
        <h3>Elementos Inline-Block</h3>
        <div class="inline-block-item">IB 1</div>
        <div class="inline-block-item">IB 2</div>
        <div class="inline-block-item">IB 3</div>
    </div>
</body>
</html>
```

[↑ Volver al Inicio](#tabla-de-contenidos)

---

## Resumen

### Puntos Clave

1. **Las Propiedades Display Controlan el Flujo del Diseño**
   - Los elementos block se apilan verticalmente y ocupan todo el ancho
   - Los elementos inline fluyen horizontalmente y se ajustan con el texto
   - Inline-block combina beneficios de ambos
   - Display: none elimina elementos completamente

2. **El Modelo de Caja Tiene Cuatro Partes Principales**
   - Contenido: El contenido real del elemento
   - Padding: Espacio dentro del borde
   - Border: El borde del elemento
   - Margin: Espacio fuera del borde

3. **Box-Sizing Cambia los Cálculos**
   - content-box: Ancho/alto se aplica solo al contenido
   - border-box: Ancho/alto incluye padding y border

4. **Los Márgenes Pueden Colapsar**
   - Los márgenes verticales entre elementos colapsan al valor mayor
   - Los márgenes horizontales nunca colapsan

5. **Los Outlines No Afectan el Diseño**
   - Útiles para resaltar sin mover otros elementos

### Casos de Uso Comunes

- **Menús de Navegación**: Usar inline o inline-block para menús horizontales
- **Diseños de Tarjetas**: Combinar padding para espaciado interno y margin para separación
- **Centrado**: Usar `margin: 0 auto` para centrado horizontal de elementos block
- **Diseño Responsivo**: Box-sizing: border-box hace los cálculos de ancho predecibles

[↑ Volver al Inicio](#tabla-de-contenidos)

---

## Recursos

### Documentación
- [MDN Web Docs - CSS Display](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
- [MDN Web Docs - CSS Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
- [W3Schools - CSS Display Property](https://www.w3schools.com/css/css_display_visibility.asp)
- [W3Schools - CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp)

### Herramientas de Práctica
- [Visualizador del Modelo de Caja CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_box_model_and_inline_boxes)
- Usar las DevTools del navegador (F12) para inspeccionar y modificar propiedades del modelo de caja

### Próximos Pasos
Después de dominar estos conceptos, estarás listo para aprender sobre:
- Posicionamiento CSS (static, relative, absolute, fixed)
- Diseño Flexbox
- CSS Grid
- Técnicas de diseño responsivo

[↑ Volver al Inicio](#tabla-de-contenidos)