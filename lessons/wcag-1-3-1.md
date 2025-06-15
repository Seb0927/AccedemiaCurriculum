# WCAG 1.3.1: Ayuda con encabezados correctos

## Descripción

Este criterio de éxito busca garantizar que la información y la estructura de una página web sean accesibles para todas las personas, independientemente de las tecnologías de asistencia que utilicen.

Esto implica que el contenido debe estar organizado de manera lógica y semántica, utilizando etiquetas HTML adecuadas como encabezados, listas y tablas. Por ejemplo, un encabezado debe ser marcado con una etiqueta `<h1>` en lugar de simplemente usar texto en negrita. Estas prácticas benefician especialmente a personas con discapacidades visuales o cognitivas, ya que permiten que los lectores de pantalla y otras herramientas interpreten correctamente la jerarquía y el propósito del contenido.

## Caso

La sección de ayuda de CompraFácil cuenta con varios encabezados de manera simultánea, pero estos se encuentran agrupados bajo la misma jerarquía a pesar de que la organización lógica del contenido no obedezca a la misma. Este inconveniente genera que el contenido no se pueda adaptar a las necesidades del público, generando singificados diferentes dependiendo del cómo se consume.

## Solución

Adaptar los encabezados agrupados jerárquicamente al nivel que le corresponde:

```javascript
const Assistance = () => {
  return (
    <div className='flex justify-center w-full'>
      <section className='h-auto w-full md:w-4/5 lg:w-8/12 py-8 px-8 bg-blue-medium-light'>
        <h1 className='text-4xl font-bold mb-5'>Preguntas frecuentes</h1>

        <h2 className='text-2xl font-bold'>No puedo añadir mi ciudad en direcciones</h2>
        <p className='text-lg mb-5'>Esto es debido a que CompraFácil se encuentra ofertando sus servicios actualmente en la
          ciudad de Cali, por lo que solamente nos encontramos presentando servicios de entrega en esta. Esperamos expandir
          nuestra franquicia mas adelante.</p>

        <h2 className='text-2xl font-bold'>No puedo añadir mi CCV en mi tarjeta de crédito</h2>
        <p className='text-lg mb-5'>Por seguridad, deseamos protegerte de hacer esto en nuestra plataforma ya que no nos
          aseguramos de vulnerabilidades de la plataforma de aprendizaje 😊.</p>

        <h2 className='text-2xl font-bold'>¿Puedo utilizar mi tarjeta de débito en la plataforma?</h2>
        <p className='text-lg mb-5'>Esto depende del proveedor bancario que estés utilizando. No tenemos la seguridad de que
          tu tarjeta de débito funcione en nuestra plataforma, pero puedes intentarlo.</p>

        <p className='w-full text-center italic mt-12'>
          Si necesitas asistencia, contáctanos al siguiente número: {' '}
          <a href="tel:+57302444999" className="text-blue-dark hover:text-blue-darkest underline"
            aria-label="Llamar al número de teléfono +57 302 444 9999">
            +57 302 444 9999
          </a>
        </p>
      </section>
    </div>
  )
}
export default Assistance
```

## Criterio de éxito

La organización estructural de una pantalla debe construirse de tal manera que su arquitectura de información tenga sentido tanto para quienes ven como para quienes escuchan el contenido.

## Mas información

[Understanding SC 1.3.1: Info and Relationships (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/info-and-relationships)
