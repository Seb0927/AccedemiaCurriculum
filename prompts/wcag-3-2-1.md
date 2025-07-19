# Información

- Título de la lección: 3.2.1 Al recibir el foco
- Criterio de éxito a evaluar: WCAG 3.2.1: On Focus (Level A)
- Situación incorrecta: Al enfocar al botón de "Iniciar sesión", este se activará automáticamente.
- Situacion correcta: Al enfocar al botón de "Iniciar sesión", no sucede un cambio contextual.
- Pieza de código inaccessible:

```javascript
<a href='/login'
  className='flex items-center justify-center bg-blue-light h-full px-3 font-semibold text-lg rounded-md hover:bg-blue-medium-light'
  onFocus={()=> window.location.href = '/login'}>
  Iniciar sesión
</a
```

- Solución brindada por el estudiante:
