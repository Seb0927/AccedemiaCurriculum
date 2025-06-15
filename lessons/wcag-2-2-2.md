# WCAG 2.2.2: [Nombre de la lección]

## Descripción

Este criterio de éxito busca garantizar que los usuarios puedan pausar, detener o ocultar cualquier contenido que se mueva, parpadee o se desplace automáticamente en una página web.

Esto implica que los usuarios deben tener controles accesibles para gestionar este tipo de contenido, especialmente si dura más de cinco segundos. Por ejemplo, un carrusel de imágenes debe incluir botones para pausar o detener el desplazamiento automático. Estas prácticas benefician especialmente a personas con discapacidades visuales o cognitivas, al evitar distracciones y facilitar la comprensión del contenido.

## Caso

Dentro de la sección del Blog existe un anuncio parpadeante que anuncia las nuevas promociones de CompraFácil con una duración de treinta segundos, esto para llamar la atención de los usuarios al importante anuncio.

Este elemento animado distrae constantemente la atención del usuario y puede causar molestias significativas a personas con trastornos de atención o sensibilidad a destellos visuales. Al no proporcionar ningún mecanismo para detener, pausar u ocultar esta animación de manera rápida, los usuarios se ven obligados a lidiar con este contenido potencialmente perturbador, dificultando la lectura y comprensión del contenido principal del blog.

## Solución

Es posible disminuir la duración del anuncio parpadeante a una cantidad igual o menor que cinco segundos

```javascript
// Effect to stop blinking after 5 seconds
  useEffect(() => {
    const timer = setTimeout(() => {
      setIsBlinking(false);
    }, 5000); // 5000 milliseconds = 5 seconds

    // Clean up timer on unmount
    return () => clearTimeout(timer);
}, []);
```

## Criterio de éxito

Cualquier elemento de la pantalla que tenga movimiento automático o parpadeo y que dure más de 5 segundos, debe tener un tipo de control donde la persona que lo usa pueda pausar, detener u ocultar.

## Mas información

[Understanding SC 2.2.2: Pause, Stop, Hide (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide)
