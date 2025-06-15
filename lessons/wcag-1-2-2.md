# WCAG 1.2.2: Anuncio con subtítulos

## Descripción

Este criterio de éxito busca garantizar que los contenidos pregrabados de solo audio incluyan alternativas textuales, como subtítulos o transcripciones, para que sean accesibles a personas con discapacidades auditivas.

Estas alternativas permiten que el contenido se perciba a través de diferentes modalidades sensoriales según las necesidades del usuario. Por ejemplo, los subtítulos pueden proporcionar una representación textual del diálogo y los sonidos importantes, mientras que las transcripciones detallan todo el contenido hablado y sonoro. Estas opciones benefician especialmente a personas con discapacidades auditivas, al ofrecer una forma paralela y accesible de entender el contenido.

## Caso

> El archivo con subtítulos se encuentra disponible dentro del código (Archivo con formato `.vtt`)

El anuncio de contenido audivisual se encuentra disponible dentro del sitio web pero este no cuenta con subtítulos. La omisión de este elemento impide que las personas usuarias con discapacidades auditivas no logren comprender este contenido ya que no pueden acceder a un contenido equivalente a lo escuchado.

## Solución

Añadir el respectivo archivo de subtítulos dentro del elemento `<video>`

```javascript
<track
  src={subtitlesUrl}
  kind="subtitles"
  srcLang="es"
  label="Español"
  default
/>
```

## Criterio de éxito

Cualquier contenido pregrabado que contenga una pista de audio (ya sea sólo de audio o video) debe tener subtítulos.

## Mas información

[Understanding SC 1.2.2: Captions (Prerecorded) (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/captions-prerecorded)
