# METÁFORA 404

Interfaz hacker viva para performance poético-digital.

> El lenguaje puede convertirse en maleza indomable o someterse a la poda de quien intenta delimitar sus posibilidades. Pero incluso lo que ha sido cuidadosamente esculpido conserva la posibilidad de desbordar su forma.

## Qué hace

1. **Arranque**: lluvia de caracteres, hexdump en vivo y un syslog que registra la "poda" del lenguaje.
2. **Manifiesto**: la frase se descifra letra por letra.
3. **`pessoa.exe`**: se abre una ventana con un fragmento del *Libro del desasosiego* (Fernando Pessoa / Bernardo Soares).
4. **`libertad.sys`**: aparece la definición de libertad como *infinita posibilidad de equivocarse*.
5. **Modo autónomo**: la máquina sigue viva.
   - Las letras de "desbordar su forma" se escapan y caen.
   - "equivocarse" se equivoca sola.
   - Aparecen y desaparecen ventanas de heterónimos apócrifos (`caeiro.exe`, `reis.exe`, `campos.exe`…).
   - El hexdump esconde palabras; las ventanas tienen glitches espontáneos.

## Controles

| Acción | Cómo |
|---|---|
| Activar sonido | botón **♪ activar sonido** (el navegador exige un clic) |
| Reiniciar la secuencia | botón **↻ reiniciar secuencia** |
| Mover ventanas | arrastrar desde la barra de título (en escritorio) |
| Pantalla completa | `F11` en el navegador |

En celular las ventanas se apilan verticalmente.

## Ver en local

Abre `index.html` en cualquier navegador moderno. No necesita servidor ni instalación.

## Publicar con GitHub Pages

1. Sube el contenido de esta carpeta a un repositorio (por ejemplo `metafora-404`).
2. En el repositorio: **Settings → Pages → Build and deployment**.
3. En **Source** elige **Deploy from a branch**, rama `main`, carpeta `/ (root)` y guarda.
4. En uno o dos minutos estará en `https://TU-USUARIO.github.io/metafora-404/`.

## Personalizar

Todo está en `index.html`:

- **Textos principales**: constantes `F1`, `F2` y `F3` en el `<script>`.
- **Ventanas de heterónimos**: el arreglo `GHOSTS` (`[nombre, color, frase]`; color puede ser `''`, `'cy'`, `'mg'` o `'am'`).
- **Mensajes del syslog ambiental**: el arreglo `AMB`.
- **Palabras ocultas del hexdump**: el arreglo `HIDDEN` (8 caracteres cada una).
- **Velocidad de escritura**: el tercer argumento de cada llamada a `type(...)` (milisegundos por letra).
- **Título**: la imagen `titulo.png`.

## Estructura

```
metafora-404/
├── index.html        # toda la interfaz (HTML + CSS + JS)
├── titulo.png        # título METÁFORA 404
└── README.md
```

## Créditos

- Fragmento de `pessoa.exe`: Fernando Pessoa (como Bernardo Soares), *Libro del desasosiego*.
- Las frases de las ventanas de heterónimos son apócrifas, escritas para esta pieza.
- Tipografías: [Chakra Petch](https://fonts.google.com/specimen/Chakra+Petch) y [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) vía Google Fonts.
