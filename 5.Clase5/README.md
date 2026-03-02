# Clase 5 - Selectores CSS y Modelo de Caja

## Descripción
Este ejemplo demuestra el uso de selectores CSS avanzados, el modelo de caja y estilos para crear una página de noticias.

## Archivos

### `index.html`
Página de artículo de noticias con:
- **Estructura semántica**: `<header>`, `<main>`, `<footer>`
- **Clases CSS**: `header-principal`, `contenido-principal`, `titulo-noticia`
- **Imagen externa**: Carga de imagen desde URL
- **Elemento `<span>`**: Para resaltar texto específico dentro del título

### `css/styles-app.css`
Hoja de estilos con selectores avanzados:

```css
/* Selector de clase */
.contenido-principal {
    padding-left: 250px;
    padding-right: 250px;
    width: 750px;
}

/* Selector hijo directo (>) */
.contenido-principal > img {
    border-radius: 20px;
    box-shadow: 5px 5px 0px rgba(0, 0, 0, 1);
    margin-bottom: 50px;
    width: 500px;
}

/* Selector de clase con propiedades de borde */
.titulo-noticia {
    border-left: 5px solid red;
    font-size: 40px;
    font-weight: 300;
    padding-left: 20px;
}

/* Selector hijo directo dentro de clase */
.titulo-noticia > span {
    font-weight: 900;
}
```

## Estructura de Carpetas
```
5.Clase5/
├── index.html
├── css/
│   └── styles-app.css
└── img/
```

## Conceptos Aprendidos
- **Selector hijo directo (`>`)**: Selecciona solo hijos directos, no descendientes
- **Modelo de caja**: padding, margin, width
- **Propiedades de borde**: border-left, border-radius
- **Box-shadow**: Sombras en elementos
- **Font-weight**: Control del grosor de la fuente
- **Uso de `<span>`**: Para aplicar estilos a partes específicas del texto
- **Imágenes externas**: Carga de imágenes desde URLs
