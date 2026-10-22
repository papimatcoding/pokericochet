# POKÉRICOCHET 1.3 — Expedition Edition

[▶ Jugar en GitHub Pages](https://papimatcoding.github.io/pokericochet/?v=1.3.0)

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

## Versión 1.2 — Animaciones de jefes y máquina cápsula

- **Navegación de escritorio:** se corrige el solape del logotipo con el contenido reservando un carril izquierdo suficientemente ancho, también a resoluciones intermedias. La pantalla móvil mantiene navegación horizontal.
- **Gachapón animado:** máquina de cápsulas, giro, bolas agitándose y salida de una Poké Ball según rareza: Poké Ball (común), Super Ball (poco común), Ultra Ball (rara) y Master Ball (extraordinaria). Son indicadores visuales, no objetos obtenidos. Las diez tiradas generan diez recompensas y al menos una poco común o superior. **Las cápsulas nunca contienen especies evolucionadas, megas ni Gigamax**; duplicados siguen dando caramelos.
- **Entradas de jefes:** escena corta con nombre grande, categoría de Mega o Gigamax y sprite GIF animado de Pokémon Showdown, con sprite estándar de reserva si el GIF falla. Inicio automático o mediante el botón visible.
- **Jefes con reglas:** Mega-Gengar usa Sombra Trampa para impedir relevos mientras permanezca vivo; los jefes ganan una segunda fase a mitad de PS, y Gigamax Charizard puede causar daño residual en esa segunda fase.
- **Persistencia:** se respeta la colección y su clave local `pokeRicochet-v04` y las mejoras/fragmentos del sistema previo.

**Estado:** el script del juego pasa revisión de sintaxis JavaScript. Las animaciones y el balance todavía requieren validación manual visual y partidas completas, sobre todo en dispositivos móviles. Los sprites remotos requieren conexión a internet; se mantienen imágenes de reserva cuando fallan.


## Versión 1.3 — Primer parche de progresión y combos

Continuación del motor original. Se conserva la clave de guardado `pokeRicochet-v04` y la colección, los IVs, caramelos, tickets y objetos adquiridos anteriormente.

### Ritmo de combate
- Encuentros corrientes: 9 filas en la primera región, 10 en la segunda y 11 en las restantes. Variantes raras: 11; hordas y élites: 12; dominantes: 13; jefes: 16.
- La vida de Pokémon corrientes baja suavemente (más al principio); no se debilitan dominantes ni jefes. Daño enemigo moderado en los pisos iniciales.
- Cada dos victorias de combate normal los Pokémon vivos recuperan un 8 % de sus PS. No hay curación adicional en dominantes ni jefes.

### Mejoras más contundentes
- Entrenamientos ofensivos: +2 daño por nivel en su categoría; +7 PS y +10 de curación en mejora de PS; Defensa también añade PS; Ráfaga mejora la potencia y añade una bola.
- Crítico y afinidad de tipo reforzados; nuevo par de especializaciones orientadas a combos y carga del especial.
- Rarezas reajustadas a 48 % común, 32 % poco común, 14 % raro, 5 % épico y 1 % legendario. Las opciones siguen filtradas por compatibilidad y nivel máximo.

### Combos incrementales por ráfaga
- Cuentan los impactos que efectivamente hacen daño (no las inmunidades ni los choques vacíos).
- Escalones ×5 / ×12 / ×20 / ×35 aumentan el daño progresivamente hasta un máximo del 26 % base; Maestría del Ricochet puede elevar el total al 35 %.
- Pequeñas bonificaciones de energía, Pokédólares limitados por ráfaga, efectos visuales y contador encima del tablero. Un combo empieza de nuevo en cada lanzamiento.

### Misiones y estadísticas
- Los retos voluntarios ya no endurecen al enemigo. Piden una ráfaga de 8 impactos en las dos primeras regiones o 12 en las siguientes, en el próximo combate; si se consigue se obtienen ₽25 y 3 fragmentos de ticket, sin castigo al fallar.
- Al finalizar la partida se muestra un resumen de turnos, impactos, daño directo registrado, récord de combos, capturas, KOs, dominantes, jefes y contribución de cada integrante. El informe se conserva en el historial del menú.

### Verificaciones
- Sintaxis del JavaScript completo comprobada.
- Las pruebas de partidas enteras y revisión visual a distintas resoluciones están pendientes. No se modifican los guardados persistentes existentes.

### Siguiente parche propuesto
- Rutas verdaderamente diferenciadas, mejoras y movimientos más específicos de cada especie, y jefes con patrones más refinados.