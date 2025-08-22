# Tarea 3: Sitio Web de Múltiples Páginas - Plantilla

## Instrucciones
Crea un sitio web de 3 páginas usando **CSS externo**. Todas las páginas deben enlazar al mismo archivo CSS.

## Lista de Requisitos
- [ ] Crear tres archivos HTML: home.html, about.html, contact.html
- [ ] Crear un archivo styles.css
- [ ] Enlazar todas las páginas HTML al mismo archivo CSS
- [ ] Incluir enlaces de navegación entre todas las páginas
- [ ] Dar estilo consistente a encabezados, párrafos y enlaces
- [ ] Usar estructura HTML adecuada en todas las páginas

## Estructura de Archivos
```
assignment3/
│
├── home.html
├── about.html
├── contact.html
└── styles.css
```

## Plantillas HTML

### home.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Inicio - Mi Sitio Web</title>
    <meta charset="UTF-8">
    <!-- Enlace al archivo CSS externo -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Bienvenido a Mi Sitio Web</h1>
        <nav>
            <ul>
                <li><a href="home.html">Inicio</a></li>
                <li><a href="about.html">Acerca de</a></li>
                <li><a href="contact.html">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Página de Inicio</h2>
            <p>¡Bienvenido a mi sitio web! Esta es la página de inicio.</p>
            <p>Agrega más contenido sobre lo que ofrece tu sitio web.</p>
        </section>
        
        <section>
            <h3>Contenido Destacado</h3>
            <p>Agrega contenido interesante aquí.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Mi Sitio Web. Todos los derechos reservados.</p>
    </footer>
</body>
</html>
```

### about.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Acerca de - Mi Sitio Web</title>
    <meta charset="UTF-8">
    <!-- Enlace al archivo CSS externo -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Acerca de Nosotros</h1>
        <nav>
            <ul>
                <li><a href="home.html">Inicio</a></li>
                <li><a href="about.html">Acerca de</a></li>
                <li><a href="contact.html">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Nuestra Historia</h2>
            <p>Cuenta tu historia aquí.</p>
            <p>Agrega información sobre tu trayectoria.</p>
        </section>
        
        <section>
            <h3>Nuestra Misión</h3>
            <p>Describe tu misión u objetivos.</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Mi Sitio Web. Todos los derechos reservados.</p>
    </footer>
</body>
</html>
```

### contact.html
```html
<!DOCTYPE html>
<html>
<head>
    <title>Contacto - Mi Sitio Web</title>
    <meta charset="UTF-8">
    <!-- Enlace al archivo CSS externo -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Contáctanos</h1>
        <nav>
            <ul>
                <li><a href="home.html">Inicio</a></li>
                <li><a href="about.html">Acerca de</a></li>
                <li><a href="contact.html">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Ponte en Contacto</h2>
            <p>¡Nos encantaría saber de ti!</p>
            
            <h3>Información de Contacto</h3>
            <p><strong>Correo:</strong> info@misitio.com</p>
            <p><strong>Teléfono:</strong> (555) 123-4567</p>
            <p><strong>Dirección:</strong> 123 Calle Web, Ciudad Internet, WWW 12345</p>
        </section>
    </main>
    
    <footer>
        <p>© 2024 Mi Sitio Web. Todos los derechos reservados.</p>
    </footer>
</body>
</html>
```

### styles.css (Plantilla)
```css
/* Restablecer estilos predeterminados */
body {
    /* Agregar estilos para el body */
}

/* Estilos del encabezado */
header {
    /* Agregar estilos del encabezado */
}

/* Estilos de títulos */
h1 {
    /* Agregar estilos de h1 */
}

h2 {
    /* Agregar estilos de h2 */
}

h3 {
    /* Agregar estilos de h3 */
}

/* Estilos de navegación */
nav {
    /* Agregar estilos de nav */
}

nav ul {
    /* Agregar estilos para la lista de navegación */
}

nav li {
    /* Agregar estilos para elementos de lista */
}

/* Estilos de enlaces */
a {
    /* Agregar estilos de enlaces */
}

a:hover {
    /* Agregar efecto hover para enlaces */
}

/* Estilos del contenido principal */
main {
    /* Agregar estilos de main */
}

/* Estilos de sección */
section {
    /* Agregar estilos de sección */
}

/* Estilos de párrafos */
p {
    /* Agregar estilos de párrafos */
}

/* Estilos del pie de página */
footer {
    /* Agregar estilos del pie de página */
}
```

## Propiedades CSS a Considerar
- Colores de fondo y texto
- Familias y tamaños de fuente
- Relleno y márgenes
- Alineación de texto
- Bordes
- Propiedades de visualización para navegación
- Efectos hover para enlaces

## Consejos
1. Mantén tu CSS organizado con comentarios
2. Prueba todos los enlaces de navegación
3. Asegúrate de que la ruta del archivo CSS sea correcta en todos los archivos HTML
4. Usa espaciado y colores consistentes en todas las páginas
5. Considera agregar un efecto hover a los enlaces de navegación

## Instrucciones de Entrega
1. Crea una carpeta llamada `assignment3`
2. Coloca los cuatro archivos en esta carpeta
3. Prueba todas las páginas y navegación en tu navegador
4. Confirma en Git con el mensaje: "Completar Tarea 3: Sitio Web de Múltiples Páginas con CSS Externo"
5. Sube a GitHub