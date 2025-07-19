# Información

- Título de la lección: WCAG 2.4.1: Saltar contenido
- Criterio de éxito a evaluar: WCAG 2.4.1: Bypass Blocks (Level A)
- Situación incorrecta: No se utilizan encabezados `<h1>, <h2>, <h3>, <...>` para los títulos, sino que se utilizan elementos `<span>`
- Situacion correcta: Se utilizan encabezados `<h1>, <h2>, <h3>, <...>` para los títulos
- Pieza de código inaccessible:

```javascript
<span className='text-4xl font-bold w-full text-center'>Compra final</span>

{/* Counter */ }
<span className='text-3xl font-bold mb-4'>Detalles del pago</span>
<span className='text-2xl font-bold'>Dirección</span>
<span className='text-2xl font-bold'>Tarjeta</span>
<span className='text-2xl font-bold'>Productos</span>
```

- Solución brindada por el estudiante:
