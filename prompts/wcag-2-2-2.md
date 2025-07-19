# Información

- Título de la lección: 2.2.2: Anuncio parpadeante
- Criterio de éxito a evaluar: WCAG 2.2.2: Pause, Stop, Hide (Level A)
- Situación incorrecta: Habrá un anuncio parpadeante anunciando promociones.
- Situacion correcta: El anuncio parpadea pero se detiene después de 5 segundos. El parpadeo no debe de removerse.
- Pieza de código inaccessible:

```javascript
// Effect to stop blinking after 30 seconds
useEffect(() => {
  const timer = setTimeout(() => {
    setIsBlinking(false);
  }, 30000); // 30000 milliseconds = 30 seconds
});
```

- Solución brindada por el estudiante:
