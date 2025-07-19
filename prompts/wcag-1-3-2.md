# Información

- Título de la lección: WCAG 1.3.2: Orden linear en lista de enlaces de la navbar
- Criterio de éxito a evaluar: 1.3.2: Meaningful Sequence (Level A)
- Situación incorrecta: La lista de enlaces de la barra de navegación al ser navegada por medio del teclado, va de derecha a izquierda.
- Situacion correcta: La lista de enlaces de la barra de navegación al ser navegada por medio del teclado, va de izquierda a derecha.
- Pieza de código inaccessible:

```javascript
<nav>
  <ul className='flex flex-row-reverse items-center space-x-4 space-x-reverse'>
    <li className='text-white text-xl'>
      <a href='assistance'>Ayuda</a>
    </li>
    <li className='text-white text-xl'>
      <a href='/blog'>Blog</a>
    </li>
    <li className='text-white text-xl'>
      <a href='/'>Catálogo</a>
    </li>
  </ul>   
</nav>
```

- Solución brindada por el estudiante:
