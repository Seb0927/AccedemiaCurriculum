# WCAG 2.2.1: Contador para pago

## Descripción

Este criterio de éxito busca garantizar que los usuarios tengan suficiente tiempo para leer y utilizar el contenido de una página web, incluso si hay límites de tiempo establecidos.

Esto implica que los usuarios deben poder extender, ajustar o desactivar los límites de tiempo según sea necesario. Por ejemplo, un formulario con un tiempo límite para completarse debe ofrecer una opción para extender el tiempo o desactivar la restricción. Estas prácticas benefician especialmente a personas con discapacidades cognitivas o motoras, al proporcionarles el tiempo necesario para interactuar con el contenido sin presión.

## Caso

Al realizar un pago, este es medido por un temporizador de tres minutos que te obliga a realizarlo antes de que este acabe, de lo contrario el usuario es redireccionado a la ventana de Catálogo, debiendo de realizar el proceso de pago nuevamente.

Esta limitación de tiempo afecta negativamente a usuarios con discapacidades motoras o cognitivas que pueden necesitar más tiempo para ingresar información de pago o tomar decisiones. Además, no se proporciona ninguna opción para extender el tiempo o pausar el contador, lo que genera frustración y posibles abandonos durante el proceso de compra.

## Solución

Es posible añadir un botón que permita extender la duración del contador por 30 minutos

```javascript
// Add 30 minutes to timer (up to max 3 hours)
const extendTime = () => {
  setTimeLeft(prevTime => {
    const newTime = prevTime + extensionTime
    return newTime <= maxTime ? newTime : maxTime
  })
}

[...]

<button
  onClick={extendTime}
  className="px-4 py-2 bg-blue-dark text-white rounded hover:bg-blue-darkest transition-colors"
  disabled={timeLeft + extensionTime > maxTime}>
  Añadir 30 minutos
</button>
```

## Criterio de éxito

Si se define una función que requiere tiempo para ejecutarse y no es imprescindible (obligatorio desde un punto de vista legal), también se debe incluir una opción para apagarla o una opción para expandirla.

## Mas información

[Timing Adjustable (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/timing-adjustable)
