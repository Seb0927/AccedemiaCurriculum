# WCAG 3.1.1: Declarar el idioma de la pantalla

## Descripción

Este criterio de éxito busca garantizar que el idioma principal de una página web esté claramente definido para que las tecnologías de asistencia puedan interpretarlo correctamente.

Esto implica que el atributo de idioma debe estar configurado en el código de la página. Por ejemplo, una página en español debe incluir el atributo `lang="es"` en la etiqueta `<html>`. Estas prácticas benefician especialmente a personas con discapacidades visuales o cognitivas, al permitir que los lectores de pantalla adapten su pronunciación y presentación del contenido.

## Caso

El sitio web de CompraFácil no declara el idioma del sitio usando el atributo `lang` en el elemento `<html>`. Esta omisión causa problemas significativos para los usuarios que utilizan lectores de pantalla, ya que estas herramientas necesitan conocer el idioma del contenido para aplicar las reglas de pronunciación adecuadas.

Sin esta información, el lector de pantalla puede intentar leer el contenido en español utilizando reglas fonéticas de otro idioma (generalmente inglés por defecto), resultando en una pronunciación incorrecta que dificulta o imposibilita la comprensión del contenido. También afecta a las herramientas de traducción automática y a las funciones de búsqueda específicas del idioma, creando barreras adicionales para usuarios internacionales o aquellos que dependen de estas tecnologías.

## Solución

Es necesario añadir el atributo `language` de la etiqueta `<html>` junto con el lenguaje del sitio web CompraFácil (En este caso, español (`es`)).

```javascript
<!doctype html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />

// [...]
```

## Criterio de éxito

Declarar correctamente el idioma de la pantalla hace que los lectores de pantalla usen una entonación correcta para citar el contenido. Declararlos siempre.

## Mas información

[Understanding SC 3.1.1: Language of Page (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/language-of-page)
