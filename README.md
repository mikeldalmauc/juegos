# Juegos

Portada con mis juegos para el navegador, publicada con GitHub Pages:
https://mikeldalmauc.github.io/juegos/

HTML y CSS a pelo: sin dependencias ni paso de build. Lo que se sube a `main` se publica solo en un minuto.

## Qué hay y dónde vive cada juego

| Juego | Dónde se publica | De dónde sale |
|---|---|---|
| Tetris | `tetris/` de este repo | [tetris](https://github.com/mikeldalmauc/tetris), compilado |
| Buscaminas | `buscaminas/` de este repo | [buscaminas](https://github.com/mikeldalmauc/buscaminas) |
| Pasapalabra | su propio GitHub Pages | [pasapalabra](https://github.com/mikeldalmauc/pasapalabra) |
| Timeline | su propio GitHub Pages | [timeline-card-game](https://github.com/mikeldalmauc/timeline-card-game) |
| Ajedrez | su propio GitHub Pages | [chess-sala-interactiva](https://github.com/mikeldalmauc/chess-sala-interactiva) |
| Dixit | su propio GitHub Pages | [dixit-sala-interactiva](https://github.com/mikeldalmauc/dixit-sala-interactiva) |
| Guerra de píxeles | https://pixel-war.lamdera.app | `pixel-war` (Lamdera) |
| Archipiélago | sin publicar todavía | `archipielago` (Lamdera) |

Los que ya se publican solos se enlazan, no se copian: así cada uno se actualiza desde su repo.

## Añadir un juego

- **Si ya está publicado en otro sitio:** añade su tarjeta a `index.html` con la URL completa.
- **Si es estático y no tiene web propia:** cópialo a una carpeta (`nombre/index.html`, con rutas relativas, nunca `/assets/...`) y enlaza `nombre/`.

```html
<li><a href="nombre/"><strong>Nombre</strong><span>Una línea sobre el juego.</span></a></li>
```

## Actualizar tetris o buscaminas

Tetris (Elm; usa `Debug`, así que sin `--optimize`):

```sh
gh repo clone mikeldalmauc/tetris && cd tetris
lamdera make src/Main.elm --output=build/tetris.js   # o elm make
```

Copia `build/tetris.js` a `tetris/`. Si cambia `tetris.css`, cópialo pasando `/assets/` a `assets/`.

Buscaminas: copia `src/buscaminas.mjs` (pasando `'/assets/` a `'assets/`) y `build/confeti.js`.

## Probar en local

Buscaminas usa módulos de JavaScript, que no cargan desde `file://`. Sirve la carpeta:

```sh
python -m http.server 8000
```

y entra en http://localhost:8000.

Decisiones de código: `docs/DECISIONS.md`.
