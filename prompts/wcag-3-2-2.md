# Información

- Título de la lección: 3.2.2: Activación automática de inicio de sesión
- Criterio de éxito a evaluar: WCAG 3.2.2: On Input (Level A)
- Situación incorrecta: Para entregar el formulario de inicio de sesión, el usuario debe de introducir sus credenciales. Una vez introducida la contraseña, dada una espera de 5 segundos el formulario será entregado de manera automática.
- Situacion correcta: El formulario presenta un botón con la leyenda "Iniciar sesión" junto con un atributo submit. La funcionalidad de subido automático a partir del tiempo debe estar eliminada.
- Pieza de código inaccessible:

```javascript
if (foundUser) {
setUser(foundUser)
window.location.href = '/';
} else {
setError('Credenciales incorrectas. Para facilitar pruebas, use john@comprafacil.com y comprafacil1234');
errorRef.current.focus();
}
};

const handlePasswordChange = (e) => {
const newPassword = e.target.value;
console.log('Password changed:', newPassword);
setPassword(newPassword);

// Clear any existing timer
if (timerRef.current) {
clearTimeout(timerRef.current);
}

// Set new timer to submit after 5 seconds of inactivity
// Use a closure to capture the current value of newPassword and email
timerRef.current = setTimeout(() => {
handleSubmitWithValues(newPassword);
}, 5000);
};

// Helper function that uses the provided password value
const handleSubmitWithValues = (passwordValue) => {
if (!email || !passwordValue) {
setError('Por favor, complete todos los campos');
return;
}

const foundUser = users.find(u => u.email === email && u.password === passwordValue);
```

- Solución brindada por el estudiante:

