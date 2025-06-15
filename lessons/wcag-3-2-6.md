# WCAG 3.2.6: Botón de ayuda

## Descripción

Este criterio de éxito busca garantizar que los mecanismos de ayuda se presenten de manera consistente en todo el sitio web, facilitando que los usuarios puedan encontrar asistencia cuando la necesiten.

Esto implica que si se proporciona ayuda en una página, como información de contacto, formularios de asistencia o enlaces a FAQs, estos elementos deben aparecer en la misma ubicación y formato en todas las páginas donde estén disponibles. Estas prácticas benefician especialmente a personas con discapacidades cognitivas o de aprendizaje, al crear un patrón predecible que reduce la carga cognitiva y mejora la experiencia de usuario.

## Caso

Dentro de la barra de navegación, el enlace que redirige a la sección de ayuda solamente se encuentra disponible cuando el usuario se encuentra en la ruta raíz (`"/"`). Esta inconsistencia en la disponibilidad de la ayuda crea confusión significativa para los usuarios, especialmente aquellos con discapacidades cognitivas o de aprendizaje, que pueden haber memorizado la ubicación del enlace de ayuda en la página principal. 

Cuando navegan a otras secciones del sitio y necesitan asistencia, no encuentran el mecanismo de ayuda en la ubicación esperada, lo que aumenta su frustración y dificulta su capacidad para resolver problemas. Esta implementación contradice directamente el principio de consistencia y previsibilidad que facilita el uso efectivo de un sitio web, especialmente para usuarios con necesidades de accesibilidad.

## Solución

Es necesario eliminar el elemento `useEffect` que realiza una validación si el usuario se encuentra en la ruta raíz.

```javascript
import { useContext } from 'react'
import { UserContext } from '@/contexts/UserContext'
import shoppingCartSvg from '../../assets/vectors/shopping_cart.svg'

const Header = () => {
  const { user, setUser } = useContext(UserContext);

  const imageUrl = 'https://res.cloudinary.com/dao5kgzkm/image/upload/logo';

  const handleLogout = () => {
    setUser(null);
  };

  return (
    <header className='fixed bg-blue-darkest h-16 w-full z-50'>
      <div className='flex items-center h-full px-4 py-3 md:space-x-5'>
        <img crossOrigin='anonymous' src={imageUrl} alt='Logo de CompraFacil' className='h-full md:block hidden' />
        <span className='text-white text-xl font-bold md:block hidden'>CompraFácil</span>
        <hr className='h-full w-0.5 blue bg-white md:block hidden' />
        {/* Justification:
      https://www.w3.org/WAI/WCAG22/Techniques/aria/ARIA11.html */}
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
        </nav>
      </div>

      <div className='absolute right-0 top-0 h-full flex items-center px-4 py-3 space-x-5'>
        <a href="/payment/cart" className='h-full'>
          <img src={shoppingCartSvg} alt='Tu carrito de compras' className='h-full' />
        </a>

        {user ? (
          <button
            onClick={handleLogout}
            className='bg-blue-light h-full px-3 font-semibold text-lg rounded-md hover:bg-blue-medium-light'>
            Cerrar sesión
          </button>
        ) : (
          <a href='/login'
            className='flex items-center justify-center bg-blue-light h-full px-3 font-semibold text-lg rounded-md hover:bg-blue-medium-light'>
            Iniciar sesión
          </a>
        )}
      </div>
    </header>
  )
}

export default Header
```

## Criterio de éxito

Si se proporcionan algunas opciones de ayuda en una pantalla (ejemplo: datos de contacto humano), este mismo formato debe ser el mismo en todas las demás pantallas donde se proporciona ayuda.

## Mas información

[Understanding SC 3.2.6: Consistent Help (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/consistent-help.html)