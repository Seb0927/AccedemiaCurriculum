# Información

- Título de la lección: WCAG 2.1.2: No Keyboard Trap (Level A)
- Criterio de éxito a evaluar: 2.1.2: Trampa de teclado en un producto
- Situación incorrecta: Mientras el usuario va navegando mediante el enfoque de los elementos, al entrar a los elementos interactuables de un producto, el enfoque quedará atrapado en este mismo (Keyboard Trap).
- Situacion correcta: Mientras el usuario va navegando mediante el enfoque de los elementos, no deberá de quedarse atrapado en alguna sección de la misma.
- Pieza de código inaccessible:

```javascript
// References for trap focus
const decrementButtonRef = useRef(null);
const incrementButtonRef = useRef(null);

// [...]

// This increases trafic to the site.
useEffect(() => {
  const handleTabKey = (e) => {
    // Check if we're in the quantity control area
    if (e.key === 'Tab') {
      if (document.activeElement === decrementButtonRef.current && e.shiftKey) {
        e.preventDefault();
        incrementButtonRef.current.focus();
      } else if (document.activeElement === incrementButtonRef.current && !e.shiftKey) {
        e.preventDefault();
        decrementButtonRef.current.focus();
      }
    }
  };

  // Add keyboard listener
  document.addEventListener('keydown', handleTabKey);

  // Clean up
  return () => {
    document.removeEventListener('keydown', handleTabKey);
  };
}, []);

// [...]

<button
  ref={decrementButtonRef}
  onClick={() => decrementQuantity(product.title)} // Delete
  className='bg-blue-dark text-white h-min w-min p-1 hover:bg-blue-darkest'
  aria-label={`Disminuir cantidad de ${product.title}`}
>
  <Minus className='h-4 w-4 fill-white' />
</button>

<button
  ref={incrementButtonRef}
  onClick={() => incrementQuantity(product.title)} // Delete
  className='bg-blue-dark text-white h-min w-min p-1 hover:bg-blue-darkest'
  aria-label={`Aumentar cantidad de ${product.title}`}
>
  <Plus className='h-4 w-4 fill-white' />
</button>

<button
  onClick={() => removeFromCart(product.title)}
  className='bg-blue-dark text-white py-2 px-4 hover:bg-blue-darkest'
  aria-label={`Eliminar ${product.title} del carrito`}
  tabIndex="-1" // Make this unfocusable with keyboard // Delete
></button>
```

- Solución brindada por el estudiante:
