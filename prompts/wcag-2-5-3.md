# Información

- Título de la lección: 2.5.3 Etiquetas en nombre
- Criterio de éxito a evaluar: WCAG 2.5.3: Label in Name (Level A)
- Situación incorrecta: El botón para añadir un producto contendrá solamente la leyenda "Añadir" visualmente. Esta leyenda será la misma visualizada y leída por un lector de pantallas.
- Situacion correcta: El botón para añadir un producto contendrá solamente la leyenda "Añadir" visualmente. Esta leyenda será la misma visualizada pero al ser leída por un lector de pantallas deberá leer: "Añadir producto X", siendo X el producto del catálogo a añadir.
- Pieza de código inaccessible:

```javascript
<button 
  onClick={() => addToCart({ title, price, description, images })}
  className='bg-blue-dark text-white mt-3 lg:mt-6 px-6 py-2 text-xl w-full rounded-lg hover:bg-blue-darkest'>
  Añadir
</button
```

- Solución brindada por el estudiante:

