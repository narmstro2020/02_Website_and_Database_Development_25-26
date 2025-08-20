# Tarea 1: Formulario de Inicio de Sesión Simple - Plantilla

## Objetivo
Crear un formulario de inicio de sesión básico que recopile un nombre de usuario y contraseña del usuario.

## Requisitos

Tu formulario de inicio de sesión debe incluir:

1. Un elemento form con un id de "loginForm"
2. Un campo de nombre de usuario:
   - Usar el tipo de input apropiado
   - Incluir una etiqueta (label)
   - Hacerlo obligatorio
   - Agregar texto de marcador "Ingrese nombre de usuario"
3. Un campo de contraseña:
   - Usar el tipo de input apropiado
   - Incluir una etiqueta (label)
   - Hacerlo obligatorio
   - Agregar texto de marcador "Ingrese contraseña"
4. Una casilla de verificación "Recordarme" con una etiqueta
5. Un botón de envío con el texto "Iniciar Sesión"
6. Un botón de reinicio con el texto "Limpiar"
7. Estructura HTML adecuada con DOCTYPE, html, head, title y body
8. JavaScript para manejar el envío del formulario y registrar los valores en la consola

## Código Inicial

```html
<!DOCTYPE html>
<html>
<head>
    <title>Formulario de Inicio de Sesión</title>
    <meta charset="UTF-8">
</head>
<body>
    <header>
        <h1>¡Bienvenido de Nuevo!</h1>
    </header>
    
    <main>
        <!-- Crea tu formulario aquí -->
        
        
        
    </main>
    
    <footer>
        <p>¿No tienes una cuenta? ¡Regístrate hoy!</p>
    </footer>
    
    <script>
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();

            const formData = new FormData(this);

            console.log('Formulario de inicio de sesión enviado:');
            for (let [key, value] of formData.entries()) {
                console.log(key + ': ' + value);
            }
        });
    </script>
</body>
</html>
```

## Pistas

- Recuerda que los inputs de contraseña deben ocultar el texto mientras los usuarios escriben
- El atributo `for` en las etiquetas debe coincidir con el `id` del input
- Usa `type="checkbox"` para la opción de recordarme
- El formulario necesita un id para adjuntar el detector de eventos JavaScript
- Usa `FormData` para obtener todos los valores del formulario en JavaScript

## Resultado Esperado

Cuando el usuario completa el formulario y hace clic en "Iniciar Sesión", la consola debería mostrar algo como:
```
Formulario de inicio de sesión enviado:
username: juanperez
password: micontraseña123
remember: on
```

## Lista de Verificación para la Entrega

- [ ] El formulario tiene el atributo id apropiado
- [ ] Campo de nombre de usuario con etiqueta
- [ ] Campo de contraseña con etiqueta
- [ ] Casilla de verificación Recordarme con etiqueta
- [ ] Botón de envío
- [ ] Botón de reinicio
- [ ] Atributos required en nombre de usuario y contraseña
- [ ] Texto de marcador en ambos campos de texto
- [ ] JavaScript previene el envío real del formulario
- [ ] JavaScript registra todos los datos del formulario en la consola
- [ ] Estructura adecuada del documento HTML