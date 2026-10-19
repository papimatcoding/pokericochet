# PokéRicochet — prototipo 0.1

Prototipo fan, sin ánimo comercial, creado como evolución de **RICOCHET**. Aventura roguelite de rebotes, Pokémon y capturas en HTML/CSS/JavaScript sin compilación. Entra desde la raíz de GitHub Pages.

## Cómo jugar

- Equipo de tres Pokémon, solo uno activo. Si cae, entra el siguiente con protección de relevo; si caen los tres, termina la expedición.
- Arrastra sobre el tablero para apuntar y suelta, o selecciona ataque y pulsa **Disparar**. Todos los Pokémon tienen ataques con un número de proyectiles y potencia propios.
- Cada enemigo derrotado da experiencia. Con **Repartir Exp.** activo se reparte 60 % al Pokémon activo y 20 % a cada reserva (si hay bajas, se redistribuye entre supervivientes).
- Cada subida de nivel permite mejorar **solo ese Pokémon** (+bolas para el ataque seleccionado, +potencia o +PS). Cada tres pisos hay mejora global.
- Se aplican los 18 tipos, resistencias, inmunidades y ventaja ×2 (×4 en dobles debilidades), con un pequeño bono por ataque del mismo tipo.
- Cada zona propone elecciones de ruta: combate, horda, rastro raro o Centro Pokémon ocasional. El primer bosque tiene 9 pisos y jefe; otras zonas tienen 7, 11 y 9 pisos y jefe.
- Los enemigos de tipo lanzador atacan tras los disparos del jugador. Todos pueden atacar cuerpo a cuerpo al alcanzar la parte inferior del tablero. Descienden con animación.
- Cuando derrotas a un Pokémon enemigo, puede dejar caer una Poké Ball con probabilidad dependiente de su especie. Debes **tocarla con una bola disparada** antes de que desaparezca para capturarlo. Shiny: 1/4096 de aparición, suelta Poké Ball al 100 %, pero también hay que recogerla.
- Las capturas se almacenan persistentemente (localStorage). En los Centros Pokémon se cura todo el equipo y se puede consultar el PC e intercambiar Pokémon; los del PC se ajustan aproximadamente al nivel medio del equipo.
- Los niveles y mejoras se reinician en cada expedición; la colección capturada se conserva.
- Botones de pantalla completa, sonido opcional y velocidad de animación ×1/×3. Los controles se ajustan a portátil y móvil.

## Estado de desarrollo

Es **una vertical slice**, no un juego terminado. Aún faltan evoluciones, movimientos de estado, estadísticas particulares por especie, escenarios persistentes complejos, rutas conectadas entre pisos, desafíos más completos, animaciones de captura elaboradas, balance extensivo y variedad de jefes y recompensas.

Para equilibrio inicial, se empieza a nivel 5; el umbral de experiencia para el siguiente nivel es `72 + 26 × (nivel - 5) + 2 × (nivel - 5)^2`. Cada bloque normal otorga cerca de 13–23 XP antes del reparto. Estos valores deberán ajustarse con sesiones reales de juego.

Los sprites se cargan desde [PokeAPI/sprites](https://github.com/PokeAPI/sprites) (hay elementos de reserva si no se cargan). Los personajes e imágenes de Pokémon son propiedad de sus titulares respectivos; que los sprites estén publicados en un repositorio accesible no implica que sean de libre explotación o redistribución. Proyecto fan experimental, no oficial ni afiliado a Nintendo, Game Freak o The Pokémon Company.
