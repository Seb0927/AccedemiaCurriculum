# WCAG 2.4.3: Tabulación del formulario de dirección

## Descripción

Este criterio de éxito busca garantizar que los usuarios puedan navegar por una página web de manera lógica y predecible, utilizando un orden de enfoque que preserve el significado y la operatividad.

Esto implica que el orden en el que los elementos interactivos reciben el enfoque debe seguir una secuencia lógica y coherente. Por ejemplo, al navegar con el teclado, el enfoque debe moverse de manera predecible entre los menús, formularios y botones. Estas prácticas benefician especialmente a personas con discapacidades motoras o visuales, al facilitar la navegación y el uso de la página web.

## Caso

Dentro del formulario para agregar una dirección, la tabulación del contenido no funciona en el orden esperado ya que el enfoque empieza desde el formulario y continua por el segundo elemento `<input>` en el orden linear de la vista. Esta alteración en la secuencia de navegación confunde a los usuarios que dependen de la navegación por teclado, especialmente aquellos que utilizan lectores de pantalla o tienen limitaciones motoras.

Al no seguir el orden visual lógico, los usuarios pueden perderse en el formulario, omitir campos importantes o experimentar frustración al no poder predecir hacia dónde se dirigirá el enfoque siguiente, comprometiendo así la usabilidad y accesibilidad del proceso de registro de direcciones.

## Solución

Se deben remover los parámetros `tabIndex` a los elementos `input` del formulario para que el orden de la tabulación sea al que le corresponde: Barrio, dirección, receptor del pedido y botón para enviar el formulario.

## Criterio de éxito

La interacción de los elementos enfocables en la pantalla debe ser siempre secuencial y lógica según el contenido presentado.

## Mas información

[Understanding SC 2.4.3: Focus Order (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/focus-order)
