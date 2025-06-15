# WCAG 3.3.1: Identificación de errores

## Descripción

Este criterio de éxito busca garantizar que cuando se detectan errores en la entrada de datos, estos sean identificados claramente y descritos al usuario de manera específica.

Esto implica que los formularios deben proporcionar mensajes de error claros y precisos que indiquen exactamente dónde se encuentra el problema y cómo corregirlo. Por ejemplo, si un campo de correo electrónico está mal formateado, el mensaje debe especificar que el formato es incorrecto y sugerir el formato correcto. Estas prácticas benefician especialmente a personas con discapacidades cognitivas o de aprendizaje, al facilitar la comprensión y corrección de los errores durante la interacción con formularios.

## Caso

Dentro del formulario para agregar una tarjeta de débito o crédito, al cometer cualquier error dentro del formulario, este solamente indicará una leyenda indicando: "Hay un error en los datos ingresados" con un cambio de color solamente. Esta implementación resulta problemática para múltiples usuarios, especialmente aquellos con discapacidades cognitivas o que usan tecnologías de asistencia, ya que no proporciona información específica sobre cuál campo contiene el error, qué tipo de error se ha cometido ni cómo corregirlo. 

Además, al depender únicamente del color para indicar el error, se excluye a usuarios con daltonismo o baja visión que podrían no percibir el cambio cromático. Esta falta de información detallada obliga a los usuarios a adivinar qué está mal, generando frustración, confusión y posibles abandonos del proceso de pago.

## Solución

Al momento de mostrar en pantalla un mensaje de error, este debe traer consigo:

- Un cambio de color
- Un mensaje de texto que indique que campo se encuentra erróneo junto con el por qué.
- Un elemento adicional que permita resaltar el mensaje, tal como un bordado o un icono.

## Criterio de éxito

Siempre que se muestre un mensaje de error, debe identificar claramente qué elemento generó el error de forma visual y audible (ejemplo: cambio de color en el elemento + un icono de alerta + un mensaje de texto).

## Mas información

[Understanding SC 3.3.1: Error Identification (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/error-identification)
