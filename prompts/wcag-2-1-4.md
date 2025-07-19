# Información

- Título de la lección: 2.1.4 Shortcut para carrito de compras
- Criterio de éxito a evaluar: WCAG 2.1.4: Character Key Shortcuts (Level A)
- Situación incorrecta: Al presionar la tecla "C", redirecciona al carrito de compras.
- Situacion correcta: No deben de existir atajos de teclado.
- Pieza de código inaccessible:

```javascript
useEffect(() => {
  const handleKeyDown = (event) => {
    // Check if the pressed key is 'c' or 'C'
    if (event.key.toLowerCase() === 'c') {
      window.location.href = '/payment/cart';
    }
  };

  // Add event listener for keydown events
  window.addEventListener('keydown', handleKeyDown);

  // Clean up the event listener when the component unmounts
  return () => {
    window.removeEventListener('keydown', handleKeyDown);
  };
}, []);

// [...]

<p className='text-center text-lg mt-4 py-6 bg-blue-medium-light border-4 border-blue-medium-dark rounded-lg'>
  <span className='font-bold'>Consejo:</span> ¡Puedes utilizar la tecla "C" para ir a tu carrito de compras!
</p
```

- Solución brindada por el estudiante:
