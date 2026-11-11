# Juegos

Página sencilla con juegos para el navegador, publicada con GitHub Pages:
https://mikeldalmauc.github.io/juegos/

HTML, CSS y JS a pelo: sin dependencias ni paso de build. Lo que se sube a `main` se publica solo en un minuto.

## Añadir un juego

1. Crea una carpeta con el nombre del juego y su `index.html` dentro (p. ej. `tetris/index.html`).
2. Añade su tarjeta a la lista de `index.html`:

   ```html
   <li><a href="tetris/"><strong>Tetris</strong><span>Una línea sobre el juego.</span></a></li>
   ```

3. `git push`. Queda en `https://mikeldalmauc.github.io/juegos/tetris/`.

## Probar en local

Abre `index.html` en el navegador o, si un juego carga ficheros, sirve la carpeta:

```sh
python -m http.server 8000
```

y entra en http://localhost:8000.

Decisiones de código: `docs/DECISIONS.md`.
