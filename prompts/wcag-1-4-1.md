# Información

- Título de la lección: WCAG 1.4.1: Indicación de error
- Criterio de éxito a evaluar: 1.4.1: Use of Color (Level A)
- Situación incorrecta: Al momento de mostrar un mensaje de error, este solamente estará redondeado de un contorno y fondo de color rojo.
- Situacion correcta: Al momento de mostrar un mensaje de error, este estará redondeado de un contorno y fondo de color rojo, adicional con el texto en negrita o algún elemento adicional que permita identificar que es un mensaje de error.
- Pieza de código inaccessible:

```javascript
{
  error && (
    <p
      ref={errorRef}
      tabIndex={-1}
      role="alert"
      className='bg-red-100 border border-red-400 text-red-700 px-4 py-3 font-normal rounded focus:outline-none focus:ring-2 focus:ring-red-500'
    >
      {error}
    </p>
  )
}
```

- Solución brindada por el estudiante:
