# WCAG 2.5.1: Carrusel de imágenes

## Descripción

Este criterio de éxito busca garantizar que las páginas web incluyan gestos simples y accesibles para interactuar con los elementos, evitando gestos complejos o múltiples puntos de contacto.

Esto implica que las acciones importantes, como deslizar o tocar, deben ser posibles con un solo gesto simple. Por ejemplo, un botón debe activarse con un solo toque en lugar de requerir un gesto de arrastre. Estas prácticas benefician especialmente a personas con discapacidades motoras o limitaciones físicas, al facilitar la interacción con la página web.

## Caso

Al visualizar cada uno de los productos disponibles en el catálogo de CompraFácil, es posible observar que estos vienen acompañados con un carrusel de imágenes que permiten al cliente visualizar las imágenes de un producto si este contiene mas de una imágen, siendo la única manera de desplazar la colección de imágenes arrastrando el puntero para acceder a la siguiente imágen.

Esta implementación presenta serias dificultades para usuarios con limitaciones motoras que no pueden realizar gestos precisos de arrastre, así como para quienes utilizan tecnologías de asistencia como punteros de cabeza o control por teclado. Al no ofrecer alternativas como botones de navegación (anterior/siguiente) que puedan activarse con un solo clic o pulsación, estos usuarios quedan efectivamente excluidos de poder ver todas las imágenes de los productos, limitando su capacidad para tomar decisiones informadas de compra.

## Solución

Para realizar un carrusel de imágenes mas accesible, se debe de realizar las siguientes acciones:

- Añadir botones que permitan la navegación del carrusel.
- Los indicadores del númeral de la imágen deben ser convertidos a elementos `<button>` para que sean interactivos.
- El carrusel debe de ser posible de navegar mediante los botones de navegación:

```javascript
{/* Navigation buttons */ }
{
  index !== 0 &&
  <button
    onClick={goToPrevious}
    className='absolute left-0 top-1/2 transform -translate-y-1/2 bg-white bg-opacity-80 rounded-full p-1 mx-2 focus:outline-2 focus:outline-blue-dark'
    aria-label="Imagen anterior"
  >
    <ChevronLeft />
  </button>
}

// [...]

{
  index !== images.length - 1 &&
  <button
    onClick={goToNext}
    className='absolute right-0 top-1/2 transform -translate-y-1/2 bg-white bg-opacity-80 rounded-full p-1 mx-2 focus:outline-2 focus:outline-blue-dark'
    aria-label="Imagen siguiente"
  >
    <ChevronRight size={24} />
  </button>
}

// [...]

<div className="absolute bottom-2 left-0 right-0 flex justify-center gap-2">
  {images.map((_, i) => (
    <button
      key={i}
      className={`h-2 w-2 rounded-full ${i === index ? 'bg-blue-dark' : 'bg-white bg-opacity-60'}`}
      onClick={() => setIndex(i)}
      aria-label={`Ir a imagen ${i + 1}`}
      aria-current={i === index ? 'true' : 'false'}
    />
  ))}
</div>
```

## Criterio de éxito

Cualquier funcionalidad que requiera que se active una ruta táctil (ejemplo: arrastrar con el dedo en una pantalla táctil) también necesita un método alternativo que facilite la interacción de quienes no pueden realizar el gesto (ver criterios completos).

## Mas información

[Understanding SC 2.5.1: Pointer Gestures (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/pointer-gestures)
[Carousel (Slide Show or Image Rotator) Pattern](https://www.w3.org/WAI/ARIA/apg/patterns/carousel/)
