# Decisiones

## D-01 · Web estática en GitHub Pages, sin build (11/11/2026)
HTML y CSS a pelo, publicados desde la raíz de `main`. Así no hay nada que instalar ni que compilar, y basta con un `git push` para publicar. El repo es público porque GitHub Pages en la cuenta gratuita solo publica repos públicos.

## D-02 · Enlazar lo publicado, copiar solo lo que no tiene web (11/11/2026)
Pasapalabra, Timeline, Ajedrez y Dixit ya tienen su propio GitHub Pages: la portada los enlaza y cada uno se sigue actualizando desde su repo. Guerra de píxeles y Archipiélago son Lamdera (necesitan backend), así que viven en `*.lamdera.app`. Tetris y Buscaminas no tenían web y sus repos llevan quietos desde 2023: se copian a su carpeta aquí (Tetris ya compilado) en vez de montarles un GitHub Pages con compilación de Elm a cada uno. Si se vuelven a tocar, se copian otra vez (pasos en el README).

## D-03 · Rutas relativas en los juegos copiados (11/11/2026)
Los originales pedían `/assets/...`, que en GitHub Pages apunta a la raíz del dominio (`mikeldalmauc.github.io/assets/`) y no a la carpeta del juego. En la copia van como `assets/...`.

## D-04 · Buscaminas sin jQuery (11/11/2026)
El HTML original cargaba jQuery de un CDN, pero el código no lo usa. Fuera, para no depender de un tercero.

## D-05 · Cada juego pone su color y su icono (11/11/2026)
Mikel pidió iconos y color. La página es neutra (gris claro u oscuro, sin acento) y cada tarjeta es un campo del color de su juego, sacado del propio juego: el azul del «1» de Buscaminas, el verde del tablero de Ajedrez, el navy del rosco, el marrón de Timeline, el dorado de Dixit, el mar de Archipiélago. Los iconos están dibujados en SVG con esos colores (el de Ajedrez es su propio favicon). Sin bordes ni sombras; texto blanco u oscuro según el contraste. Sin fotos ni vídeo, para que siga siendo sencilla.
