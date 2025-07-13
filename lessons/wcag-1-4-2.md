# WCAG 1.4.2: Música al iniciar el sitio web

## Descripción

Este criterio de éxito busca garantizar que los usuarios puedan pausar, detener o ajustar el volumen del audio que se reproduce automáticamente en una página web.

Esto implica que cualquier contenido de audio que se reproduzca automáticamente durante más de tres segundos debe incluir controles accesibles para pausarlo o detenerlo. Por ejemplo, un video con audio que se inicia automáticamente debe tener un botón claramente visible para detener la reproducción. Estas prácticas benefician especialmente a personas con discapacidades auditivas o cognitivas, al evitar distracciones o dificultades para concentrarse en otros contenidos.

## Caso

Al entrar al sitio web dentro del catálogo de CompraFácil, una pieza músical inicia de manera automática con una duración de 30 segundos sin botón de pausa alguno disponible.

Que la música no pueda ser pausada puede significar que usuarios que utilizan lectores de pantalla encuentren díficil escuchar las instrucciones del mismo.

## Solución

Es posible crear un botón de reproducción que permita al usuario reproducir la pieza de música si lo desea. Es importante tener en cuenta que la música no debe de iniciar de manera automática sino que debe iniciar cuando el usuario lo permita

```javascript
import React, { useState, useRef } from 'react';
import { PlayCircle, StopCircle } from 'lucide-react'; // Import icons from lucide-react

const Music = () => {
  const [isPlaying, setIsPlaying] = useState(false); // Default state is "stop"
  const audioUrl = 'https://res.cloudinary.com/dao5kgzkm/video/upload/v1741316071/audio/backgroundMusic.mp3'
  const audioRef = useRef(new Audio(audioUrl)); // Reference to the audio file

  // Set the volume to 0.25 when the component is initialized
  audioRef.current.volume = 0.25;

  const toggleMusic = () => {
    if (isPlaying) {
      audioRef.current.pause(); // Pause the music
      audioRef.current.currentTime = 0; // Reset to the beginning
    } else {
      audioRef.current.play(); // Play the music
    }
    setIsPlaying(!isPlaying); // Toggle the state
  };

  return (
    <button
      onClick={toggleMusic}
      className="md:absolute top-28 bg-blue-dark text-white px-4 py-2 rounded hover:bg-blue-darkest flex items-center space-x-2"
    >
      {isPlaying ? (
        <>
          <StopCircle className="w-6 h-6" /> {/* Stop icon */}
          <span>Parar música</span>
        </>
      ) : (
        <>
          <PlayCircle className="w-6 h-6" /> {/* Play icon */}
          <span>Reproducir música</span>
        </>
      )}
    </button>
  );
};
export default Music;
```

## Criterio de éxito

Se debe proporcionar una forma sencilla de pausar, silenciar o ajustar el volumen de cualquier audio que se reproduzca automáticamente durante más de 3 segundos en la interfaz.

## Mas información

[Understanding SC 1.4.2: Audio Control (Level A)](https://www.w3.org/WAI/WCAG22/Understanding/audio-control)
