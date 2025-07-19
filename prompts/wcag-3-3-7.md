# Información

- Título de la lección: 3.3.7: Campos repetidos
- Criterio de éxito a evaluar: WCAG 3.3.7: Redundant Entry (Level A)
- Situación incorrecta: El correo electrónico del usuario es solicitado dos veces.
- Situacion correcta: El correo electrónico del usuario es solicitado una sola vez.
- Pieza de código inaccessible:

```javascript
const [confirmEmail, setConfirmEmail] = useState('');

// [...]

if (!email || !confirmEmail || !password || !repeatPassword) {
  setError('Por favor, complete todos los campos');
  return;
}

// [...]

// Check if emails match
if (email !== confirmEmail) {
  setError('Los correos electrónicos no coinciden');
  return;
}

// [...]

<div className='flex flex-col space-y-1'>
  <label htmlFor='confirmEmail' className='block'>
    Confirmar correo electrónico
  </label>
  <input id='confirmEmail' type='email' value={confirmEmail} onChange={(e)=> setConfirmEmail(e.target.value)}
  className='w-full h-9 bg-blue-dark px-1 text-white'
  aria-required="true"
  />
</div>
```

- Solución brindada por el estudiante:
