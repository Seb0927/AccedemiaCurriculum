# WCAG 2.1.4: Shortcut para carrito de compras

## Descripción

Este criterio de éxito busca garantizar que cualquier atajo de teclado que use una sola tecla (incluidas letras, números y caracteres de puntuación) pueda ser desactivado, reconfigurado o sólo se active cuando el componente correspondiente tenga el foco.

Esto implica que los atajos de teclado de una sola tecla no deben interferir con la capacidad de los usuarios para usar el teclado para navegar o interactuar con la página. Por ejemplo, una aplicación web puede ofrecer atajos de teclado para funciones comunes, pero debe permitir que estos sean personalizados o desactivados. Estas prácticas benefician especialmente a personas que usan tecnologías de asistencia o que tienen limitaciones motoras, al evitar activaciones accidentales de funciones mientras navegan.

## Caso

Dentro del catálogo existe un atajo de teclado que permite redireccionar al carrito de compras al presionar la tecla "C". Este atajo se activa en cualquier momento mientras se navega por el sitio, sin importar dónde esté el foco y sin opción para desactivarlo o reconfigurarlo.

Esta implementación causa problemas a usuarios que utilizan tecnologías de asistencia como lectores de pantalla o software de reconocimiento de voz, ya que pueden activar accidentalmente el atajo mientras intentan escribir o navegar, interrumpiendo inesperadamente su experiencia y causando confusión.

## Solución

Se puede modificar el atajo de tal manera que no interrumpa con funcionalidades del sistema (Por ejemplo, utilizando dos teclas) o simplemente eliminar el atajo y sus referencias dentro del catálogo. En este caso se elimina:

```javascript
import React from 'react'
import Item from './Item';
import products from '@/utils/products';
import { ShoppingCartProvider } from '../../contexts/ShoppingCartContext';
import Music from './Music';

const Catalog = () => {
  console.log(localStorage.getItem('shopping_cart'))
  return (
    <section>
      <div className='flex flex-col items-center md:items-start mb-4 md:mb-0'>
        <Music />
      </div>
      { /*(Section) Justification:
    https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section#usage_notes */}
      <h1 className='text-6xl text-blue-darkest pb-8 text-center font-bold'>Catálogo</h1>
      {/* ¿Why not ul-li tags? TL;DR: Think a list as you always do, short elements and that's it
    https://stackoverflow.com/questions/16213214/is-it-a-good-practice-to-put-articles-inside-lis
    Posdata: Actually, there is a debate: https://stackoverflow.com/questions/19307443/semantic-html-of-an-articles-list */}
      <div className='grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-8'>
        <ShoppingCartProvider>
          {products.map((product, index) => (
            <Item
              key={index}
              title={product.title}
              price={product.price}
              description={product.description}
              images={product.images}
            />
          ))}
        </ShoppingCartProvider>
      </div>
    </section>
  )
}
export default Catalog
```

## Criterio de éxito

Debe evitarse la creación de atajos de teclado utilizando solo caracteres simples (por ejemplo: letras o números) que pueden entrar en conflicto con los atajos existentes en el sistema. Si esto ocurre, se deben cumplir ciertas condiciones (consulte los criterios completos).

## Mas información

[Understanding SC 2.1.4: Character Key Shortcuts (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/character-key-shortcuts)
