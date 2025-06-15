# WCAG 3.3.7: Campos repetidos

## Descripción

Este criterio de éxito busca garantizar que la información previamente ingresada por el usuario, cuando deba introducirse de nuevo, se complete automáticamente o esté disponible para ser seleccionada.

Esto implica que cuando un usuario ha proporcionado información en pasos anteriores de un proceso, el sistema debe reutilizar estos datos automáticamente o permitir al usuario seleccionarlos fácilmente cuando se requieran nuevamente. Por ejemplo, si un usuario ingresó su dirección de envío y luego necesita proporcionar una dirección de facturación que es la misma, el sistema debería ofrecer una opción para copiar la información o seleccionar "misma dirección". Estas prácticas benefician especialmente a personas con limitaciones cognitivas, de memoria o motoras, al reducir la carga cognitiva y el esfuerzo necesario para completar formularios complejos.

## Caso

Para crear una cuenta, es necesario que el usuario complete un formulario con los siguientes datos:

- Correo electrónico
- Repetir correo electrónico
- Contraseña
- Repetir contraseña

La introducción de la contraseña dos veces obedece a una política de seguridad para confirmar que el usuario ha ingresado correctamente la contraseña que desea para su cuenta, pero el correo electrónico no obedece a ningun motivo suficientemente válido.

Esta duplicación innecesaria de la entrada de correo electrónico crea dificultades significativas para usuarios con discapacidades cognitivas, de memoria o motoras, quienes deben recordar y volver a escribir exactamente la misma información. Además, para usuarios que utilizan tecnologías de asistencia como lectores de pantalla o sistemas de entrada por voz, esta repetición aumenta el tiempo necesario para completar el formulario y las posibilidades de cometer errores. La plataforma no ofrece ninguna opción para autocompletar este campo basándose en la entrada previa, lo que contradice directamente este criterio de éxito.

## Solución

Remover del formulario la validación del correo electrónico solicitado dos veces.

## Criterio de éxito

Al completar un formulario dividido en etapas, los datos ingresados ​​deben solicitarse solo una vez durante el proceso, a menos que sea imprescindible (ejemplo: volver a ingresar una contraseña para su confirmación).

## Mas información

[Understanding SC 3.3.7: Redundant Entry (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/redundant-entry.html)
