# WCAG 1.3.2: Orden linear en lista de enlaces de la navbar

## Descripción

Este criterio de éxito busca garantizar que el contenido web sea presentado de manera significativa y comprensible, independientemente de la orientación o disposición visual del contenido.

Esto implica que la secuencia de lectura y el significado del contenido no dependan únicamente de su presentación visual. Por ejemplo, si un formulario tiene campos organizados en columnas, el orden lógico de los campos debe mantenerse incluso si se accede al contenido mediante un lector de pantalla. Estas prácticas benefician especialmente a personas con discapacidades visuales o cognitivas, al asegurar que puedan navegar y comprender el contenido sin confusión.

## Caso

Las barra de navegación de CompraFácil cuenta con una lista de enlaces que permite navegar por cada una de las secciones del aplicativo web. Lastimósamente al pasar por esta misma mediante la navegación del teclado (Usando la tecla tabuladora), esta es leída de derecha a izquierda, diferente al orden visual de los elementos que es de derecha a izquierda.

Esta discrepancia afecta a aquellos usuarios que dependen de tecnología asistida, ya que el orden no es presentado en el respectivo orden en que debería estar.

## Solución

Remover las propiedades `flex-row reverse` y `space-x-reverse` del elemento `<navbar>`  y organizar la lista de enlaces al orden correcto:

```javascript
<nav>
  <ul className='flex items-center space-x-4'>
    <li className='text-white text-xl'>
      <a href='/'>Catálogo</a>
    </li>
    <li className='text-white text-xl'>
      <a href='/blog'>Blog</a>
    </li>
    <li className='text-white text-xl'>
      <a href='assistance'>Ayuda</a>
    </li>
  </ul>
</nav >
```

## Criterio de éxito

Cualquiera que sea el método de interacción, la presentación de información en la pantalla siempre debe tener una secuencia lógica.

## Mas información

[Understanding SC 1.3.2: Meaningful Sequence (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/meaningful-sequence)
