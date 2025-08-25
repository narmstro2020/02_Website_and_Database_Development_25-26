# Tarea 1: Creador de Paleta de Colores

## Objetivo
Crear una página web que demuestre tu comprensión de los formatos de color CSS construyendo una muestra de paleta de colores. Crearás muestras de colores usando diferentes formatos de color y los aplicarás a varios elementos HTML.

## Requisitos

### Estructura HTML
Crea un archivo HTML con:
1. Un encabezado principal (h1) para el título de la página
2. Seis secciones, cada una conteniendo:
   - Un subtítulo (h2) para el nombre del formato de color
   - Al menos 3 elementos párrafo demostrando diferentes colores
   - Un elemento article con fondo coloreado

### Requisitos CSS
Debes demostrar TODOS los siguientes formatos de color:
1. **Sección de Colores Nombrados**: Usa al menos 5 colores nombrados diferentes
2. **Sección Hexadecimal**: Usa colores hex completos (#RRVVAA) y abreviados (#RVA)
3. **Sección RGB**: Crea colores usando valores rgb()
4. **Sección RGBA**: Muestra transparencia con al menos 3 valores alfa diferentes
5. **Sección HSL**: Crea un esquema de colores usando hsl()
6. **Sección HSLA**: Combina HSL con transparencia

### Tareas Específicas
1. Crea un efecto "arcoíris" usando al menos 7 colores diferentes en cualquier formato
2. Demuestra transparencia superponiendo elementos con RGBA o HSLA
3. Crea un esquema de color monocromático (diferentes tonos del mismo color)
4. Estiliza el color del texto Y el color de fondo para cada sección
5. Añade un pie de página con un efecto tipo gradiente usando transparencia

## Código Inicial

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Muestra de Paleta de Colores</title>
    <meta charset="UTF-8">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Muestra de Paleta de Colores CSS</h1>
    </header>
    
    <main>
        <section>
            <h2>Colores Nombrados</h2>
            <p>Este texto usa un color nombrado.</p>
            <p>Este tiene un color nombrado diferente.</p>
            <p>Esto combina colores nombrados de texto y fondo.</p>
            <article>
                Este artículo tiene un fondo de color nombrado.
            </article>
        </section>
        
        <!-- Añade más secciones para cada formato de color -->
        
    </main>
    
    <footer>
        <p>Pie de página con efectos de color creativos</p>
    </footer>
</body>
</html>
```

styles.css
```css
        body {
            /* Añade un color de fondo claro */
        }
        
        h1 {
            /* Centra y estiliza el encabezado principal */
        }
        
        section {
            /* Añade espaciado entre secciones */
        }
        
        /* Añade tus estilos de color abajo */


```

## Consejos
- Usa comentarios en tu CSS para etiquetar cada sección de formato de color
- Prueba la transparencia superponiendo elementos
- Recuerda que los valores de matiz HSL van de 0-360 grados
- Para el arcoíris, piensa en la rueda de colores
- Un esquema monocromático puede usar diferentes valores de luminosidad o saturación

## Entrega
Entrega dos archivos:
1. `paleta-colores.html` - Tu archivo HTML completo con CSS integrado
2. Una captura de pantalla de tu página web renderizada

## Desafío Adicional (Opcional)
Crea un diseño de "tarjeta de color" donde cada muestra de color parezca una tarjeta física con:
- Un efecto de sombra usando RGBA
- El valor del color mostrado como texto en la tarjeta
- Esquinas redondeadas usando CSS que investigues por tu cuenta