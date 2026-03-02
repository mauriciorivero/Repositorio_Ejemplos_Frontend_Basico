# Clase 4 - Introducción a CSS

## Descripción
Este ejemplo introduce los conceptos básicos de CSS, incluyendo hojas de estilo externas, estilos internos y selectores.

## Archivos

### `index.html`
Página principal que demuestra:
- **Enlace a CSS externo**: `<link rel="stylesheet" href="css/styles.css">`
- **Navegación**: Lista desordenada con enlaces
- **Contenido**: Múltiples títulos y párrafos para demostrar estilos

### `contacto.html`
Página de contacto que demuestra:
- **CSS externo**: Mismo archivo de estilos que index.html
- **CSS interno**: Estilos dentro de `<style>` en el `<head>` que sobrescriben los externos
  ```css
  h1 {
      color: purple;
  }
  ```
- **Cascada CSS**: El color purple del CSS interno tiene prioridad sobre el red del CSS externo

### `css/styles.css`
Hoja de estilos externa con:

```css
/* Selector de elemento */
h1 {
    color: red;
    font-size: 40px;
    font-family: sans-serif;
}

p {
    color: darkgray;
    font-size: 17px;
    width: 600px;
}

/* Selector de clase */
.titulo1 {
    color: pink;
}
```

## Estructura de Carpetas
```
4.Clase4/
├── index.html
├── contacto.html
└── css/
    └── styles.css
```

## Conceptos Aprendidos
- **Tres formas de aplicar CSS**:
  1. CSS externo (archivo .css)
  2. CSS interno (etiqueta `<style>`)
  3. CSS inline (atributo style - no mostrado aquí)
- **Selectores**: De elemento (`h1`, `p`) y de clase (`.titulo1`)
- **Propiedades CSS básicas**: color, font-size, font-family, width
- **Cascada y especificidad**: Los estilos internos sobrescriben los externos
- **Navegación entre páginas** con estilos consistentes
