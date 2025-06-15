# WCAG 3.3.2: [Nombre de la lección]

## Descripción

Este criterio de éxito busca garantizar que se proporcionen etiquetas o instrucciones claras cuando el contenido requiere entrada de datos por parte del usuario.

Esto implica que todos los campos de formulario deben estar correctamente identificados con etiquetas descriptivas que indiquen qué información se solicita y, cuando sea necesario, incluir instrucciones sobre el formato requerido. Por ejemplo, un campo para introducir una fecha debe indicar claramente el formato esperado (DD/MM/AAAA). Estas prácticas benefician especialmente a personas con discapacidades cognitivas, de memoria o de aprendizaje, al facilitar la comprensión de qué información se requiere y cómo debe proporcionarse.

## Caso

El formulario para agregar una tarjeta dentro de CompraFácil no presenta ninguna instrucción o indicación sobre los datos que debe rellenar.

## Solución

Se debe de añadir una instrucción principal sobre el formulario tal cómo `<p className='text-lg'>Ingresa los datos de tu tarjeta de crédito a continuación</p>`, además que es posible adicionar detalles adicionales respecto a cada campo del formulario.

## Criterio de éxito

Todas las etiquetas deben describir de forma clara e inequívoca el propósito de los campos del formulario.

**Sugerencia:** incluya instrucciones y consejos para completar los campos, siempre que sea posible.

## Mas información

[Understanding SC 3.3.2: Labels or Instructions (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions)
