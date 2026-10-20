# POKÉRICOCHET · Rogue Bounce 0.7

Juego fan experimental de rebotes con progresión roguelite, hecho en HTML, CSS y JavaScript, servido mediante GitHub Pages.

## Novedades de la 0.7

- **Menú a pantalla completa:** cuartel con navegación lateral en escritorio y pestañas horizontales en móvil; selección inaugural de un solo Pokémon y equipo de hasta tres en expediciones posteriores. Se conserva el guardado.
- **Ruta preestablecida:** no hay que elegir bifurcaciones. Cada piso tiene un encuentro pre-generado aleatorio, con presentación y vista previa de los siguientes pisos. Se mantienen centros, combates especiales, tesoros, élites y jefe de la zona. Las paradas pacíficas están separadas.
- **Clima visible y jugable:** lluvia con gotas (Agua mejor, Fuego peor), sol intenso (Fuego mejor, Agua peor), arena y nieve con partículas; bonificaciones moderadas para tipos adecuados.
- **Activación de habilidades:** carteles y etiqueta visible del Pokémon activo para Espesura, Mar Llamas, Torrente, Intimidación, Clorofila, Robustez y Electricidad Estática, según la especie y condición. Más habilidades oficiales quedan pendientes.
- **Tablero compacto:** menor espacio entre bloques, sprites grandes e indicadores pequeños en las esquinas, conservando física anti-grazing y un efecto especial máximo por bola.
- **Especial apuntable:** pulsar el botón prepara el movimiento, y luego se apunta arrastrando o usando el disparador. Algunos movimientos reconocibles ya tienen efectos propios: Ascuas (salpicadura), Pistola Agua (perforación), Impactrueno (cadena), Látigo Cepa (recuperación al eliminar rivales). Otros usan un especial reforzado provisional. Requiere 20 impactos para cargar.
- **Música y efectos:** temas chiptune **originales**, compuestos mediante WebAudio en tiempo real para menú y combate, con arpegios de victoria, niveles, gachapón y especiales. Se activan/desactivan desde el icono de audio. No se distribuyen grabaciones oficiales extraídas de Pokémon.

## Controles

Ratón o dedo: arrastrar y soltar para apuntar/disparar. Teclas 1–3: movimientos, espacio: disparo, F: pantalla completa (en navegadores compatibles). Para el especial, primero pulsar su botón (con la barra llena), y luego apuntar.

## Guardado

La partida persistente sigue usando el guardado anterior de v0.4/v0.5/v0.6: colección, caramelos y progreso no se reinician por esta actualización. Niveles y mejoras dentro de la expedición se reinician al comenzar una nueva run.

## Estado y propiedad intelectual

Versión de prototipo: balance y animaciones requieren pruebas completas en navegadores y dispositivos reales. No existe integración de música o efectos oficiales sin permiso; las melodías son originales. Los sprites de personajes accesibles a través de PokéAPI no están necesariamente bajo licencia libre y Pokémon pertenece a sus respectivos titulares.
