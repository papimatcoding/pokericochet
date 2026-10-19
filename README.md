# POKÉRICOCHET — Rogue Bounce v0.6

Versión jugable publicada mediante GitHub Pages, sin compilación. Mantiene los datos de colección y equipo de v0.5.

## Cambios principales

- Física anti-multigolpe: cada proyectil registra el contacto con cada bloque y se recoloca fuera de la colisión antes de rebotar. Un impacto tangencial no puede dañar repetidamente durante el solapamiento; volver a impactar tras rebotar es válido.
- Los **efectos secundarios** de cada bola se activan como máximo una vez por vuelo: salpicadura, perforación o cadena eléctrica. Una mejora del movimiento Eléctrico permite encadenar descargas a enemigos cercanos y respeta la inmunidad a Eléctrico.
- HUD enemigo limpio: números de PS y contador de ataque arriba a los lados, barra de PS fina abajo, sprite más grande en el centro.
- Enemigos con aproximadamente un 20-25 % menos de PS y ataques más peligrosos. El escalado sigue dependiendo de región y tipo de enemigo.
- Mapa con decisiones diferenciadas: duelo contra dos rivales reforzados, emboscada con rivales adelantados, lluvia que potencia Agua y debilita Fuego, fortaleza blindada y cacería con mejores probabilidades de Poké Ball (sin garantía). Los centros siguen limitados para evitar saltarse los combates.
- Seis reliquias globales nuevas con efectos reales, escogiendo entre categorías de ataque, defensa y utilidad. Incluyen rebotes potentes, conductividad eléctrica, curación por KOs, protección periódica y bonificación de supereficacia.
- Mismo guardado persistente; no se reinicia ninguna captura o progreso.

**Balance de prueba:** los nuevos valores requieren feedback sobre combates con uno y tres Pokémon.

Proyecto fan no oficial. Los sprites alojados en PokéAPI son públicamente accesibles, pero los derechos de los personajes y materiales siguen perteneciendo a sus respectivos titulares.
