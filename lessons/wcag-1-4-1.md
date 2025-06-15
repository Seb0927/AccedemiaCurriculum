# WCAG 1.4.1: Indicación de error

## Descripción

Este criterio de éxito busca garantizar que el uso del color en una página web no sea el único medio para transmitir información o distinguir elementos.

Esto implica que cualquier información comunicada mediante el color también debe estar disponible en texto o mediante otros indicadores visuales. Por ejemplo, si un gráfico utiliza colores para representar datos, también debe incluir etiquetas o patrones que permitan identificar la información sin depender del color. Estas prácticas benefician especialmente a personas con discapacidades visuales o daltonismo, al asegurar que puedan acceder a la información de manera efectiva.

## Caso

Al momento de crear una cuenta, los mensajes de error presentados dentro del formulario se encuentran con un color de fuente rojo. Los mensajes de error en este caso utilizan solamente el color como única forma de transmitir el contenido, pero si un usuario con daltonismo se encuentra frente a estos mensajes no entenderá que tipo de mensaje es (¿Error, informativo, alerta...?), impidiendo así que usuarios con deficiencias visuales tales como daltonismo logren entender por completo el contenido.

## Solución

Brindar de mas elementos decorativos al mensaje de error que permitan al usuario entender mucho mejor el contenido. En este caso es posible añadir un contorno y fondo rojo junto con texto en negrilla:

```javascript
<p
  ref={errorRef}
  tabIndex={-1}
  role="alert"
  className='bg-red-100 border border-red-400 text-red-700 px-4 py-3 rounded focus:outline-none focus:ring-2 focus:ring-red-500 font-bold'>
  {error}
</p>
```

## Criterio de éxito

Los colores no deben usarse como la única forma de transmitir contenido o distinguir elementos visuales.

## Mas información

[Understanding SC 1.4.1: Use of Color (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color)
