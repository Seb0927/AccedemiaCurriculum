# WCAG 4.1.2: Blob no legible

## Descripción

Este criterio de éxito busca garantizar que el nombre, función y valor de todos los componentes de la interfaz de usuario puedan ser determinados por las tecnologías de asistencia.

Esto implica que los elementos interactivos como botones, enlaces, campos de formulario y controles personalizados deben implementarse utilizando tecnologías estándar o proporcionando información adicional para que las tecnologías de asistencia puedan interpretarlos correctamente. Por ejemplo, un botón personalizado debe comunicar que es un botón, su nombre o etiqueta, y su estado actual (presionado, desactivado, etc.). Estas prácticas benefician especialmente a personas que utilizan lectores de pantalla, magnificadores o control por voz, al permitirles comprender y operar todos los componentes de la interfaz.

## Caso

En la interfaz general de CompraFácil existe en la esquina superior izquierda del fondo una imagen decorativa (Blob) que no aporta información relevante al contenido. Sin embargo, esta imagen se ha implementado sin el atributo `alt=""` que la identificaría como puramente decorativa, lo que provoca que los lectores de pantalla la anuncien, mencionando su nombre de archivo o una descripción genérica.

Esta implementación incorrecta genera una experiencia confusa para usuarios de tecnologías asistivas, ya que reciben información irrelevante que interrumpe el flujo de navegación. Además, al no identificar correctamente el propósito (o la ausencia de propósito) de este elemento visual, se crea ruido innecesario en la interfaz auditiva, dificultando la comprensión general de la estructura y contenido relevante de la página.

## Solución

Es posible utilizar el parámetro `aria-hidden` para ocultar de los lectores de pantalla el elemento gráfico

```javascript
<img 
  src={blobSvg} aria-hidden="true" 
  className='w-80 h-80 md:h-108 md:w-108 lg:h-128 lg:w-128'/>
```

## Criterio de éxito

Toda la tecnología de asistencia hace uso de las propiedades de nombre, función y valor para identificar correctamente los elementos estandarizados de HTML. Cualquier componente personalizado también debe traer estas marcas de manera adecuada.

## Mas información

[Understanding SC 4.1.2: Name, Role, Value (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value)
