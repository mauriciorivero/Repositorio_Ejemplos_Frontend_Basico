# Clase 8 Flex - Tienda de Productos con Flexbox

## Descripción
Este ejemplo demuestra la creación de una tienda de productos completa usando Flexbox, con header de navegación y galería de productos responsive. Incluye integración de Google Fonts.

## Archivos

### `index.html`
Estructura de tienda con:

1. **Header de navegación** (`encabezado`):
   - Logo de Shopify
   - Menú de navegación horizontal (Inicio, Productos, Servicios, Contacto)

2. **Galería de productos** (`contenido`):
   - 20 tarjetas de producto usando `<picture>`
   - Cada tarjeta contiene imagen y nombre del producto

3. **Google Fonts**:
   - Integración de la fuente "Inter" desde Google Fonts

### `css/styles.css`
Estilos completos de la tienda:

```css
/* Reset */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

/* Header con Flexbox */
.encabezado {
    align-items: center;
    background-color: blueviolet;
    display: flex;
    justify-content: space-between;
    height: 15vh;
    padding: 1% 5%;
    width: 100vw;
}

/* Menú de navegación horizontal */
.encabezado > nav > ul {
    display: flex;
    gap: 20px;
    list-style: none;
}

/* Estilos de enlaces */
.encabezado > nav > ul > li > a {
    color: white;
    font-family: "Inter", sans-serif;
    font-size: 26px;
    font-weight: 700;
    text-decoration: none;
}

/* Galería de productos */
.contenido {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    padding: 2% 5%;
}

/* Tarjetas de producto */
.contenido > picture {
    align-items: center;
    background-color: blueviolet;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    height: 400px;
    padding: 10px;
    width: 300px;
}
```

## Estructura de Carpetas
```
10.Clase_8_flex/
├── index.html
├── css/
│   └── styles.css
└── img/
    ├── shopify.png
    └── [20 imágenes de productos .webp]
```

## Conceptos Aprendidos

### Google Fonts
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:..." rel="stylesheet">
```
- `preconnect`: Optimiza la carga de fuentes externas
- Uso en CSS: `font-family: "Inter", sans-serif`

### Flexbox para Layout
- **Header**: `justify-content: space-between` para logo y menú
- **Menú**: `display: flex` con `gap` para espaciado
- **Galería**: `flex-wrap: wrap` para diseño responsive

### Elemento `<picture>`
- Contenedor semántico para imágenes con descripción
- Útil para galerías y catálogos de productos

### Unidades Responsive
- `vh` (viewport height): `15vh` para altura del header
- `vw` (viewport width): `100vw` para ancho completo
- `%`: Padding proporcional

### Diseño de Tarjetas
- `flex-direction: column`: Imagen arriba, texto abajo
- `border-radius`: Esquinas redondeadas
- Altura fija con contenido flexible
