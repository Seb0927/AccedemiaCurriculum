# Información

- Título de la lección: 2.4.4: "Leer mas" sobre noticias
- Criterio de éxito a evaluar: WCAG 2.4.4: Link Purpose (In Context) (Level A)
- Situación incorrecta: Cada pre-visualización a cada una de las publicaciones en el blog solamente contiene un hipervínculo con la leyenda "Leer más"
- Situacion correcta: Cada pre-visualización a cada una de las publicaciones en el blog contiene una entrada al contenido textual de la publicación acompañado con un hipervínculo con la leyenda "Leer más"
- Pieza de código inaccessible:

```javascript
<a
// No contiene elemento title
href={'/blog/post' + (id + 1)}
className='flex items-center justify-center h-9 w-28 bg-blue-dark text-white text-xl mt-3 hover:bg-blue-darkest'>Leer más</a>
```

- Solución brindada por el estudiante:
