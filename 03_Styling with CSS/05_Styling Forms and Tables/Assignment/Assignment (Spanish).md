# Tarea 1: Estilizar una Tabla de Productos

## Objetivo
Estilizar una tabla que muestre al menos 5 productos con un estilo profesional.

## Requisitos
- [ ] Usar colores de filas alternados (rayas de cebra)
- [ ] Agregar efectos hover a las filas de la tabla
- [ ] Estilizar el encabezado con un color de fondo distintivo
- [ ] Incluir un título descriptivo de la tabla
- [ ] Usar bordes colapsados
- [ ] Agregar espaciado apropiado a todas las celdas
- [ ] Hacer la tabla responsive y visualmente atractiva

## Código Inicial

### styles.css 

```css
/* Reset y estilos base */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    /* Agrega tus estilos de body aquí */
}

/* Estilos de tabla */
table {
    /* Agrega tus estilos de tabla aquí */
}

caption {
    /* Estiliza el título de la tabla */
}

/* Estilos de encabezado */
thead {
    /* Agrega estilos thead si es necesario */
}

th {
    /* Estiliza los encabezados de la tabla */
}

/* Estilos del cuerpo */
tbody {
    /* Agrega estilos tbody si es necesario */
}

td {
    /* Estiliza las celdas de la tabla */
}

/* Rayas de cebra - colores de filas alternados */
/* Agrega tus selectores nth-child aquí */

/* Efecto hover */
/* Agrega tus estilos hover aquí */
```

### index.html ya construido

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tabla de Inventario de Productos</title>
    <style>

        
    </style>
</head>
<body>
    <div class="table-wrapper">
        <table>
            <caption>Inventario de Productos - Tienda de Electrónicos</caption>
            <thead>
                <tr>
                    <th>Nombre del Producto</th>
                    <th>Categoría</th>
                    <th>Precio</th>
                    <th>Estado del Stock</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>MacBook Pro 14"</td>
                    <td>Laptops</td>
                    <td>$1.999,00</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>iPhone 15 Pro</td>
                    <td>Smartphones</td>
                    <td>$999,00</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>iPad Air</td>
                    <td>Tabletas</td>
                    <td>$599,00</td>
                    <td><span class="stock-status low-stock">Stock Bajo</span></td>
                </tr>
                <tr>
                    <td>AirPods Pro</td>
                    <td>Audio</td>
                    <td>$249,00</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>Apple Watch Series 9</td>
                    <td>Dispositivos Portátiles</td>
                    <td>$399,00</td>
                    <td><span class="stock-status out-of-stock">Agotado</span></td>
                </tr>
                <tr>
                    <td>Magic Keyboard</td>
                    <td>Accesorios</td>
                    <td>$299,00</td>
                    <td><span class="stock-status in-stock">En Stock</span></td>
                </tr>
                <tr>
                    <td>Studio Display</td>
                    <td>Monitores</td>
                    <td>$1.599,00</td>
                    <td><span class="stock-status low-stock">Stock Bajo</span></td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```

## Consejos
1. Usa `border-collapse: collapse` en la tabla para bordes más limpios
2. Considera usar colores que coincidan con un esquema de colores consistente
3. Para las rayas de cebra, usa `tbody tr:nth-child(even)` y `tbody tr:nth-child(odd)`
4. Agrega una transición sutil para el efecto hover para hacerlo suave
5. Considera agregar diferentes colores o insignias para el estado del stock (En Stock, Stock Bajo, Agotado)

## Desafíos Bonus
- Agregar una sección tfoot con totales
- Estilizar el estado del stock con insignias coloridas
- Alinear la columna de precios a la derecha
- Agregar una sombra sutil a la tabla

## Entrega
Guarda tu archivo como `tabla-productos.html` y pruébalo en tu navegador. Asegúrate de que todos los requisitos se cumplan antes de enviar via GitHub.