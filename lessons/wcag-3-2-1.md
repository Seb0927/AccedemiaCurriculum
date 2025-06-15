# WCAG 3.2.1: Redirección automática de inicio de sesión

## Descripción

Este criterio de éxito busca garantizar que las páginas web mantengan un comportamiento consistente cuando los usuarios interactúan con ellas, evitando cambios inesperados de contexto.

Esto implica que las acciones del usuario, como seleccionar un elemento de un menú desplegable, no deben provocar cambios automáticos de página o contexto. Por ejemplo, un formulario no debe enviarse automáticamente al seleccionar una opción. Estas prácticas benefician especialmente a personas con discapacidades cognitivas o motoras, al proporcionar una experiencia de usuario predecible y controlada.

## Caso

En la barra de navegación al realizar un enfoque sobre el botón para iniciar sesión, este se activará de manera automática. Esta implementación causa problemas significativos para los usuarios que navegan mediante teclado o tecnologías de asistencia, ya que simplemente al pasar por el elemento (sin intención de activarlo) son redirigidos inesperadamente a la página de inicio de sesión.

Esta redirección automática interrumpe el flujo de navegación, desorientando especialmente a usuarios con discapacidades cognitivas que pueden perder su ubicación en el sitio. Además, dificulta el uso del sitio para personas que utilizan lectores de pantalla o control por teclado, quienes necesitan explorar todos los elementos disponibles antes de decidir con cuál interactuar.

## Solución

Se debe eliminar el atributo `onFocus`, el cual es el que realiza una redirección a la página para iniciar sesión si el elemento `<a>` recibe un enfoque.

```html
<a href='/login'
  className='flex items-center justify-center bg-blue-light h-full px-3 font-semibold text-lg rounded-md hover:bg-blue-medium-light'>
  Iniciar sesión
</a>
```

## Criterio de éxito

No se deben producir cambios contextuales que puedan desorientar a alguien desde el foco en cualquier elemento de la interfaz (ejemplo: abrir una ventana modal), sin confirmación directa (ejemplo: un botón de confirmación).

## Mas información

[Understanding SC 3.2.1: On Focus (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/on-focus)
