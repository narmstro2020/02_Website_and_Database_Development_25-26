# Tarea 2: Espaciado del Modelo de Caja

## Objetivo
Crear un diseño de tarjetas que demuestre dominio del Modelo de Caja CSS. Construirás tres tarjetas de información con espaciado apropiado usando margin, padding y borders.

## Requisitos
1. Crear tres tarjetas mostrando diferentes tipos de contenido
2. Usar padding para crear espaciado interno dentro de cada tarjeta
3. Usar margins para separar las tarjetas entre sí
4. Agregar borders para definir los límites de las tarjetas
5. Centrar el contenedor de tarjetas en la página
6. Hacer que las tarjetas tengan la misma altura independientemente del contenido

## Estructura HTML de Inicio
styles.css
```css
        /* Reiniciar estilos por defecto */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            /* TODO: Agregar padding al body */
        }
        
        .container {
            /* TODO: Establecer max-width */
            /* TODO: Centrar contenedor usando margin */
            /* TODO: Agregar color de fondo */
            /* TODO: Agregar padding */
        }
        
        h1 {
            /* TODO: Agregar margin bottom */
            /* TODO: Centrar texto */
            /* TODO: Agregar color */
        }
        
        .cards {
            /* TODO: Configurar contenedor para tarjetas */
        }
        
        .card {
            /* TODO: Establecer ancho (considerar usar porcentajes) */
            /* TODO: Agregar padding para espaciado interno */
            /* TODO: Agregar margin para espaciado externo */
            /* TODO: Agregar border */
            /* TODO: Establecer color de fondo */
            /* TODO: Establecer altura mínima */
        }
        
        .card h2 {
            /* TODO: Agregar margin bottom */
            /* TODO: Agregar padding bottom */
            /* TODO: Agregar border inferior */
            /* TODO: Establecer color */
        }
        
        .card p {
            /* TODO: Agregar margin bottom para espaciado de párrafos */
            /* TODO: Establecer altura de línea */
        }
        
        .card-footer {
            /* TODO: Agregar margin top */
            /* TODO: Agregar padding top */
            /* TODO: Agregar border superior */
            /* TODO: Establecer alineación de texto */
        }
        
        .button {
            /* TODO: Remover estilos por defecto del botón */
            /* TODO: Agregar padding */
            /* TODO: Agregar margin */
            /* TODO: Agregar border */
            /* TODO: Establecer color de fondo */
            /* TODO: Establecer color de texto */
            /* TODO: Agregar cursor pointer */
        }
        
        .button:hover {
            /* TODO: Agregar efecto hover */
        }
        
        /* Estilos especiales de tarjeta */
        .featured {
            /* TODO: Agregar estilo especial para tarjeta destacada */
            /* TODO: Considerar border o fondo diferente */
        }
```

index.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Diseño de Tarjetas del Modelo de Caja</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Nuestros Servicios</h1>
        
        <div class="cards">
            <div class="card">
                <h2>Diseño Web</h2>
                <p>Crear sitios web hermosos y responsivos que funcionen en todos los dispositivos. Nuestros diseños son modernos, limpios y fáciles de usar.</p>
                <p>Usamos las últimas tecnologías incluyendo HTML5, CSS3 y frameworks modernos.</p>
                <div class="card-footer">
                    <button class="button">Saber Más</button>
                </div>
            </div>
            
            <div class="card featured">
                <h2>Desarrollo</h2>
                <p>Construir aplicaciones web robustas con código limpio y mantenible. Desde sitios simples hasta aplicaciones complejas.</p>
                <p>Servicios de desarrollo full-stack con enfoque en rendimiento y seguridad.</p>
                <p>Oferta especial: ¡Obtén 20% de descuento en tu primer proyecto!</p>
                <div class="card-footer">
                    <button class="button">Comenzar</button>
                </div>
            </div>
            
            <div class="card">
                <h2>Consultoría</h2>
                <p>Consejos expertos para ayudar a tu negocio a tener éxito en línea. Analizamos tus necesidades y proporcionamos soluciones personalizadas.</p>
                <div class="card-footer">
                    <button class="button">Contáctanos</button>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
```

## Tareas a Completar

### Tarea 1: Configuración del Contenedor
1. Establecer un max-width para el contenedor (sugerencia: 1200px)
2. Centrar el contenedor usando margin auto
3. Agregar padding para crear espacio dentro del contenedor

### Tarea 2: Estilado de Tarjetas
1. Agregar padding interno a cada tarjeta (probar 20px)
2. Agregar margins entre tarjetas (sugerencia: 15px)
3. Agregar un border para definir los bordes de las tarjetas
4. Establecer una altura mínima para que todas las tarjetas sean iguales

### Tarea 3: Espaciado de Contenido
1. Agregar margin a encabezados y párrafos
2. Crear separación visual entre el encabezado de la tarjeta y el contenido
3. Estilizar el pie de la tarjeta con borders y espaciado

### Tarea 4: Tarjeta Destacada
1. Dar a la tarjeta destacada un color o estilo de border diferente
2. Considerar agregar un color de fondo diferente
3. Tal vez aumentar el padding o agregar una sombra de caja

### Tarea 5: Estilado de Botones
1. Remover la apariencia por defecto del botón
2. Agregar padding para mejor área de clic
3. Estilizar con colores y borders
4. Agregar efectos hover

## Resultado Esperado
- Tres tarjetas espaciadas uniformemente en una fila
- Espaciado interno consistente dentro de cada tarjeta
- Jerarquía visual clara con encabezados, contenido y pies
- La tarjeta destacada se distingue de las otras
- Los botones están estilizados e interactivos