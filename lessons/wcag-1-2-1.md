# WCAG 1.2.1: Entrevista del blog con transcripción

## Descripción

Este criterio de éxito busca garantizar que los contenidos pregrabados que combinan audio y video sean accesibles para todas las personas mediante alternativas como audiodescripciones o transcripciones textuales.

Estas alternativas permiten que el contenido audiovisual se perciba a través de diferentes modalidades sensoriales según las necesidades del usuario. Por ejemplo, una audiodescripción puede narrar elementos visuales clave durante las pausas naturales del diálogo, mientras que una transcripción textual puede detallar tanto el diálogo como las acciones visuales importantes. Estas opciones benefician especialmente a personas con discapacidades visuales o auditivas, al ofrecer una forma paralela y accesible de entender el contenido.

## Caso

El contenido audivisual se encuentra recientemente añadido al sitio web por lo que no cuenta aún con subtítulos, pero se encuentra presente dentro del código una transcripción del mismo el cual no se encuentra dentro del sitio. La omisión de esta transcripción impide que las personas usuarias con discapacidades auditivas no logren comprender este contenido ya que no pueden acceder a un contenido equivalente a lo escuchado.

## Solución

Añadir la respectiva transcripción de la entrevista

```javascript
{/* Transcripción de la entrevista */}
<h4 className='text-2xl font-semibold mb-4'>Transcripción</h4>
{transcriptParagraphs.map((paragraph, index) => (
  <p key={index} className='text-base mb-4'>
    {paragraph}
  </p>
))}
```

## Criterio de éxito

Se debe proporcionar una de las siguientes alternativas para el contenido presentado:

- Sólo audio: proporcione transcripción de texto descriptivo
- Sólo video: proporcione una transcripción de texto descriptivo y / o una pista descriptiva de audio que se pueda habilitar

## Mas información

[Understanding SC 1.2.1: Audio-only and Video-only (Prerecorded) (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/audio-only-and-video-only-prerecorded)
