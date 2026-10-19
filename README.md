# PokéRicochet — prototipo 0.2

Minijuego fan de rebotes y progresión roguelite en una página HTML (sin compilación). Publicado en la raíz del repositorio con GitHub Pages. Proyecto experimental no oficial.

## Cambios de la 0.2

- Menú de preparación: eliges el líder y las dos reservas entre las especies capturadas. Solo uno combate a la vez. Admite shiny en el equipo inicial.
- Gachapón persistente que cuesta 4 fichas; empiezas con 8 fichas y puedes ganar más superando salas (se conserva con las capturas). Los Pokémon obtenidos van a la colección permanente.
- Al empezar una expedición, cada Pokémon está a nivel 5 y tiene **un único movimiento**. Al subir de nivel elige entre tres mejoras individuales variables, como aprender un movimiento, aumento de proyectiles, potencia, vida, críticos, salpicadura de área, taladro o escudos.
- Reliquias globales aleatorias cada tercera **victoria en combate** (los eventos que no implican combate no cuentan): ataque, proyectiles, curación, resistencia, XP extra, crítico, eco, monedas, captura y relevo.
- Repartir Exp. 60/20/20 entre el activo y sus dos reservas vivas (se redistribuye cuando hay bajas). Cada enemigo derrotado otorga experiencia según piso, rareza y categoría, con umbrales crecientes.
- Enemigos con más PS al avanzar, más pisos por zona (Bosque 12 + jefe, Cueva 14 + jefe, Costa 16 + jefe, Cumbre 14 + jefe), y una mayor variedad de caminos: combate normal, horda, encuentro raro, élite, Centro Pokémon, descanso y alijo.
- Ataques a distancia con cuenta atrás **✦ N** sobre el enemigo (número de turnos que faltan), proyectiles animados y daño aplicado al llegar al Pokémon. Los atacantes cuerpo a cuerpo indican **↓ N** (turnos aproximados hasta alcanzar la parte inferior). Las filas siguen descendiendo con suavidad.
- Pokémon activo con sprite y nombre en el punto de lanzamiento, además del perfil y la barra de PS. PS iniciales y protección de relevo aumentados para que el jugador pueda recuperarse tras una baja.
- Poké Balls menos frecuentes para las especies normales, según rareza. Shiny natural 1/4096; si derrotas a uno, suelta Poké Ball al 100%, pero aún debes tocarla con un proyectil.
- Se mantiene la tabla de 18 tipos, ventajas y resistencias. Centros Pokémon con curación y PC. Pantalla completa, sonido opcional y velocidad ×3. El juego y los controles caben en tamaños habituales de portátil y móvil.

## Estado y limitaciones

Este es un prototipo funcional con números **provisionales**; queda por pulir el balance con partidas reales. Aún no incluye evoluciones, toda la Pokédex, animaciones de ataques específicas para cada especie, movimientos de estado o un mapa ramificado permanente de nodos conectados. El gachapón es una colección simple, no una economía comercial ni un sistema de micropagos. El HTML depende de sprites remotos con fallback a iconos si no se cargan.

Los sprites se cargan desde [PokeAPI/sprites](https://github.com/PokeAPI/sprites), pero la accesibilidad pública de un sprite no equivale a licencia libre de uso. Pokémon y sus personajes son de sus titulares. Este proyecto fan no está asociado a Nintendo, Game Freak ni The Pokémon Company.