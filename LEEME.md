# LEGADO — Primer prototipo jugable para iPhone

Esta es una versión inicial, original y funcional de un simulador de carrera futbolística para el navegador del teléfono. No es un juego 3D ni contiene los cientos de competiciones, licencias y animaciones de un videojuego comercial. Los clubes se usan como referencia textual; escudos y otros contenidos gráficos son originales y simplificados.

## Jugar ahora

Abrí `index.html` desde un servidor web. En computadora se puede ejecutar un servidor local desde esta misma carpeta:

```bash
python -m http.server 8000
```

Abrí http://localhost:8000 en el navegador.

## Publicar como app en el iPhone

1. Creá un repositorio en GitHub (por ejemplo `legado`).
2. Subí **todos** los archivos de esta carpeta a la raíz del repositorio, manteniendo los nombres.
3. En GitHub: Settings → Pages → Deploy from a branch → main → / (root) → Save.
4. Al publicarse, abrí en Safari `https://TU_USUARIO.github.io/legado/`.
5. Tocá Compartir → Agregar a pantalla de inicio → Agregar.
6. Abrí LEGADO desde el ícono de inicio. GitHub Pages ya ofrece HTTPS, necesario para el modo instalable y el guardado sin conexión.

Nota: algunos navegadores no permiten instalar una PWA desde un archivo local. Usá una URL HTTPS para la experiencia completa.

## Funciones de esta versión

- Crear futbolista, elegir posición y uno de 20 clubes argentinos.
- Partidas independientes: semilla aleatoria distinta, resultados simulados para todos los equipos, clasificación en vivo, calendario de 19 fechas.
- Partidos 2D interactivos en vertical con joystick, pases, remates, cambio de jugador, compañeros y rivales automáticos, marcador y cronómetro acelerado.
- Simulación rápida de partidos, progreso de atributos, descanso, energía, forma, confianza e hinchas.
- Noticias y decisiones dinámicas con consecuencias, ofertas de transferencia que pueden aparecer, contratos y salarios.
- Historial de resultados, campeones, estadísticas personales y temporadas consecutivas.
- Guardado automático en el mismo dispositivo con `localStorage` más exportación e importación manual de la partida en JSON.
- App instalable: manifiesto, iconos, service worker con copia de recursos para uso sin conexión después de la primera carga.

## Controles

- iPhone: joystick táctil izquierdo, botones CAMBIO, PASE y TIRO. El partido dura aproximadamente 79 segundos reales (90 minutos simulados).
- Computadora: flechas o WASD para moverte, Q para pasar, E para cambiar y espacio para rematar.

## Limitaciones actuales / próximos desarrollos

- Es un **prototipo 2D**, no tiene un motor 3D estilo FIFA, físicas avanzadas, animaciones esqueléticas ni multijugador.
- Hay una liga argentina simplificada de una sola rueda; no están implementadas copas continentales, selecciones nacionales, ascensos, descensos o calendarios internacionales.
- Los compañeros usan comportamientos sencillos, sin IA táctica avanzada. El mercado y los eventos son una primera base, no el sistema definitivo.
- El modo entrenador, la vida personal expandida, el teléfono social interno, entrenamientos jugables y sistemas narrativos de cientos de eventos quedan para siguientes versiones.
- Los datos se guardan en el navegador de ese dispositivo. Borrar los datos del sitio puede borrar la partida; exportá el JSON para hacer copia de seguridad.
