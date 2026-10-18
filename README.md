# CHALA DIET

Sitio web de **CHALA DIET**, una dietética online: *"Dietética Online al alcance de tu mano"*.

🔗 **Sitio desplegado:** https://juani-ai.github.io/ChalaDiet/

## Páginas

- **Inicio** (`index.html`): presentación, galería con carousel y producto destacado.
- **Sobre mí** (`pages/sobre-mi.html`): quiénes somos y nuestros valores.
- **Productos** (`pages/productos.html`): catálogo con grilla de productos.
- **Preguntas frecuentes** (`pages/preguntas-frecuentes.html`): dudas comunes en un accordion.
- **Contacto** (`pages/contacto.html`): medios de contacto y horarios.

## Tecnologías

- HTML5 semántico
- SCSS (variables, mixins con parámetros, @extend, operadores, partials y nesting) compilado a CSS
- CSS3 (Flexbox, CSS Grid y media queries)
- Bootstrap 5 por CDN (navbar, carousel y accordion)
- AOS por CDN (animaciones al hacer scroll)
- Google Fonts (Inter)

## Responsive

Las 5 páginas están adaptadas a mobile, tablet y desktop (mobile first):

- **Mobile:** navbar con menú hamburguesa y todo en una columna.
- **Tablet (desde 768px):** el catálogo pasa a 2 columnas.
- **Desktop (desde 1024px):** el catálogo pasa a 3 columnas, y el index, sobre mí y contacto se organizan en 2 columnas.

## Animaciones

- **Nativas (SCSS):** los títulos de cada página aparecen con un `@keyframes` (`aparecer`) aplicado con el mixin `animacion()`. Botones, links, tarjetas y carousel tienen `transition` en sus estados `:hover`, `:focus` y `:active`.
- **Librería AOS:** las secciones aparecen con `fade-up` al hacer scroll. Se inicializa en `js/main.js`.

## Estructura

```
├── index.html
├── README.md
├── package.json
├── assets/
├── js/
│   └── main.js
├── pages/
│   ├── sobre-mi.html
│   ├── productos.html
│   ├── preguntas-frecuentes.html
│   └── contacto.html
├── scss/
│   ├── main.scss
│   ├── utilities/
│   │   ├── _variables.scss
│   │   ├── _mixins.scss
│   │   └── _placeholders.scss
│   ├── base/
│   │   ├── _base.scss
│   │   └── _tipografia.scss
│   ├── layout/
│   │   ├── _header.scss
│   │   ├── _nav.scss
│   │   ├── _main.scss
│   │   └── _footer.scss
│   └── components/
│       ├── _buttons.scss
│       ├── _cards.scss
│       ├── _carousel.scss
│       ├── _listas.scss
│       └── _accordion.scss
└── styles/
    └── style.css   (generado por Sass, no se edita a mano)
```

## Cómo compilar los estilos

Los estilos se escriben en la carpeta `scss/` y `main.scss` es el único punto de entrada. Para generar `styles/style.css`:

```
npm install
npm run build
```

Para que se compile solo cada vez que guardo un cambio:

```
npm run sass
```

## Autor

Juan Ignacio Bressan