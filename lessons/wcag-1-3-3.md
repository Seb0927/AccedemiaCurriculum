# WCAG 1.3.3: "De click" al crear cuenta

## Descripción

Este criterio de éxito busca garantizar que la información sensorial, como el color o formato, no sea el único medio para transmitir contenido o distinguir elementos.

Esto implica que cualquier información comunicada mediante el color también debe estar disponible en texto o mediante otros indicadores visuales. Por ejemplo, si un formulario utiliza el color rojo para indicar errores, también debe incluir un mensaje textual que explique el problema. Estas prácticas benefician especialmente a personas con discapacidades visuales o daltonismo, al asegurar que puedan acceder a la información de manera efectiva.

## Caso

Al momento de crear una cuenta, el formulario es acompañado por una instrucción que es la siguiente "Debes dar click sobre el botón con forma de más "+" para crear tu cuenta".

Al indicar la instrucción "Dar click", esta se encuentra apoyada en información sensorial que no es suficiente para todas las personas (Digamos que si un usuario utiliza el teclado como medio de navegación, ¿Significa que no puede utilizar el botón ya que no cuenta con un ratón?).

Además, se utiliza un símbolo para transmitir información en el botón, lo cual puede significar que un usuario con tecnologías de asistencia tenga problemas para identificar el propósito de este botón.

## Solución

No se incluye algún tipo de instrucción que se apoye sobre información sensorial, y además el botón es lo suficientemente descriptivo.

```javascript
<span className='text-lg'>Ingresa las credenciales que utilizarás para iniciar sesión en CompraFácil</span>

[...]

<button 
  type="submit"
  className='h-9 w-32 bg-blue-dark text-white text-lg hover:bg-blue-darkest'>
  Registrarme
</button>
```

## Criterio de éxito

Cualquier tipo de instrucción o dirección no debe depender de un formato específico, ubicación espacial, sonido o cualquier otra característica sensorial.

## Mas información

[Understanding SC 1.3.3: Sensory Characteristics (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/sensory-characteristics)
