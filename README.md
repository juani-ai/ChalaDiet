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
- SCSS (variables, mixins, partials y nesting) compilado a CSS
- CSS3 (Flexbox, CSS Grid y media queries)
- Bootstrap 5 por CDN (navbar, carousel y accordion)
- Google Fonts (Inter)

## Responsive

El index, productos y preguntas frecuentes están adaptados a mobile, tablet y desktop:

- **Mobile:** navbar con menú hamburguesa y todo en una columna.
- **Tablet (desde 768px):** el catálogo pasa a 2 columnas.
- **Desktop (desde 1024px):** el catálogo pasa a 3 columnas y el index se organiza en 2 columnas.

## Estructura

```
├── index.html
├── README.md
├── package.json
├── assets/
├── pages/
│   ├── sobre-mi.html
│   ├── productos.html
│   ├── preguntas-frecuentes.html
│   └── contacto.html
├── scss/
│   ├── main.scss
│   ├── utilities/
│   │   ├── _variables.scss
│   │   └── _mixins.scss
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