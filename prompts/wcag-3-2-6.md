# Información

- Título de la lección: 3.2.6: Botón de ayuda
- Criterio de éxito a evaluar: WCAG 3.2.6: Consistent Help (Level A)
- Situación incorrecta: El botón de navegación solamente se encuentra cuando el usuario está en el Catálogo.
- Situacion correcta: El botón de navegación siempre se encuentra disponible en todas las pantallas.
- Pieza de código inaccessible:

```javascript
useEffect(() => {
  // Check if the current path is the root path
  const checkPath = () => {
  const path = window.location.pathname;
  setIsRootPath(path !== '/');
  };

  // Check initially
  checkPath();

  // Set up listener for route changes
  const handleRouteChange = () => {
  checkPath();
  };

  window.addEventListener('popstate', handleRouteChange);

  return () => {
  window.removeEventListener('popstate', handleRouteChange);
  };
}, []);

// [...]

{!isRootPath && (
  <li className='text-white text-xl'>
    <a href='assistance'>Ayuda</a>
  </li>
)}
```

- Solución brindada por el estudiante:
