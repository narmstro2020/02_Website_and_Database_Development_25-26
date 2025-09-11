# Estilizar Formularios y Tablas con CSS

## Tabla de Contenidos

| Tema | Descripción |
|------|-------------|
| [Introducción](#introducción) | Visión general del estilo de formularios y tablas |
| [Vocabulario](#vocabulario) | Términos clave y definiciones |
| [1. Estilizar Tablas con CSS](#1-estilizar-tablas-con-css) | Aprender a estilizar tablas HTML |
| [2. Estilizar Formularios con CSS](#2-estilizar-formularios-con-css) | Aprender a estilizar formularios HTML |
| [Ejemplos Visuales](#ejemplos-visuales) | Ejemplos completos funcionales |
| [Tareas](#tareas) | Ejercicios prácticos |
| [Resumen](#resumen) | Puntos clave para recordar |
| [Recursos](#recursos) | Material de aprendizaje adicional |

---

## Introducción

¡Bienvenidos a nuestra lección sobre estilizar formularios y tablas con CSS! Los formularios y tablas son componentes esenciales del desarrollo web. Las tablas nos ayudan a organizar datos en filas y columnas, mientras que los formularios permiten a los usuarios ingresar y enviar información. En esta lección, aprenderemos cómo hacer estos elementos visualmente atractivos y fáciles de usar usando CSS.

### Lo que Aprenderás:
- Cómo estilizar bordes, espaciado y fondos de tablas
- Cómo crear formularios atractivos y accesibles
- Mejores prácticas para el diseño de formularios y tablas
- Propiedades CSS específicas para formularios y tablas

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

## Vocabulario

### Términos Relacionados con Tablas
- **border-collapse**: Propiedad CSS que determina si los bordes de tabla están separados o colapsados en un solo borde
- **border-spacing**: Propiedad CSS que establece la distancia entre los bordes de celdas adyacentes
- **caption-side**: Propiedad CSS que posiciona un título de tabla
- **thead**: Elemento HTML que agrupa contenido de encabezado en una tabla
- **tbody**: Elemento HTML que agrupa contenido del cuerpo en una tabla
- **tfoot**: Elemento HTML que agrupa contenido de pie de página en una tabla
- **nth-child()**: Selector de pseudo-clase CSS que coincide con elementos basados en su posición

### Términos Relacionados con Formularios
- **fieldset**: Elemento HTML que agrupa controles de formulario relacionados
- **legend**: Elemento HTML que proporciona un título para un fieldset
- **placeholder**: Atributo HTML que proporciona texto de sugerencia en entradas de formulario
- **focus**: El estado cuando un elemento de formulario está seleccionado/activo
- **:focus**: Pseudo-clase CSS que estiliza un elemento cuando tiene foco
- **:hover**: Pseudo-clase CSS que estiliza un elemento cuando el mouse se posa sobre él
- **:disabled**: Pseudo-clase CSS que estiliza elementos de formulario deshabilitados
- **outline**: Propiedad CSS que dibuja una línea alrededor de elementos (a menudo vista en foco)

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

## 1. Estilizar Tablas con CSS

Las tablas son herramientas poderosas para mostrar datos estructurados. Aprendamos cómo hacerlas hermosas y funcionales.

### Revisión de la Estructura Básica de Tablas

```html
<table>
    <caption>Calificaciones de Estudiantes</caption>
    <thead>
        <tr>
            <th>Nombre</th>
            <th>Calificación</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Alicia</td>
            <td>A</td>
        </tr>
        <tr>
            <td>Roberto</td>
            <td>B+</td>
        </tr>
    </tbody>
</table>
```

### Propiedades Esenciales de Estilo de Tablas

#### 1. Colapso de Bordes

La propiedad `border-collapse` controla cómo se comportan los bordes de tabla:

```css
/* Bordes separados (predeterminado) */
table {
    border-collapse: separate;
    border-spacing: 2px;
}

/* Bordes colapsados (recomendado) */
table {
    border-collapse: collapse;
}
```

#### 2. Agregar Bordes

```css
table {
    border: 2px solid #333;
}

th, td {
    border: 1px solid #ddd;
    padding: 8px;
}
```

#### 3. Estilizar Encabezados de Tabla

```css
th {
    background-color: #4CAF50;
    color: white;
    font-weight: bold;
    text-align: left;
    padding: 12px;
}
```

#### 4. Colores de Filas Alternados (Rayas de Cebra)

```css
/* Filas pares */
tbody tr:nth-child(even) {
    background-color: #f2f2f2;
}

/* Filas impares */
tbody tr:nth-child(odd) {
    background-color: white;
}
```

#### 5. Efectos Hover

```css
tbody tr:hover {
    background-color: #ddd;
    cursor: pointer;
}
```

### Ejemplo Completo de Tabla

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tabla Estilizada</title>
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
        <caption>Inventario de Productos</caption>
        <thead>
            <tr>
                <th>Producto</th>
                <th>Cantidad</th>
                <th>Precio</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Laptop</td>
                <td>15</td>
                <td>$999</td>
            </tr>
            <tr>
                <td>Ratón</td>
                <td>50</td>
                <td>$25</td>
            </tr>
            <tr>
                <td>Teclado</td>
                <td>30</td>
                <td>$75</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

### Tablas Responsivas

Para mejor visualización móvil:

```css
/* Contenedor para desplazamiento horizontal en pantallas pequeñas */
.table-container {
    overflow-x: auto;
}

table {
    min-width: 600px;
}
```

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

## 2. Estilizar Formularios con CSS

Los formularios son cómo los usuarios interactúan con tu sitio web. Un buen diseño de formulario mejora la experiencia del usuario y aumenta las tasas de completación.

### Revisión de la Estructura Básica de Formularios

```html
<form>
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre">
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email">
    
    <input type="submit" value="Enviar">
</form>
```

### Técnicas Esenciales de Estilo de Formularios

#### 1. Estilo Básico de Entradas

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

#### 2. Estilo de Etiquetas

```css
label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
    color: #333;
}
```

#### 3. Estados de Foco

```css
input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus {
    outline: none;
    border-color: #4CAF50;
    box-shadow: 0 0 5px rgba(76, 175, 80, 0.3);
}
```

#### 4. Estilo de Botones

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

#### 5. Fieldset y Legend

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

### Ejemplo Completo de Formulario

```html
<!DOCTYPE html>
<html>
<head>
    <title>Formulario Estilizado</title>
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
        <h2>Formulario de Registro</h2>
        
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" placeholder="Ingresa tu nombre">
        
        <label for="apellido">Apellido:</label>
        <input type="text" id="apellido" name="apellido" placeholder="Ingresa tu apellido">
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" placeholder="tu@email.com">
        
        <label for="pais">País:</label>
        <select id="pais" name="pais">
            <option value="">Selecciona tu país</option>
            <option value="españa">España</option>
            <option value="mexico">México</option>
            <option value="argentina">Argentina</option>
        </select>
        
        <button type="submit">Registrarse</button>
    </form>
</body>
</html>
```

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

## Ejemplos Visuales

### Ejemplo 1: Tabla de Datos Profesional

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tabla Profesional</title>
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
        
        .status-activo {
            background-color: #d4edda;
            color: #155724;
        }
        
        .status-pendiente {
            background-color: #fff3cd;
            color: #856404;
        }
    </style>
</head>
<body>
    <div class="table-container">
        <table>
            <caption>Directorio de Empleados</caption>
            <thead>
                <tr>
                    <th>Nombre</th>
                    <th>Departamento</th>
                    <th>Email</th>
                    <th>Estado</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Juan Pérez</td>
                    <td>Ingeniería</td>
                    <td>juan@empresa.com</td>
                    <td><span class="status status-activo">Activo</span></td>
                </tr>
                <tr>
                    <td>María García</td>
                    <td>Marketing</td>
                    <td>maria@empresa.com</td>
                    <td><span class="status status-activo">Activo</span></td>
                </tr>
                <tr>
                    <td>Carlos López</td>
                    <td>Ventas</td>
                    <td>carlos@empresa.com</td>
                    <td><span class="status status-pendiente">Pendiente</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

## Tareas

### Tarea 1: Estilizar una Tabla de Productos
Crea y estiliza una tabla mostrando al menos 5 productos con columnas para Nombre del Producto, Categoría, Precio y Estado del Stock.

**Requisitos:**
- Usar colores de filas alternados
- Agregar efectos hover
- Estilizar el encabezado con un color de fondo distintivo
- Incluir un título de tabla
- Hacer los bordes colapsados
- Agregar espaciado apropiado

### Tarea 2: Crear un Formulario de Registro Estilizado
Construye un formulario de registro con varios tipos de entrada y estilo profesional.

**Requisitos:**
- Incluir campos de texto, email, contraseña, select y textarea
- Usar fieldsets para agrupar campos relacionados
- Agregar estados de foco a todas las entradas
- Estilizar botón de envío con efecto hover
- Incluir texto placeholder
- Hacer el formulario responsive

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

## Resumen

### Puntos Clave para Recordar

#### Tablas
- Usa `border-collapse: collapse` para diseños de tabla más limpios
- Aplica selectores `:nth-child()` para colores de filas alternados
- Siempre incluye estructura de tabla apropiada (thead, tbody, tfoot)
- Agrega efectos hover para mejorar la interacción del usuario
- Usa padding para crear espacio de respiración en las celdas

#### Formularios
- Estiliza todos los estados del formulario: predeterminado, hover, foco y deshabilitado
- Agrupa campos relacionados con fieldsets
- Usa espaciado y alineación consistentes
- Proporciona retroalimentación visual clara para las interacciones del usuario
- Siempre incluye etiquetas para accesibilidad
- Usa texto placeholder para guiar a los usuarios

### Propiedades CSS Aprendidas

**Propiedades de Tabla:**
- `border-collapse`
- `border-spacing`
- `caption-side`
- `:nth-child()`

**Propiedades de Formulario:**
- `:focus`
- `:hover`
- `:disabled`
- `:valid` / `:invalid`
- `outline`
- `box-shadow`
- `transition`

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

## Recursos

### Documentación
- [MDN - Estilizar Tablas](https://developer.mozilla.org/es/docs/Learn/CSS/Building_blocks/Styling_tables)
- [MDN - Estilizar Formularios](https://developer.mozilla.org/es/docs/Learn/Forms/Styling_web_forms)
- [W3Schools - Tablas CSS](https://www.w3schools.com/css/css_table.asp)
- [W3Schools - Formularios CSS](https://www.w3schools.com/css/css_form.asp)

### Referencias CSS
- [MDN - border-collapse](https://developer.mozilla.org/es/docs/Web/CSS/border-collapse)
- [MDN - :nth-child()](https://developer.mozilla.org/es/docs/Web/CSS/:nth-child)
- [MDN - :focus](https://developer.mozilla.org/es/docs/Web/CSS/:focus)
- [MDN - fieldset](https://developer.mozilla.org/es/docs/Web/HTML/Element/fieldset)

[↑ Volver al Índice](#estilizar-formularios-y-tablas-con-css)

---

*Fin de las Notas de Clase - Estilizar Formularios y Tablas con CSS*