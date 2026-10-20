# POKÉRICOCHET · Rogue Bounce 0.8

Prototipo fan de Pokémon + rebotes con progresión roguelite, publicado directamente en GitHub Pages. HTML/CSS/JavaScript sin herramientas de compilación.

## Versión 0.8 — ritmo, tácticas y audio

### Estructura de expedición
- Menos interrupciones: los pisos de combate comienzan automáticamente sin abrir una pantalla de ruta y, al vencer, se avanza al siguiente. Solo eventos, decisiones de mejora y jefes requieren confirmación.
- Zonas de **6, 7, 8 y 8 pisos**, respectivamente, más un jefe. Cada encuentro normal incluye **3 oleadas**, los combates fuertes y jefes **4 oleadas**.
- Bonificación pequeña de recuperación entre oleadas para primeros equipos de un solo Pokémon.
- Al subir de nivel, la elección aparece **inmediatamente al terminar la ráfaga de proyectiles**, incluso a mitad de un piso; tras elegir, la ronda continúa.
- Poké Balls sin recoger permanecen hasta la siguiente oleada. Si queda alguna después de acabar la última oleada, hay una oportunidad adicional de apuntar y recogerla.

### Ataques y movimientos
- Movimientos iniciales y repertorios de aprendizaje distintos para los 27 iniciales, repartidos en físicos, especiales y de estado.
- **Drenadoras:** apuntar a fila o columna; 3 rondas de daño y recuperación limitada; inmune el tipo Planta.
- **Onda Trueno:** apuntar a fila o columna, retrasa a los enemigos; inmunidad de tipos Tierra y Eléctrico.
- **Pantalla Luz / Protección**, **Danza Espada / Desarrollo**, **Síntesis** y **Pantalla Humo** consumen una acción y proporcionan beneficios temporales.
- Efectos secundarios por movimiento: quemaduras de Ascuas/Giro Fuego, descargas en cadena con Impactrueno, efectos ralentizadores de Burbuja/Disparo Lodo, recuperación de Absorber y efectos especiales diferenciados en otros movimientos.
- **Un efecto secundario como máximo por bola**. Los proyectiles siguen rebotando y pueden realizar impactos posteriores.
- Los ataques especiales requieren **70 impactos acumulados** en vez de 20; el especial se prepara, apunta y dispara, y depende del movimiento seleccionado, no solo de su tipo.
- Habilidades como Torrente, Espesura y Mar Llamas avisan al cruzar el **50 % de PS**, umbral adaptado a este juego (en Pokémon principal activan con un tercio de PS).

### UI y tipos
- Pantalla principal completa, barra superior y HUD reforzados, selección de movimientos más clara y etiquetas para ambos tipos de amenaza enemiga: cuenta atrás a distancia y rondas hasta la zona de contacto.
- **Tabla completa de los 18 tipos** accesible mediante el botón **◈ TIPOS**, con tabla 18×18 y calculadora para Pokémon de uno o dos tipos (incluidas inmunidades y multiplicadores x4 / x0,25).
- Mejores opciones de subida de nivel: geometría letal, carga acelerada de especial, curación entre oleadas, escudo inicial y puntería crítica.

### Sonido
- Eliminada la música chiptune repetitiva en bucle.
- Los gritos de Pokémon se transmiten bajo demanda a volumen bajo desde los enlaces públicos de **[PokéAPI Cries](https://github.com/PokeAPI/cries)** al comenzar ciertos combates y hacer relevos. No se copian al repositorio. El audio depende del navegador y requiere activación desde el botón de sonido.
- Efectos sintéticos originales y más suaves, con límite de frecuencia para evitar acumulación de pitidos.
- Los gritos son materiales asociados a Pokémon: que se puedan consultar públicamente no equivale a una licencia libre de derechos ni garantiza autorización de uso. La música oficial de los videojuegos no se redistribuye.

## Guardado y controles
- Se conserva el guardado local anterior: colección, equipo configurado, caramelos, progreso permanente y gachapón. Las mejoras y niveles de una expedición se reinician en cada nueva partida.
- Ratón o dedo: apuntar arrastrando y disparar. Teclas 1–3: movimientos, espacio: disparar, F: pantalla completa en navegadores compatibles.
- Movimientos de estado: selecciona fila/columna cuando corresponda; pierdes el turno de disparo.
- Botón de especial: cuando esté cargado, púlsalo, apunta y dispara.

## Estado
Sistema todavía en desarrollo: faltan bastantes movimientos oficiales, más habilidades por especie, IVs/EVs y más pruebas de equilibrio y acabado visual en navegadores reales. El programa es un proyecto fan no oficial y Pokémon y sus personajes pertenecen a sus respectivos titulares.
