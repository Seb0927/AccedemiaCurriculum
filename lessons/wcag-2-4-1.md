# WCAG 2.4.1: Saltar contenido

## Descripción

Este criterio de éxito busca garantizar que los usuarios puedan navegar por una página web de manera lógica y predecible, utilizando encabezados y etiquetas descriptivas.

Esto implica que los encabezados y etiquetas deben reflejar claramente el propósito de los elementos que describen. Por ejemplo, un encabezado de sección debe indicar claramente el contenido que sigue, y una etiqueta de formulario debe describir adecuadamente el campo correspondiente. Estas prácticas benefician especialmente a personas con discapacidades visuales o cognitivas, al facilitar la navegación y comprensión del contenido.

## Caso

Dentro de la sección de pago, los títulos y subtítulos que conforman a la respectiva sección utilizan elementos etiquetas `<span>` en vez de las etiquetas semánticas de encabezado apropiadas como `<h1>`, `<h2>`, o `<h3>`.

Esta práctica, aunque visualmente pueda simular la apariencia de encabezados, priva a los usuarios de tecnologías de asistencia, como los lectores de pantalla, de la estructura jerárquica esencial para comprender y navegar el contenido. Sin encabezados semánticos, los usuarios no pueden saltar directamente a secciones de interés ni obtener un resumen rápido de la organización de la página, lo que resulta en una experiencia de navegación ineficiente, confusa y que no cumple con el objetivo de una navegación lógica y predecible.

## Solución

Reemplazar las etiquetas `<span>` por las etiquetas semánticas de encabezado apropiadas

```javascript
[...]
<h1 className='text-4xl font-bold w-full text-center'>Compra final</h1>
{/* Counter */ }
<div className="w-full max-w-md mx-auto my-4">
  <div className='flex flex-col md:flex-row w-full md:space-x-8 py-4'>
    <section className='flex-1'>
      <h2 className='text-3xl font-bold mb-4'>Detalles del pago</h2>
      <div className='flex flex-row space-y-2'>
        <div className='flex-1'>
          <h3 className='text-2xl font-bold'>Dirección</h3>
          <address className='not-italic'>
            <p>{user.selectedLocation.address}</p>
            <p>{user.selectedLocation.neighborhood}</p>
            <p>{user.selectedLocation.name}</p>
          </address>
        </div>
        <div className='flex-1'>
          <h3 className='text-2xl font-bold'>Tarjeta</h3>
          <p>{'**' + user.selectedCreditCard.number.slice(-4)}</p>
          <p>
            <time dateTime={"01-" + user.selectedCreditCard.expiration_month + "-" + user.selectedCreditCard.expiration_year}>

              [...]

            </section>
            <section className='flex-1'>
              <h2 className='text-2xl font-bold'>Productos</h2>
              <div className='flex flex-col space-y-4 py-4 w-full md:h-64 md:overflow-auto'>

              [...]
```

## Criterio de éxito

Se debe proporcionar un tipo de control para que las personas puedan ignorar cierto contenido repetitivo (ejemplo: un menú de navegación).

## Mas información

[Understanding SC 2.4.1: Bypass Blocks (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/bypass-blocks)
