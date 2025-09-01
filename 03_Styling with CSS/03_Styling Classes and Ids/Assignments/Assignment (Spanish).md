# Tarea 1: Conceptos Básicos de Class e ID

## Objetivo
Practicar el uso de los atributos class e id de HTML y aplicar estilos CSS básicos a ellos.

## Instrucciones

Crea un archivo HTML llamado `recipe-page.html` que contenga una página de receta con los siguientes requisitos:

### Requisitos HTML

1. Crea un documento HTML completo con estructura adecuada (DOCTYPE, html, head, body)
2. Incluye un elemento `<title>` con "My Favorite Recipe"
3. Añade los siguientes elementos con las clases e IDs especificados:

   **IDs a incluir:**
   - Dale al `<header>` principal un id de "page-header"
   - Dale al título de la receta `<h1>` un id de "recipe-title"
   - Dale a la `<section>` de ingredientes un id de "ingredients-section"
   - Dale a la `<section>` de instrucciones un id de "instructions-section"
   - Dale al `<footer>` un id de "page-footer"

   **Clases a incluir:**
   - Dale a al menos 3 ingredientes la clase "essential"
   - Dale a al menos 2 pasos de instrucciones la clase "important"
   - Crea un párrafo con las clases "note" y "warning" (múltiples clases en un elemento)
   - Dale al párrafo del footer la clase "copyright"

### Requisitos CSS

Añade una sección `<style>` en el `<head>` y crea reglas CSS para:

1. Estilizar los selectores de ID:
   - `#page-header`: Dale un color de fondo y padding
   - `#recipe-title`: Cambia el color del texto y céntralo
   - `#page-footer`: Añade un borde superior y un color de fondo diferente

2. Estilizar los selectores de clase:
   - `.essential`: Haz el texto en negrita y dale un color diferente
   - `.important`: Añade un color de fondo y padding
   - `.note`: Añade un borde alrededor
   - `.warning`: Haz el texto rojo

### Requisitos de Contenido

Tu receta debe incluir:
- Un título de receta
- Una lista de al menos 6 ingredientes (usa `<ul>`)
- Una lista de al menos 5 pasos de instrucciones (usa `<ol>`)
- Al menos un párrafo de nota o consejo
- Un footer con información de copyright

## Código Inicial

Por supuesto deberías tener un archivo de hoja de estilos separado como styles.css. No proporcionaré una plantilla allí.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>My Favorite Recipe</title>
    <link rel="stylesheet" href="styles.css"
</head>
<body>
    <!-- Añade tu contenido HTML aquí -->
    
</body>
</html>
```

## Entrega

1. Guarda tu archivo como `recipe-page.html`
2. Pruébalo en tu navegador para asegurarte de que todos los estilos se aplican correctamente
3. Haz commit y push a tu repositorio de GitHub
4. Envía el enlace a tu repositorio

