# Fundamentos WEB - Equipo 03 (Grupo 4303A)

Mini sitio web de tres páginas HTML5 sobre **Computación cuántica**, desarrollado de forma colaborativa con Git y GitHub. Las tres páginas comparten una hoja de estilos externa (`css/styles.css`); no usa JavaScript.

## Integrantes

* Cristian Andrés Revelo
* Beken Carabali Palacios

## Tema y subtemas

Tema general: Computación cuántica.

1. Principios generales (`index.html`)
2. Avances recientes (`tema2.html`)
3. Aplicaciones potenciales (`tema3.html`)

## Distribución del trabajo

Cristian: Principios generales (`index.html`) y primera parte de Aplicaciones potenciales
Beken: Avances recientes (`tema2.html`) y segunda parte de Aplicaciones potenciales

## Revisión cruzada (Tarea II)

* Estudiante 1 revisó `tema2.html`: se corrigió un enlace roto hacia `tema3.html` y se mejoró el texto alternativo de la imagen.
* Estudiante 2 revisó `index.html`: se propuso y agregó la sección "Limitaciones y mitos frecuentes".

## Validación HTML

Validador utilizado: https://validator.w3.org/

### Página 1 (`index.html`)

Errores encontrados:
-Ninguno

### Página 2 (`tema2.html`)

Errores encontrados:
-Ninhuno

### Página 3 (`tema3.html`)

Errores encontrados:
-Ninguno

## Convención CSS

- Idioma de clases: inglés
- Formato: kebab-case
- Componentes: BEM cuando aplica (`block__element`, `block--modifier`), por ejemplo `site-header__title` y `main-nav__link--active`

## Paleta de color

- Primary: `#16213e`
- Secondary: `#4b3f8f`
- Accent: `#0b6b76`
- Background: `#f5f6fb`
- Surface: `#ffffff`
- Text: `#1c2130`

Justificación: el tema es computación cuántica, así que elegimos un azul profundo como color principal para transmitir seriedad tecnológica y académica, un violeta como secundario para reforzar el carácter "cuántico" sin caer en tonos neón, y un cian oscuro como acento para diferenciar enlaces y estados interactivos sin competir con el resto del contenido.

Contraste verificado con una calculadora de contraste WCAG (referencia AA = 4.5:1 para texto normal):
- Texto sobre fondo: 14.86:1
- Texto sobre superficie: 16.04:1
- Blanco sobre primary: 15.89:1
- Blanco sobre secondary: 8.73:1
- Accent sobre superficie: 6.22:1

Todos superan el mínimo exigido.

## Revisión cruzada (Tarea de CSS)

* Beken revisó `index.html`: la clase de la introducción del encabezado se llamaba `.texto-grande` (nombre visual). Se renombró a `site-header__intro` según la convención acordada.
* Cristian revisó `tema2.html` y `tema3.html`: confirmó que ambas enlazan el mismo `css/styles.css`, que la navegación mantiene subrayado en `hover`/`focus` además del cambio de color, y que las tablas y enlaces conservan buen contraste.

## Prueba de cascada

Se realizó sobre un `<h2>` de prueba con `id="demo-title"` y `class="demo-title"` en una copia temporal de `tema2.html`, retirada después del experimento.

- Resultado del selector de elemento (`h2 { color: blue; }`): azul.
- Resultado de la clase (`.demo-title { color: green; }`): verde. La clase tiene mayor especificidad que el selector de elemento.
- Resultado del ID (`#demo-title { color: purple; }`): morado. El ID tiene mayor especificidad que la clase.
- Resultado del estilo en línea (`style="color: orange;"`): naranja. El estilo en línea prevalece sobre las reglas normales de la hoja de estilos.

Explicación: cada paso ganó porque aumentó la especificidad frente al anterior (elemento < clase < ID < en línea); el orden de las reglas en el archivo no decidió el resultado porque las especificidades eran distintas en cada comparación. El código de la prueba (el `id`, la clase `demo-title` y el `style` en línea) fue retirado del archivo final; en el sitio solo queda esta documentación y las clases con nombre semántico.
