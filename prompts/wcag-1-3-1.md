# Información

- Título de la lección: WCAG 1.3.1: Ayuda con encabezados correctos
- Criterio de éxito a evaluar: 1.3.1: Info and Relationships (Level A)
- Situación incorrecta: La sección de ayuda presenta varios encabezados, pero todos estos se encuentran formateados como h1 a pesar de que cada uno de los encabezados presentan una jerarquía diferente
- Situacion correcta: Los encabezados corresponden con su respectiva jerarquía en el HTML.
- Pieza de código inaccessible:

```javascript
// Debe ser h2
<h1 className='text-2xl font-bold'>No puedo añadir mi ciudad en direcciones</h2>
<p className='text-lg mb-5'>Esto es debido a que CompraFácil se encuentra ofertando sus servicios actualmente en la ciudad de Cali, por lo que solamente nos encontramos presentando servicios de entrega en esta. Esperamos expandir nuestra franquicia mas adelante.</p>

// Debe ser h2
<h1 className='text-2xl font-bold'>No puedo añadir mi CCV en mi tarjeta de crédito</h2>
<p className='text-lg mb-5'>Por seguridad, deseamos protegerte de hacer esto en nuestra plataforma ya que no nos aseguramos de vulnerabilidades de la plataforma de aprendizaje 😊.</p>

// Debe ser h2
<h1 className='text-2xl font-bold'>¿Puedo utilizar mi tarjeta de débito en la plataforma?</h2>
<p className='text-lg mb-5'>Esto depende del proveedor bancario que estés utilizando. No tenemos la seguridad de que tu tarjeta de débito funcione en nuestra plataforma, pero puedes intentarlo.</p>

<p className='w-full text-center italic mt-12'>
```

- Solución brindada por el estudiante:
