# Tetris (estilo Tetr.io) — Proyecto local

Pequeña implementación de Tetris en un único archivo HTML, con varias mejoras visuales y de jugabilidad inspiradas en Tetr.io. El proyecto está pensado para uso local (sin servidor) y es ideal para jugar, estudiar la lógica del juego o como base para mejoras.

## Características
- Tablero 10x20 con escala agrandada para mejor visibilidad.
- Randomizador de 7-bag (colas de piezas).
- Rotación con SRS simplificado y *kicks* básicos.
- Hold, cola de siguientes, ghost piece.
- DAS/ARR (auto repeat para desplazamiento lateral).
- Soft drop, hard drop y puntuación básica por líneas.
- Efectos: partículas al limpiar filas y sacudida de cámara cuando se limpian varias filas a la vez.
- Contador de combos (muestra cuántas limpiezas consecutivas se hacen).
- Soporte para reproducir música ambiente desde un enlace (URL) o fichero local.
- Imagen de fondo personalizada.

## Archivos importantes
- `tetr20.html` — Juego principal (todo en un solo archivo).

Si editas el proyecto o quieres usar los recursos incluidos, coloca los archivos en las rutas siguientes (opcional):
- `img/anime-bg.jpg` — imagen de fondo (si quieres una foto tipo anime detrás del juego).
- `audio/zen.mp3` — pista local por defecto (si no usas URL).

También puedes pegar cualquier enlace directo a un archivo de audio (por ejemplo, `https://.../mi-pista.mp3`) en la caja `Pegar enlace de audio` dentro de la interfaz y pulsar `Cargar`.

## Cómo ejecutar
1. Abre `tetr20.html` en tu navegador (doble clic o arrastra al navegador).
2. Pulsa `Start / Restart` para empezar la partida.
3. Usa la casilla `Música` y el campo de URL para activar música ambiente si lo deseas.

> Nota: por seguridad y políticas de los navegadores, la reproducción automática de audio puede estar bloqueada hasta que interactúes con la página (clic/tecla). Si no suena la música, pulsa `Start` o haz clic en la página y vuelve a intentarlo.

## Controles
- Mover: ← → (flechas izquierda/derecha)
- Rotar: `X` / `Z` / ↑ (flecha arriba también rota)
- Soft drop: ↓ (flecha abajo)
- Hard drop: `Space` (barra espaciadora)
- Hold: `C`
- Pause: `P` o `Esc`
- Enter: iniciar partida si no está corriendo

## Personalización rápida
- Cambiar tamaño de celda: en `tetr20.html` edita la constante `CELL` (valor por defecto: `48`).
- Cambiar fondo: reemplaza `img/anime-bg.jpg` o modifica la regla CSS `background` en la parte superior del archivo.
- Cambiar música por defecto: coloca un MP3 en `audio/zen.mp3` o pega otra URL en la caja correspondiente.

## Limitaciones y notas técnicas
- El archivo es una implementación ligera; la SRS y los *kicks* son simplificados.
- Reproducción de audio desde enlaces depende de CORS: algunos servidores no permiten reproducir archivos desde dominios externos.
- No hay sistema de guardado de partidas ni ranking en línea.

## Sugerencias de mejora
- Añadir controles de volumen y mute para la música ambiente.
- Guardar la URL de música en `localStorage` como preset.
- Implementar SRS completo y detección T-Spin más precisa.
- Añadir opciones responsive para pantallas pequeñas (escalado del canvas).

## Licencia
Usa este código libremente para fines personales o educativos. Si quieres que agregue una licencia formal (por ejemplo MIT), dímelo y la incluyo.
