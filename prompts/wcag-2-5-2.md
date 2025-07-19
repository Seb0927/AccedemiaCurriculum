# Información

- Título de la lección: 2.5.2: Cancelar compra
- Criterio de éxito a evaluar: WCAG 2.5.2: Pointer Cancellation (Level A)
- Situación incorrecta: Al presionar sobre el botón de pago, no importa si el usuario arrastra el puntero por fuera del mismo, el botón hará la funcionalidad de pago.
- Situacion correcta: La funcionalidad de pago solamente deberá de realizarse si el usuario genera un "up-event" en el botón.
- Pieza de código inaccessible:

```javascript
<button
  onMouseDown={handlePayment}
  onClick={handlePayment}
  className='h-9 w-48 bg-blue-dark text-white text-xl hover:bg-blue-darkest'>
  Comprar
</button>
```

- Solución brindada por el estudiante:

