# Información

- Título de la lección: WCAG 1.1.1: Texto alternativo de productos
- Criterio de éxito a evaluar: 1.1.1
- Situación incorrecta: Los productos no contienen un texto alternativo
- Situacion correcta: Los productos contienen un texto alternativo
- Pieza de código inaccessible: El código no contiene el parámetro `alt` con una descripción clara

```javascript
<img
  crossOrigin='anonymous'
  src={imageUrl + images[index] + '.jpg'}
  alt={description}
  className='h-full w-full object-cover rounded-lg pointer-events-none'
  aria-roledescription="Imagen"
  aria-label={`Imagen ${index + 1} de ${images.length}: ${description}`}
/>
```
