# Clase 8 - CSS Grid: Layout Avanzado

## Descripción
Este ejemplo demuestra el uso de CSS Grid para crear layouts complejos con elementos que ocupan múltiples filas y columnas, combinado con Flexbox para elementos internos.

## Archivos

### `index.html`
Grid de 7 elementos con diferentes configuraciones:
- **Caja 1**: Ocupa 2 filas (span)
- **Cajas 2, 3**: Tamaño normal
- **Caja 5**: Ocupa 2 columnas y contiene un grid interno de 8 elementos
- **Caja 6**: Ocupa 2 columnas
- **Caja 7**: Tamaño normal

### `css/styles.css`
Estilos Grid completos:

```css
/* Reset */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

/* Centrado del body con Flexbox */
body {
    align-items: center;
    display: flex;
    justify-content: center;
    height: 100vh;
    width: 100vw;
}

/* Contenedor Grid principal */
.contenedor-principal {
    display: grid;
    grid-template-columns: 200px 200px 200px;  /* 3 columnas de 200px */
    grid-template-rows: 200px 200px 200px;     /* 3 filas de 200px */
    column-gap: 30px;
    row-gap: 30px;
    transform: rotate(30deg);  /* Efecto visual de rotación */
}

/* Caja que ocupa 2 filas */
#caja1 {
    background-color: orange;
    grid-row: span 2;          /* Ocupa 2 filas */
    height: 430px;             /* Altura ajustada (200+200+30 gap) */
}

/* Caja que ocupa 2 columnas con Flexbox interno */
#caja5 {
    background-color: red;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 10px;
    grid-column: span 2;       /* Ocupa 2 columnas */
    width: 430px;
}

/* Caja que ocupa 2 columnas */
#caja6 {
    background-color: violet;
    grid-column: span 2;
    width: 430px;
}
```

## Estructura de Carpetas
```
10.Clase8_Grid/
├── index.html
└── css/
    └── styles.css
```

## Conceptos Aprendidos

### CSS Grid
- **`display: grid`**: Activa el modo grid
- **`grid-template-columns`**: Define el número y tamaño de columnas
- **`grid-template-rows`**: Define el número y tamaño de filas
- **`column-gap` / `row-gap`**: Espaciado entre celdas
- **`grid-row: span 2`**: Elemento ocupa 2 filas
- **`grid-column: span 2`**: Elemento ocupa 2 columnas

### Combinación Grid + Flexbox
- El contenedor principal usa Grid
- Los elementos internos (como #caja5) usan Flexbox para su contenido

### Transform
- `transform: rotate(30deg)` aplica una rotación visual al grid completo

## Visualización del Grid
```
┌─────────┬─────────┬─────────┐
│         │    2    │    3    │
│    1    ├─────────┴─────────┤
│ (span2) │         5         │
│         │      (span2)      │
├─────────┼───────────────────┤
│         │                   │
│    6    │         7         │
│ (span2) │                   │
└─────────┴───────────────────┘
```
