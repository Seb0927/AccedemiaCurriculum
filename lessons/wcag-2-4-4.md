# WCAG 2.4.4: "Leer mas" sobre noticias

## Descripción

Este criterio de éxito busca garantizar que los enlaces en una página web sean descriptivos y proporcionen suficiente información sobre su destino o propósito.

Esto implica que los textos de los enlaces deben ser claros y específicos, evitando frases genéricas como "haz clic aquí". Por ejemplo, un enlace a una página de contacto debe decir "Contáctanos" en lugar de algo ambiguo. Estas prácticas benefician especialmente a personas con discapacidades visuales o cognitivas, al facilitar la navegación y comprensión del contenido.

## Caso

Al encontrarse dentro de la sección de Blog donde se pueden encontrar los posts publicados, cada una de las pre-visualizaciones de las publicaciones solamente contienen un hipervínculo con la leyenda "Leer más". Esta práctica genera problemas significativos para usuarios que utilizan tecnologías de asistencia, ya que cuando un lector de pantalla enumera todos los enlaces de la página, se encuentran con múltiples enlaces que dicen simplemente "Leer más" sin contexto adicional.

Esto hace imposible distinguir entre las diferentes publicaciones sin tener que navegar al contenido circundante, resultando en una experiencia frustrante e ineficiente para comprender el propósito específico de cada enlace.

## Solución

Cada pre-visualización a las publicaciones del blog debe de contener una entrada al contenido textual de la publicación acompañado del respectivo hipervínculo con la leyenda "Leer más".

```javascript
<h2 className='text-2xl font-bold mb-2'>{title}</h2>
<p className='text-lg mb-4'>{getSubstring(content, 150)}</p>
<a
  title={'Leer más sobre ' + title}
  href={'/blog/post' + (id + 1)}
  className='flex items-center justify-center h-9 w-28 bg-blue-dark text-white text-xl mt-3 hover:bg-blue-darkest'>Leer más</a>
```

## Criterio de éxito

El propósito de un enlace debe determinarse a partir del texto del propio enlace o del contexto que lo rodea.

## Mas información

[Understanding SC 2.4.4: Link Purpose (In Context) (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/link-purpose-in-context)
