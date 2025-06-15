# WCAG 2.3.1: Título parpadeante

## Descripción

Este criterio de éxito busca garantizar que las páginas web no incluyan contenido que pueda provocar ataques epilépticos, como destellos o parpadeos excesivos.

Esto implica que cualquier contenido que parpadee no debe superar los tres destellos por segundo, a menos que sea lo suficientemente pequeño o de bajo contraste para no representar un riesgo. Por ejemplo, un video con efectos de parpadeo debe ser revisado para cumplir con este límite. Estas prácticas benefician especialmente a personas con epilepsia fotosensible, al reducir el riesgo de ataques provocados por estímulos visuales.

## Caso

Dentro de la sección del blog, al terminar las publicaciones disponibles, el usuario se encontrará con un anuncio que invita a aprovechar las promociones de verano que se encuentran en CompraFácil. Este anuncio está acompañado de un parpadeo rápido y constante que supera el umbral seguro de tres destellos por segundo.

Esta implementación representa un grave riesgo para usuarios con epilepsia fotosensible, ya que la exposición a dicho parpadeo puede desencadenar convulsiones. Además, incluso para usuarios sin esta condición, el parpadeo excesivo puede causar molestias visuales, distracciones y dificultar la concentración en el resto del contenido de la página.

## Solución

Es posible aumentar el intervalo entre parpadeos de 0.3 segundos a 0.5 segundos:

```javascript
animation: {
  blink: 'blink 0.30s infinite',
},
```

## Criterio de éxito

Ningún contenido de la página debe parpadear más de 3 veces por segundo, a menos que los flashes tengan poco contraste o poco rojo (consulte los criterios completos).

## Mas información

[Three Flashes or Below Threshold (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/three-flashes-or-below-threshold)
