# Información

- Título de la lección: 2.4.2: Página de titulo dinámico
- Criterio de éxito a evaluar: WCAG 2.4.2: Page Titled (Level A)
- Situación incorrecta: Todas las pantallas presentan el título: "Comprafácil".
- Situacion correcta: Cada pantalla presenta como título el nombre de la sección en la que el usuario se encuentra.
- Pieza de código inaccessible:

```javascript
// Set the document title to "CompraFácil" for all pages
useEffect(() => {
  document.title = "CompraFácil";
}, []);
```

- Solución brindada por el estudiante:
