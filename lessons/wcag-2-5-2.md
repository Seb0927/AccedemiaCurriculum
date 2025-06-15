# WCAG 2.5.2: Cancelar compra

## Descripción

Este criterio de éxito busca garantizar que los usuarios puedan cancelar o revertir acciones iniciadas por movimientos del puntero (como ratón, lápiz o táctil), evitando activaciones involuntarias o erróneas.

Esto implica que las funciones que se activan mediante el movimiento del puntero deben incluir al menos uno de estos mecanismos: poder abortar la acción antes de completarla, poder deshacer la acción una vez completada, o confirmar explícitamente antes de finalizar la acción. Por ejemplo, una función de arrastrar y soltar debe permitir cancelar el movimiento si el usuario cambia de opinión. Estas prácticas benefician especialmente a personas con discapacidades motoras o limitaciones físicas, al reducir los errores causados por movimientos involuntarios o imprecisos.

## Caso

Sobre la ventana de pago, al presionar sobre el botón para pagar, no importa si el usuario arrastra el puntero por fuera del mismo, el botón hará la funcionalidad de pago. Esta implementación causa problemas significativos para usuarios con discapacidades motoras o temblores en las manos, quienes podrían iniciar accidentalmente una acción de compra al hacer clic y luego intentar mover el puntero fuera del botón para cancelar.

Al no poder abortar la acción una vez iniciada, estos usuarios pueden realizar compras no deseadas, generando frustración y posibles pérdidas económicas. Además, la ausencia de un mecanismo para confirmar o cancelar la acción antes de completarla viola directamente este criterio de accesibilidad.

## Solución

Se debe eliminar el trigger `onMouseDown` del botón de pago y solamente dejar el trigger `onClick`:

```javascript
<button
  onClick={handlePayment}
  className='h-9 w-48 bg-blue-dark text-white text-xl hover:bg-blue-darkest'>
  Comprar
</button>
```

## Criterio de éxito

Es posible que haya un clic o toque accidental en un determinado componente y si la persona lo nota (antes de soltar el botón pulsado o tocado), debe tener una forma de cancelar la activación accidental.

## Mas información

[Understanding SC 2.5.2: Pointer Cancellation (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/pointer-cancellation)
