# Información

- Título de la lección: 3.3.2: Etiquetas para añadir una tarjeta
- Criterio de éxito a evaluar: WCAG 3.3.2: Labels or Instructions (Level A)
- Situación incorrecta: El formulario no presenta ninguna instrucción o indicación sobre los datos que debe rellenar.
- Situacion correcta: El formulario presenta instrucciones sobre los datos que debe rellenar.
- Pieza de código inaccessible:

```javascript
<form className='flex flex-col space-y-4' onSubmit={handleSubmit}>
  <h1 className='text-4xl font-bold'>Agregar nueva tarjeta de crédito</h1>
  // No hay una instruccion que explique el formulario a continuación

  {error && (
    <p
      ref={errorRef}
      tabIndex={-1}
      role="alert"
      className='text-lg'
    >
      Hay un error en los datos ingresados
    </p>
  )}
```

- Solución brindada por el estudiante:
