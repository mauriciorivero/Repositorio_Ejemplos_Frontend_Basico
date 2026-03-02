# Clase 7 - Flexbox: Catálogo de Productos

## Descripción
Este ejemplo demuestra el uso de CSS Flexbox para crear un catálogo de productos responsive con tarjetas de producto estilizadas.

## Archivos

### `index.html`
Catálogo de productos con:
- **Contenedor flex**: `<section class="products-list">`
- **Tarjetas de producto**: Cada `<div>` contiene:
  - Imagen del producto
  - Nombre (h2)
  - Precio (p)
  - Botón "Add to cart"
  - Badge de descuento (span)

### `css/styles.css`
Estilos Flexbox completos:

```css
/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Contenedor flex principal */
.products-list {
    align-items: flex-start;
    display: flex;
    flex-wrap: wrap;           /* Permite que los items salten de línea */
    justify-content: space-between;
    padding: 5% 10%;
}

/* Tarjetas de producto (también son flex) */
.products-list > div {
    align-items: center;
    background-color: #FF3EAA;
    border-radius: 20px;
    display: flex;
    flex-direction: column;    /* Elementos apilados verticalmente */
    justify-content: flex-start;
    gap: 10px;                 /* Espacio entre elementos */
    margin-bottom: 20px;
    padding: 5px;
    position: relative;        /* Para posicionar el badge */
    width: 300px;
}

/* Badge de descuento con posición absoluta */
.products-list > div > span {
    background-color: red;
    border-radius: 10px;
    position: absolute;
    right: -20px;
    top: 10px;
    transform: rotate(45deg);  /* Rotación del badge */
}
```

## Estructura de Carpetas
```
7.Clase7_Flex/
├── index.html
├── css/
│   └── styles.css
└── img/
    └── [imágenes de productos]
```

## Conceptos Aprendidos
- **Flexbox Container**: `display: flex`
- **Dirección**: `flex-direction: column`
- **Wrap**: `flex-wrap: wrap` para diseño responsive
- **Alineación**: `justify-content`, `align-items`
- **Gap**: Espaciado entre elementos flex
- **Position relative/absolute**: Para badges y elementos superpuestos
- **Transform rotate**: Rotación de elementos
- **Reset CSS**: Normalización de estilos por defecto
- **Box-sizing**: `border-box` para cálculos de tamaño más intuitivos
