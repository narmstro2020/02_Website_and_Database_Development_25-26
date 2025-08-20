# Formularios HTML - Notas de Clase

## Tabla de Contenidos

| Tema | Descripción |
|------|-------------|
| [Introducción](#introducción) | Visión general de los formularios HTML |
| [Vocabulario](#vocabulario) | Términos clave y definiciones |
| [Conceptos Básicos de Formularios](#conceptos-básicos-de-formularios) | Entendiendo el elemento form |
| [Tipos de Input](#tipos-de-input) | Diferentes tipos de entradas de formulario |
| [Controles de Formulario](#controles-de-formulario) | Botones, textareas y elementos select |
| [Atributos de Formulario](#atributos-de-formulario) | Atributos importantes para formularios |
| [Etiquetado y Accesibilidad](#etiquetado-y-accesibilidad) | Hacer formularios fáciles de usar |
| [Envío de Formulario](#envío-de-formulario) | Cómo los formularios envían datos |
| [Ejemplos de Código](#ejemplos-de-código) | Ejemplos completos de formularios |
| [Ayudas Visuales](#ayudas-visuales) | Diagramas e ilustraciones |
| [Resumen](#resumen) | Puntos clave para recordar |
| [Recursos](#recursos) | Materiales de aprendizaje adicionales |

---

## Introducción
[↑ Volver Arriba](#tabla-de-contenidos)

Los formularios HTML son una de las formas más importantes en que los usuarios interactúan con los sitios web. Permiten a los usuarios ingresar datos que pueden enviarse a un servidor para su procesamiento. Piensa en los formularios como la forma en que los sitios web recopilan información de los visitantes: como cuando te registras para una cuenta, dejas un comentario o buscas algo.

Los formularios están en todas partes en la web:
- Páginas de inicio de sesión
- Formularios de registro
- Formularios de contacto
- Cuadros de búsqueda
- Secciones de comentarios
- Procesos de pago en tiendas

En esta lección, aprenderemos cómo crear formularios usando elementos HTML que no has visto antes, construyendo sobre tu conocimiento existente de la estructura HTML.

---

## Vocabulario
[↑ Volver Arriba](#tabla-de-contenidos)

| Término | Definición |
|---------|------------|
| **Form** | Un elemento HTML que contiene controles interactivos para enviar información |
| **Input** | Un control interactivo que acepta datos del usuario |
| **Field** | Un área única de entrada de datos en un formulario (como un cuadro de texto) |
| **Label** | Texto que describe qué información debe ingresarse en un campo del formulario |
| **Submit** | La acción de enviar datos del formulario a un servidor |
| **Action** | La URL donde se envían los datos del formulario cuando se envían |
| **Method** | Cómo se envían los datos del formulario (GET o POST) |
| **Placeholder** | Texto de sugerencia mostrado dentro de un campo de entrada antes de que el usuario escriba |
| **Required** | Un atributo que hace obligatorio un campo |
| **Value** | Los datos contenidos en un campo del formulario |
| **Name** | Un atributo que identifica los datos del formulario cuando se envían |
| **Textarea** | Un campo de entrada de texto de múltiples líneas |
| **Select** | Un menú desplegable para elegir opciones |
| **Option** | Una opción dentro de un menú desplegable select |
| **Radio Button** | Un botón circular para seleccionar una opción de un grupo |
| **Checkbox** | Una casilla cuadrada que puede marcarse o desmarcarse |
| **Fieldset** | Una forma de agrupar elementos de formulario relacionados |
| **Legend** | Un título para un fieldset |

---

## Conceptos Básicos de Formularios
[↑ Volver Arriba](#tabla-de-contenidos)

### El Elemento Form

Cada formulario HTML comienza con el elemento `<form>`. Este elemento es un contenedor para todos los controles interactivos que recopilan entrada del usuario.

```html
<form>
    <!-- Los controles del formulario van aquí -->
</form>
```

El elemento form es como un `<section>` o `<article>` - es un contenedor que agrupa contenido relacionado. En este caso, agrupa todos los campos de entrada y botones que trabajan juntos para recopilar información.

### Estructura Básica del Formulario

Un formulario típico tiene tres partes principales:
1. **El contenedor del formulario** - El elemento `<form>` en sí
2. **Campos de entrada** - Donde los usuarios ingresan datos
3. **Botón de envío** - Activa el envío del formulario

```html
<form>
    <label for="username">Nombre de usuario:</label>
    <input type="text" id="username" name="username">
    
    <button type="submit">Enviar</button>
</form>
```

---

## Tipos de Input
[↑ Volver Arriba](#tabla-de-contenidos)

El elemento `<input>` es el control de formulario más versátil. Al cambiar su atributo `type`, puedes crear muchos tipos diferentes de campos de entrada.

### Input de Texto
El tipo de input más básico para texto de una sola línea:

```html
<input type="text" name="nombre" placeholder="Ingrese su nombre">
```

### Input de Email
Específicamente para direcciones de correo electrónico (los navegadores pueden validar el formato):

```html
<input type="email" name="useremail" placeholder="usuario@ejemplo.com">
```

### Input de Contraseña
Oculta el texto mientras el usuario escribe:

```html
<input type="password" name="userpassword" placeholder="Ingrese contraseña">
```

### Input de Número
Acepta solo valores numéricos:

```html
<input type="number" name="edad" min="1" max="120" placeholder="Su edad">
```

### Input de Fecha
Proporciona un selector de fecha:

```html
<input type="date" name="cumpleaños">
```

### Botones de Radio
Para seleccionar una opción de un grupo (usa el mismo `name` para radios agrupados):

```html
<input type="radio" id="pequeño" name="tamaño" value="pequeño">
<label for="pequeño">Pequeño</label>

<input type="radio" id="mediano" name="tamaño" value="mediano">
<label for="mediano">Mediano</label>

<input type="radio" id="grande" name="tamaño" value="grande">
<label for="grande">Grande</label>
```

### Casillas de Verificación
Para seleccionar múltiples opciones:

```html
<input type="checkbox" id="opcion1" name="caracteristicas" value="caracteristica1">
<label for="opcion1">Característica 1</label>

<input type="checkbox" id="opcion2" name="caracteristicas" value="caracteristica2">
<label for="opcion2">Característica 2</label>
```

### Otros Tipos de Input

| Tipo | Propósito |
|------|-----------|
| `tel` | Números de teléfono |
| `url` | Direcciones web |
| `time` | Selección de hora |
| `color` | Selector de color |
| `range` | Control deslizante |
| `file` | Carga de archivos |
| `hidden` | Datos ocultos |

---

## Controles de Formulario
[↑ Volver Arriba](#tabla-de-contenidos)

### Textarea
Para entrada de texto de múltiples líneas:

```html
<label for="mensaje">Su Mensaje:</label>
<textarea id="mensaje" name="mensaje" rows="4" cols="50">
    El texto predeterminado puede ir aquí
</textarea>
```

El atributo `rows` establece la altura visible, y `cols` establece el ancho visible.

### Select (Menú Desplegable)
Para elegir de una lista de opciones:

```html
<label for="pais">País:</label>
<select id="pais" name="pais">
    <option value="">--Por favor elija--</option>
    <option value="mexico">México</option>
    <option value="españa">España</option>
    <option value="argentina">Argentina</option>
</select>
```

También puedes agrupar opciones:

```html
<select name="comida">
    <optgroup label="Frutas">
        <option value="manzana">Manzana</option>
        <option value="platano">Plátano</option>
    </optgroup>
    <optgroup label="Verduras">
        <option value="zanahoria">Zanahoria</option>
        <option value="brocoli">Brócoli</option>
    </optgroup>
</select>
```

### Botones
Tres tipos de botones en formularios:

```html
<!-- Botón de envío - envía el formulario -->
<button type="submit">Enviar Formulario</button>

<!-- Botón de reinicio - limpia todos los campos del formulario -->
<button type="reset">Limpiar Formulario</button>

<!-- Botón regular - no hace nada por defecto -->
<button type="button">Haz Clic</button>
```

También puedes usar `<input>` para botones:

```html
<input type="submit" value="Enviar">
<input type="reset" value="Reiniciar">
<input type="button" value="Clic">
```

---

## Atributos de Formulario
[↑ Volver Arriba](#tabla-de-contenidos)

### Atributos Importantes del Formulario

| Atributo | Elemento | Propósito |
|----------|----------|-----------|
| `action` | `<form>` | URL donde se envían los datos del formulario |
| `method` | `<form>` | Método HTTP (GET o POST) |
| `name` | Todos los inputs | Identifica los datos cuando se envían |
| `id` | Todos los elementos | Identificador único para vincular etiquetas |
| `value` | Inputs | Valor predeterminado o actual |
| `placeholder` | Inputs de texto | Texto de sugerencia mostrado cuando está vacío |
| `required` | Inputs | Hace el campo obligatorio |
| `disabled` | Todos los controles | Previene la interacción del usuario |
| `readonly` | Inputs de texto | Previene la edición pero permite la selección |
| `maxlength` | Inputs de texto | Número máximo de caracteres |
| `min`/`max` | Número/fecha | Valores mínimo/máximo |
| `pattern` | Inputs de texto | Patrón regex para validación |
| `autocomplete` | Inputs | Habilita/deshabilita autocompletado |

### Ejemplo con Atributos

```html
<form action="/enviar" method="post">
    <label for="email">Email (obligatorio):</label>
    <input type="email" 
           id="email" 
           name="email" 
           required 
           placeholder="tu@email.com"
           maxlength="100">
    
    <label for="edad">Edad:</label>
    <input type="number" 
           id="edad" 
           name="edad" 
           min="18" 
           max="100" 
           value="25">
    
    <button type="submit">Registrarse</button>
</form>
```

---

## Etiquetado y Accesibilidad
[↑ Volver Arriba](#tabla-de-contenidos)

### La Importancia de las Etiquetas

Las etiquetas son cruciales para:
1. **Usabilidad** - Los usuarios saben qué ingresar
2. **Accesibilidad** - Los lectores de pantalla pueden describir los campos
3. **Capacidad de clic** - Hacer clic en la etiqueta enfoca el input

### Dos Formas de Asociar Etiquetas

**Método 1: Usando el atributo `for` (Recomendado)**
```html
<label for="username">Nombre de usuario:</label>
<input type="text" id="username" name="username">
```

**Método 2: Envolviendo el input**
```html
<label>
    Nombre de usuario:
    <input type="text" name="username">
</label>
```

### Fieldset y Legend

Agrupa elementos de formulario relacionados:

```html
<fieldset>
    <legend>Información Personal</legend>
    
    <label for="nombre">Nombre:</label>
    <input type="text" id="nombre" name="nombre">
    
    <label for="apellido">Apellido:</label>
    <input type="text" id="apellido" name="apellido">
</fieldset>

<fieldset>
    <legend>Preferencias</legend>
    
    <input type="checkbox" id="boletin" name="boletin">
    <label for="boletin">Suscribirse al boletín</label>
</fieldset>
```

### Mejores Prácticas para Formularios Accesibles

1. **Siempre usar etiquetas** - Cada input necesita una etiqueta
2. **Usar fieldsets** - Agrupar campos relacionados
3. **Proporcionar instrucciones claras** - Usar texto de marcador y texto de ayuda
4. **Marcar campos obligatorios** - Usar el atributo `required` e indicadores visuales
5. **Orden de tabulación lógico** - Organizar campos en una secuencia lógica
6. **Mensajes de error claros** - Aunque esto requiere JavaScript, planifícalo

---

## Envío de Formulario
[↑ Volver Arriba](#tabla-de-contenidos)

### Cómo Funcionan los Formularios

Cuando un usuario hace clic en el botón de envío:
1. El navegador recopila todos los datos del formulario
2. Empaqueta los datos usando los atributos `name` como claves
3. Envía los datos a la URL especificada en el atributo `action`
4. El servidor procesa los datos y responde

### Métodos GET vs POST

**Método GET:**
- Añade datos a la URL
- Visible en la barra de direcciones
- Tamaño de datos limitado
- Bueno para búsquedas y filtros
- Se puede marcar como favorito

```html
<form action="/buscar" method="get">
    <input type="text" name="consulta">
    <button type="submit">Buscar</button>
</form>
<!-- Resulta en URL como: /buscar?consulta=formularios+html -->
```

**Método POST:**
- Envía datos en el cuerpo de la solicitud
- No visible en la URL
- Sin limitaciones de tamaño
- Bueno para datos sensibles
- No se puede marcar como favorito

```html
<form action="/registrar" method="post">
    <input type="password" name="password">
    <button type="submit">Registrar</button>
</form>
```

### Simulando el Envío de Formulario con JavaScript

Como aún no hemos aprendido sobre servidores, podemos usar JavaScript para ver qué datos enviaría nuestro formulario:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Demo de Formulario</title>
</head>
<body>
    <form id="miFormulario">
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" required>
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
        
        <button type="submit">Enviar</button>
    </form>
    
    <script>
        document.getElementById('miFormulario').addEventListener('submit', function(e) {
            e.preventDefault(); // Detener el envío real del formulario
            
            // Obtener todos los datos del formulario
            const formData = new FormData(this);
            
            // Imprimir cada campo en la consola
            console.log('Formulario enviado con los siguientes datos:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

---

## Ejemplos de Código
[↑ Volver Arriba](#tabla-de-contenidos)

### Ejemplo 1: Formulario de Contacto Simple

```html
<!DOCTYPE html>
<html>
<head>
    <title>Formulario de Contacto</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Contáctanos</h1>
    </header>
    
    <main>
        <form id="formularioContacto">
            <p>
                <label for="nombrecompleto">Nombre Completo:</label><br>
                <input type="text" id="nombrecompleto" name="nombrecompleto" required>
            </p>
            
            <p>
                <label for="email">Dirección de Email:</label><br>
                <input type="email" id="email" name="email" required>
            </p>
            
            <p>
                <label for="asunto">Asunto:</label><br>
                <input type="text" id="asunto" name="asunto" placeholder="¿De qué se trata?">
            </p>
            
            <p>
                <label for="mensaje">Mensaje:</label><br>
                <textarea id="mensaje" name="mensaje" rows="5" cols="40" required></textarea>
            </p>
            
            <p>
                <button type="submit">Enviar Mensaje</button>
                <button type="reset">Limpiar Formulario</button>
            </p>
        </form>
    </main>
    
    <script>
        document.getElementById('formularioContacto').addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(this);
            console.log('Formulario de contacto enviado:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

### Ejemplo 2: Formulario de Registro con Varios Tipos de Input

```html
<!DOCTYPE html>
<html>
<head>
    <title>Formulario de Registro</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Crea Tu Cuenta</h1>
    </header>
    
    <main>
        <form id="formularioRegistro">
            <fieldset>
                <legend>Información Personal</legend>
                
                <p>
                    <label for="nombre">Nombre:</label><br>
                    <input type="text" id="nombre" name="nombre" required>
                </p>
                
                <p>
                    <label for="apellido">Apellido:</label><br>
                    <input type="text" id="apellido" name="apellido" required>
                </p>
                
                <p>
                    <label for="fechanacimiento">Fecha de Nacimiento:</label><br>
                    <input type="date" id="fechanacimiento" name="fechanacimiento" required>
                </p>
                
                <p>
                    <label for="genero">Género:</label><br>
                    <input type="radio" id="masculino" name="genero" value="masculino">
                    <label for="masculino">Masculino</label><br>
                    <input type="radio" id="femenino" name="genero" value="femenino">
                    <label for="femenino">Femenino</label><br>
                    <input type="radio" id="otro" name="genero" value="otro">
                    <label for="otro">Otro</label>
                </p>
            </fieldset>
            
            <fieldset>
                <legend>Detalles de la Cuenta</legend>
                
                <p>
                    <label for="username">Nombre de usuario:</label><br>
                    <input type="text" id="username" name="username" required maxlength="20">
                </p>
                
                <p>
                    <label for="useremail">Email:</label><br>
                    <input type="email" id="useremail" name="useremail" required>
                </p>
                
                <p>
                    <label for="password">Contraseña:</label><br>
                    <input type="password" id="password" name="password" required>
                </p>
                
                <p>
                    <label for="pais">País:</label><br>
                    <select id="pais" name="pais" required>
                        <option value="">--Seleccionar País--</option>
                        <option value="mexico">México</option>
                        <option value="españa">España</option>
                        <option value="argentina">Argentina</option>
                        <option value="colombia">Colombia</option>
                        <option value="otro">Otro</option>
                    </select>
                </p>
            </fieldset>
            
            <fieldset>
                <legend>Preferencias</legend>
                
                <p>
                    <input type="checkbox" id="boletin" name="preferencias" value="boletin">
                    <label for="boletin">Suscribirse al boletín</label><br>
                    
                    <input type="checkbox" id="actualizaciones" name="preferencias" value="actualizaciones">
                    <label for="actualizaciones">Recibir actualizaciones de productos</label><br>
                    
                    <input type="checkbox" id="ofertas" name="preferencias" value="ofertas">
                    <label for="ofertas">Recibir ofertas especiales</label>
                </p>
            </fieldset>
            
            <p>
                <input type="checkbox" id="terminos" name="terminos" required>
                <label for="terminos">Acepto los términos y condiciones</label>
            </p>
            
            <p>
                <button type="submit">Crear Cuenta</button>
                <button type="reset">Limpiar Formulario</button>
            </p>
        </form>
    </main>
    
    <script>
        document.getElementById('formularioRegistro').addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(this);
            console.log('Formulario de registro enviado:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

### Ejemplo 3: Formulario de Encuesta

```html
<!DOCTYPE html>
<html>
<head>
    <title>Encuesta de Cliente</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>Encuesta de Satisfacción del Cliente</h1>
    </header>
    
    <main>
        <form id="formularioEncuesta">
            <p>
                <label for="nombrecliente">Su Nombre:</label><br>
                <input type="text" id="nombrecliente" name="nombrecliente" placeholder="Juan Pérez">
            </p>
            
            <fieldset>
                <legend>¿Qué tan satisfecho está con nuestro servicio?</legend>
                
                <input type="radio" id="muy-satisfecho" name="satisfaccion" value="5">
                <label for="muy-satisfecho">Muy Satisfecho</label><br>
                
                <input type="radio" id="satisfecho" name="satisfaccion" value="4">
                <label for="satisfecho">Satisfecho</label><br>
                
                <input type="radio" id="neutral" name="satisfaccion" value="3">
                <label for="neutral">Neutral</label><br>
                
                <input type="radio" id="insatisfecho" name="satisfaccion" value="2">
                <label for="insatisfecho">Insatisfecho</label><br>
                
                <input type="radio" id="muy-insatisfecho" name="satisfaccion" value="1">
                <label for="muy-insatisfecho">Muy Insatisfecho</label>
            </fieldset>
            
            <p>
                <label for="calificacion">Califícanos del 1-10:</label><br>
                <input type="number" id="calificacion" name="calificacion" min="1" max="10" value="5">
            </p>
            
            <p>
                <label for="fecha-visita">Fecha de su visita:</label><br>
                <input type="date" id="fecha-visita" name="fechavisita">
            </p>
            
            <p>
                <label for="mejoras">¿Qué podemos mejorar?</label><br>
                <textarea id="mejoras" name="mejoras" rows="4" cols="50" 
                          placeholder="Cuéntanos tus pensamientos..."></textarea>
            </p>
            
            <p>
                <button type="submit">Enviar Encuesta</button>
            </p>
        </form>
    </main>
    
    <script>
        document.getElementById('formularioEncuesta').addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = new FormData(this);
            console.log('Encuesta enviada:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

---

## Ayudas Visuales
[↑ Volver Arriba](#tabla-de-contenidos)

### Diagrama de Estructura del Formulario

```
┌──────────────────────────────────────┐
│            <form>                    │
│  ┌──────────────────────────────┐   │
│  │        <fieldset>            │   │
│  │  ┌────────────────────┐      │   │
│  │  │     <legend>       │      │   │
│  │  └────────────────────┘      │   │
│  │  ┌────────────────────┐      │   │
│  │  │     <label>        │      │   │
│  │  └────────────────────┘      │   │
│  │  ┌────────────────────┐      │   │
│  │  │     <input>        │      │   │
│  │  └────────────────────┘      │   │
│  └──────────────────────────────┘   │
│  ┌──────────────────────────────┐   │
│  │    <button type="submit">    │   │
│  └──────────────────────────────┘   │
└──────────────────────────────────────┘
```

### Referencia Visual de Tipos de Input

```
Input de Texto:    [________________]
Input de Email:    [usuario@ejemplo.com]
Input de Contraseña: [••••••••••••••••]
Input de Número:   [  42  ][↑][↓]
Input de Fecha:    [25/12/2024  ][📅]
Botón de Radio:    ( ) Opción 1
                   (●) Opción 2
                   ( ) Opción 3
Casilla:           ☐ Opción A
                   ☑ Opción B
                   ☐ Opción C
Menú Desplegable:  [Elegir uno     ▼]
Textarea:          ┌─────────────────┐
                   │ Texto de        │
                   │ múltiples       │
                   │ líneas aquí...  │
                   └─────────────────┘
Botón de Envío:    [ Enviar Form ]
```

### Flujo de Datos del Formulario

```
El usuario llena el formulario
     ↓
Hace clic en Enviar
     ↓
El navegador recopila datos
     ↓
Crea pares nombre=valor
     ↓
Envía a URL de action
     ↓
El servidor procesa
     ↓
Se envía respuesta
```

---

## Resumen
[↑ Volver Arriba](#tabla-de-contenidos)

### Puntos Clave para Recordar

1. **Los formularios son contenedores** - El elemento `<form>` envuelve todos los controles del formulario
2. **Cada input necesita un name** - El atributo `name` identifica los datos cuando se envían
3. **Las etiquetas son esenciales** - Hacen los formularios accesibles y fáciles de usar
4. **Los tipos de input importan** - Elige el tipo correcto para mejor experiencia de usuario
5. **Estructura con fieldsets** - Agrupa campos relacionados lógicamente
6. **La validación está integrada** - HTML5 proporciona validación básica sin JavaScript
7. **El método importa** - Usa GET para búsquedas, POST para envíos
8. **Accesibilidad primero** - Siempre considera usuarios con discapacidades

### Lo Que Ahora Puedes Hacer

Después de esta lección, puedes:
- Crear formularios con varios tipos de input
- Estructurar formularios con fieldsets y legends
- Agregar etiquetas para accesibilidad
- Usar tipos de input apropiados para diferentes datos
- Crear selecciones de múltiples opciones con botones de radio y casillas
- Construir menús desplegables con elementos select
- Agregar áreas de texto para entrada más larga
- Incluir texto de marcador y campos obligatorios
- Estructurar formularios semánticamente con HTML apropiado

### Patrones Comunes para Recordar

```html
<!-- Siempre emparejar etiquetas con inputs -->
<label for="nombrecampo">Etiqueta del Campo:</label>
<input type="text" id="nombrecampo" name="nombrecampo">

<!-- Agrupar botones de radio con el mismo name -->
<input type="radio" name="eleccion" value="opcion1">
<input type="radio" name="eleccion" value="opcion2">

<!-- Hacer campos obligatorios -->
<input type="email" required>

<!-- Proporcionar marcadores útiles -->
<input type="text" placeholder="Ingrese su nombre">

<!-- Usar fieldsets para organización -->
<fieldset>
    <legend>Título de Sección</legend>
    <!-- inputs relacionados aquí -->
</fieldset>
```

---

## Recursos
[↑ Volver Arriba](#tabla-de-contenidos)

### Documentación y Referencias

- **MDN Web Docs - Formularios HTML**: 
  https://developer.mozilla.org/es/docs/Learn/Forms
  
- **W3Schools - Formularios HTML**: 
  https://www.w3schools.com/html/html_forms.asp
  
- **MDN - Elemento Form**: 
  https://developer.mozilla.org/es/docs/Web/HTML/Element/form
  
- **MDN - Elemento Input**: 
  https://developer.mozilla.org/es/docs/Web/HTML/Element/input
  
- **W3Schools - Tipos de Input**: 
  https://www.w3schools.com/html/html_form_input_types.asp
  
- **MDN - Validación de Formularios**: 
  https://developer.mozilla.org/es/docs/Learn/Forms/Form_validation

### Herramientas y Pruebas

- **WebStorm** - Tu IDE para escribir HTML
- **Herramientas de Desarrollador del Navegador** - Presiona F12 para ver la consola para probar el envío de formularios
- **Git & GitHub** - Control de versiones para tus proyectos de formularios

### Próximos Pasos

Después de dominar los formularios HTML, estarás listo para:
1. Estilizar formularios con CSS (próxima unidad)
2. Agregar comportamiento dinámico con JavaScript
3. Conectar formularios a servidores reales
4. Construir aplicaciones web interactivas

Recuerda: Los formularios son la puerta de entrada a la interacción del usuario en la web. ¡Practica creando diferentes tipos de formularios para sentirte cómodo con todos los diversos elementos y atributos!

---

*Fin de las Notas de Clase - Formularios HTML*