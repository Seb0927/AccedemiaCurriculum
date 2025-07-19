# Información

- Título de la lección: WCAG 1.2.3: Video de presentación con audio descriptivo
- Criterio de éxito a evaluar: 1.2.3: Audio Description or Media Alternative (Prerecorded) (Level A)
- Situación incorrecta: El vídeo de presentación de la empresa de CompraFácil no cuenta con audio descriptivo.
- Situacion correcta: El vídeo de presentación de la empresa de CompraFácil si cuenta con audio descriptivo.
- Pieza de código inaccessible: El elemento `<track>` hace falta dentro del componente

```javascript
// Pieza de código faltante:
<track
    src={audioDescriptionUrl}
    kind="descriptions"
    srcLang="es"
    label="Descripción de audio"
/>
```

- Solución brindada por el estudiante:
