# RICOCHET · v1.2

Juego arcade de rebotes, creado en HTML/CSS/JavaScript sin dependencias externas.

## Jugar

https://papimatcoding.github.io/the-last-menagerie/

El navegador siempre intenta encajar el tablero completo, el marcador y los botones en el alto visible, tanto en móvil como en ordenador, sin desplazar la página. Para ampliar utiliza «⛶ PANTALLA» o la tecla F; el mismo botón permite salir del modo pantalla completa.

1. Arrastra sobre el tablero para apuntar.
2. Suelta para disparar la ráfaga. Cada bola resta vida a los bloques.
3. Recoge los orbes dorados para añadir una bola a la siguiente ronda.
4. Cuando termina la ráfaga, los bloques **descienden animados** y aparece una fila nueva.
5. Si llegan al límite rojo, la partida termina.

El récord se almacena únicamente en el navegador (`localStorage`). Puedes acelerar una ráfaga con «RÁPIDO x3» y activar el audio opcionalmente.

## Pruebas

Se comprobó en Chromium con distintos tamaños de ventana, desde 320×480 hasta 1920×1080, sin desbordamiento del documento ni controles fuera de pantalla. Probados lanzamiento, descenso entre rondas, reinicio y activación/desactivación de pantalla completa.

## Futuro

La base está preparada para evolucionar hacia una variante inspirada en monstruos de bolsillo: equipo de tres combatientes, ataques únicos que generan proyectiles, enemigos capaces de atacar cada ronda, jefes, capturas y recompensas de elección múltiple. Se debatirá el diseño antes de implementarlo.
