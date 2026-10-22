# POKÉRICOCHET 0.9 — Expedition Edition

[▶ Jugar en GitHub Pages](https://papimatcoding.github.io/the-last-menagerie/?v=0.9.0)

Juego fan roguelite de Pokémon y rebotes, en HTML/CSS/JavaScript sin servidor ni compilación.

## Nueva experiencia en la 0.9

**Tablero continuo:** desaparecen las oleadas. Un encuentro normal genera **15 filas** de enemigos (18 en jefes), tres iniciales y una fila nueva cada turno, bajando hacia la zona de contacto. Algunas filas son **hordas** completas. El combate nunca se reinicia entre filas. La arena tiene siete columnas que llenan la anchura física; se han reducido los huecos junto a las paredes.

**Rutas:** cuatro zonas con 4, 5, 5 y 6 pisos respectivamente más sus jefes. El avance sigue siendo lineal con encuentros aleatorios. Hay campamentos en pisos seleccionados y Centros Pokémon durante la expedición.

**Estadísticas oficiales:** el archivo separado `pokemon-data.js` integra las estadísticas base, recompensas EV, habilidades y requisitos evolutivos de PokéAPI; las estadísticas se calculan con nivel, IVs, EVs y naturaleza. Fórmulas habituales de Pokémon para seis estadísticas, adaptando el daño final al sistema multigolpe de rebotes.

**IVs y EVs:** cada captura o cápsula revela seis IVs (0–31). Los mejores valores **por atributo y familia** se guardan permanentemente y se aplican a nuevas expediciones. Los EVs se ganan derrotando especies concretas y se reinician al comienzo de cada run, con límites de 252 por estadística y 510 en total. Naturalezas persistentes por familia. La nueva ficha de Pokémon (botón **▤ FICHA**) muestra estadísticas, base, IVs, EVs, naturaleza, habilidad, objeto y próxima evolución.

**Evoluciones reales:** evoluciones por nivel desde los datos de Pokémon, sin bonificaciones arbitrarias. Piedras, enlaces de intercambio y otras condiciones se adaptan mediante objetos escasos; nunca se ofrece un objeto evolutivo en tienda si nadie del equipo puede usarlo. Una evolución conserva IVs, EVs, nivel y movimientos. Nueva animación de transformación.

**Pokétienda y campamentos:** Pokédólares de expedición (₽), obtenidos derrotando rivales; no son las fichas permanentes del gachapón. En campamentos hay objetos de curación, bayas, objetos equipables (Carbón, Agua Mística, Restos, Mineral Evol, etc.) y una probabilidad baja (**13 % por visita, si hay un Pokémon compatible**) de ofrecer un objeto evolutivo. Descanso y entrenamiento EV están limitados a una vez por campamento. Las monedas no se venden ni se compran con dinero real.

**Movimientos:** aprendizaje automático de repertorio según el nivel: durante la partida se consultan los datos de movimientos por nivel de **Escarlata/Púrpura** en PokéAPI y se guardan localmente por especie. Los efectos actualmente jugables cubren un subconjunto de movimientos y existe un repertorio de respaldo si el servicio no responde o esa especie no tiene datos de novena generación. Las mejoras al subir de nivel se aplican al movimiento aprendido o al Pokémon: Fuego, Agua, Planta, Eléctrico y movimientos de estado tienen opciones específicas, además de recompensas generales.

**Habilidades:** se muestra únicamente el nombre cuando se activan. Las habilidades oficiales aparecen en la ficha; ya hay una selección de efectos programados y opciones de habilidad oculta desbloqueable con caramelos. No todas las habilidades oficiales tienen efecto adaptado todavía.

**Arte e interfaz:** nueva hoja `v09.css`, estilo de expedición y mejoras de la arena y HUD, campamentos visuales, tarjetas de objetos con sprites, evolución animada y tabla de tipos ampliada para escritorio y móvil. Los sprites del juego se sirven desde los recursos públicos de PokéAPI, y los gritos opcionales desde PokéAPI Cries.

## Controles

Apunta arrastrando con el ratón o el dedo y suelta para disparar. Teclas 1–3: seleccionar movimiento; espacio: disparar; F: pantalla completa (según el navegador). El especial se prepara con su botón cuando está cargado. **◈ TIPOS** abre la tabla de enfrentamientos y **▤ FICHA** muestra estadísticas y entrenamientos.

## Guardado y compatibilidad

Se sigue usando `pokeRicochet-v04` en el almacenamiento local del navegador. Se mantienen las capturas, caramelos, monedas de cápsulas y equipo preparado de la versión anterior. El esquema se amplía sin borrarlo. Los IVs obtenidos a partir de ahora se guardan en `ivBest`; si no hay IVs previos se parte de valores neutrales de 10. Las expediciones nuevas empiezan al nivel 5, pero conservan las mejoras permanentes.

## Fuentes, derechos y límites

- [PokéAPI](https://pokeapi.co/) y [datos CSV públicos](https://github.com/PokeAPI/pokeapi/tree/master/data/v2/csv): estadísticas, tipos, evolución, habilidades y datos de nivel. El código de PokéAPI tiene licencia BSD-3-Clause (ver `THIRD_PARTY_NOTICES.md`).
- [PokéAPI Sprites](https://github.com/PokeAPI/sprites): imágenes remotas de Pokémon, objetos y tipos.
- [PokéAPI Cries](https://github.com/PokeAPI/cries): gritos remotos opcionales a bajo volumen.

**Proyecto fan no oficial.** Pokémon y los personajes, sprites y sonidos asociados pertenecen a sus titulares. Que los recursos estén disponibles en internet no los convierte en contenido libre de derechos. No hay monetización.

El juego continúa siendo un prototipo: falta implementar todos los movimientos, habilidades, formas y condiciones evolutivas, así como más pruebas visuales y de balance en navegadores reales. Los datos referenciados se seleccionan con Escarlata/Púrpura como generación objetivo; se usan alternativas compatibles cuando esa versión no tiene información.


## Cambios de la rama 1.1 — dominantes, balance y móvil

Esta rama continúa el juego original, sin cambiar la clave de guardado pokeRicochet-v04 ni borrar la colección.

- Director de dificultad: primeras rondas más ligeras; la dificultad crece después.
- Dominantes: minijefes alfa con habilidades propias. Teracristalización defensiva ocasional; Llovizna, Sequía, Chorro Arena o Nevada solo si el Pokémon tiene esa habilidad. Ya no se lanza clima aleatorio por piso.
- Jefes: Mega-Beedrill, Mega-Gengar, Mega-Gyarados y Charizard Gigamax con presentación diferenciada. Los sprites de formas alternativas se intentan cargar, conservando los originales si fallan.
- Velocidad: recuperación gradual de energía especial por impactos, sin disparar la velocidad física de la bola. Nuevas mejoras de ritmo y rebote.
- Física: rescate de trayectorias horizontales y recuperación de ráfagas bloqueadas.
- Gachapón: tickets x1, tiradas x10 con tickets acumulados, tickets x10 poco frecuentes y conversión de los fragmentos heredados.
- PC: ordenación por IVs, caramelos, estadísticas base, shinies y nombre; búsqueda, detalle individual y caramelos por especie.
- Móvil: menús compactos, estadísticas en una columna y acciones secundarias plegables.

### Pruebas pendientes

Se ha validado la sintaxis del script completo. Falta comprobar manualmente partidas enteras en navegador y móvil, el balance final, las formas especiales disponibles, y los guardados antiguos. Rama de revisión: no sustituye main hasta pasar las pruebas.