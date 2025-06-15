# WCAG 2.1.2: Trampa de teclado en un producto

## Descripción

Este criterio de éxito busca garantizar que los usuarios puedan detener o desactivar cualquier funcionalidad que se active automáticamente al presionar una tecla.

Esto implica que las acciones activadas por teclas específicas deben ser configurables o desactivables para evitar activaciones accidentales. Por ejemplo, si una página utiliza la tecla "Espacio" para iniciar un video, también debe permitir que los usuarios desactiven esta funcionalidad. Estas prácticas benefician especialmente a personas con discapacidades motoras o cognitivas, al evitar interacciones no deseadas y mejorar la experiencia de uso.

## Caso

Dentro de la sección del carrito de compras, mientras el usuario se encuentra navegando mediante el enfoque de elementos (Utilizando la tecla tabuladora), al entrar a los elementos interactuables de un producto tales como la cantidad, imágen, entre otros, el enfoque quedará atrapado en este mismo dentro de los botones de cantidad.

Este inconveniente impide que usuarios que dependen del usuo del teclado, tales como personas ciegas o con discapacidades motrices, puedan navegar la interfaz de manera libre.

## Solución

Eliminar el hook `useEffect` que impide que el enfoque avance hacia los demás elementos interactuables de la interfaz junto con los demás elementos relacionados a la trampa de teclado

```javascript
import { useContext } from 'react'
import { ShoppingCartContext } from '@/contexts/ShoppingCartContext'
import { Plus, Minus } from 'lucide-react';

const Item = (props) => {
  const { product } = props;

  const { removeFromCart, incrementQuantity, decrementQuantity } = useContext(ShoppingCartContext);
  const imageUrl = 'https://res.cloudinary.com/dao5kgzkm/image/upload/v1741316071/Clothing/';

  // Calculate total for this item
  const formattedTotal = new Intl.NumberFormat('es-CO', {
    style: 'currency',
    currency: 'COP',
    minimumFractionDigits: 0,
  }).format(product.price * product.quantity);

  return (
    <div className='flex flex-row w-full space-x-6 items-center py-4 border-b-2 border-black first:border-t-2'>
      {/* Product image */}
      <img
        src={imageUrl + product.images[0]}
        alt={product.description || `Imagen de ${product.title}`}
        className='w-24 h-24 aspect-square object-cover rounded-sm'
      />

      {/* Product title */}
      <div className='flex-1'>
        <h3 className='text-lg'>{product.title}</h3>
      </div>

      {/* Quantity controls */}
      <div className='flex flex-row items-center space-x-4 flex-1 justify-center'>
        <button
          onClick={() => decrementQuantity(product.title)}
          className='bg-blue-dark text-white h-min w-min p-1 hover:bg-blue-darkest'
          aria-label={`Disminuir cantidad de ${product.title}`}
        >
          <Minus className='h-4 w-4 fill-white' />
        </button>

        <span className='text-xl' aria-label={`Cantidad: ${product.quantity}`}>
          {product.quantity}
        </span>

        <button
          onClick={() => incrementQuantity(product.title)}
          className='bg-blue-dark text-white h-min w-min p-1 hover:bg-blue-darkest'
          aria-label={`Aumentar cantidad de ${product.title}`}
        >
          <Plus className='h-4 w-4 fill-white' />
        </button>
      </div>

      {/* Price information */}
      <div className='flex-1 text-center'>
        <p className='text-lg'>
          {formattedTotal}
        </p>
      </div>

      {/* Remove button */}
      <div className='flex-1 text-right'>
        <button
          onClick={() => removeFromCart(product.title)}
          className='bg-blue-dark text-white py-2 px-4 hover:bg-blue-darkest'
          aria-label={`Eliminar ${product.title} del carrito`}>
          Eliminar
        </button>
      </div>
    </div>
  )
}

export default Item
```

## Criterio de éxito

Al interactuar a través del teclado, la navegación a través de todos los elementos en los que se puede hacer clic debe ocurrir sin ningún bloqueo o interrupción.

## Mas información

[Understanding SC 2.1.2: No Keyboard Trap (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/no-keyboard-trap)
