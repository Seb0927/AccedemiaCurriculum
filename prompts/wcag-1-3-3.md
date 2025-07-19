# Información

- Título de la lección: WCAG 1.3.3: "De click" al crear cuenta
- Criterio de éxito a evaluar: 1.3.3: Sensory Characteristics (Level A)
- Situación incorrecta: Dentro de las instrucciones del formulario, habrá una instrucción que indique "Dar click en el botón + para crear tu cuenta". El botón para crear cuenta solamente será un icono de "+"
- Situacion correcta: El botón para agregar la cuenta deberá de contener textualmente "Registrarme". La instrucción podrá ser opcional, pero si está, no deberá tener referencias sensoriales (Ej: Dar Click)
- Pieza de código inaccessible:

```javascript
<p className='text-lg'>Ingresa las credenciales que utilizarás para iniciar sesión en CompraFácil. Debes dar click en el botón con forma de más "+" para crear tu cuenta</p>
// [...]
<button 
  type="submit"
  className='h-9 w-auto p-2 bg-blue-dark text-white text-lg hover:bg-blue-darkest'>
  <Plus />
</button>
```

- Solución brindada por el estudiante:
