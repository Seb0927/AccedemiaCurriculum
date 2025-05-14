# WCAG 1.1.1: Texto alternativo de productos

## Descripción

Este criterio de éxito busca garantizar que la información en contenidos pregrabados de solo audio o solo video sea accesible para todas las personas mediante alternativas basadas en texto.

Estas alternativas permiten que el contenido se perciba a través de diferentes modalidades sensoriales según las necesidades del usuario. Por ejemplo, una película muda puede ser acompañada por una transcripción que describa lo que se ve, y un video puede tener una pista de audio equivalente. Estas opciones benefician especialmente a personas con discapacidades visuales, cognitivas, del lenguaje o del aprendizaje, al ofrecer una forma paralela y accesible de entender el contenido.

## Caso

La lista de productos del catálogo contienen un contenido visual cuyas imágenes no se acompañadas de un texto alternativo. . Esta omisión impide que las personas usuarias con discapacidades visuales comprendan el contenido visual, ya que los lectores de pantalla no pueden interpretar imágenes sin descripciones textuales.

## Solución

Para cumplir con el criterio WCAG 1.1.1, es necesario añadir un texto alternativo (`alt`) descriptivo a cada imagen de producto. Este atributo permite que tecnologías de asistencia, como los lectores de pantalla, transmitan el significado de las imágenes a los usuarios con discapacidades visuales.

```html
<!-- Situación incorrecta -->
<img src="camisa.jpg">

<!-- Situación correcta -->
<img src="camisa.jpg" alt="Camisa de algodón azul de manga larga">
```

## Criterio de éxito

Todo contenido no textual que se presenta al usuario tiene una alternativa en texto que cumple el mismo propósito, excepto en las situaciones que se enumeran a continuación.

## Mas información

- [Understanding Success Criterion 1.1.1: Non-text Content](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html)