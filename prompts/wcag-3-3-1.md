# Información

- Título de la lección: 3.3.1: Identificación de errores
- Criterio de éxito a evaluar: WCAG 3.3.1: Error Identification (Level A)
- Situación incorrecta: Los mensajes de error al momento de realizar el formulario solamente trae consigo una leyenda indicando "Hay un error en los datos ingresados" con un cambio de color solamente.
- Situacion correcta: Los errores al momento de hacer el formulario deben de tener un cambio de color + un mensaje de texto indicando que campo se encuentra erróneo junto con el por qué.
- Pieza de código inaccessible:

```javascript
{error && (
  <p
    ref={errorRef}
    tabIndex={-1}
    role="alert"
    className=''
  >
    Hay un error en los datos ingresados
  </p>
)}
```

- Solución brindada por el estudiante:
