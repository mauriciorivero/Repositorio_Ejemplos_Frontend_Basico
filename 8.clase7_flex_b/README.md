# Clase 7B - Flexbox: Barra de Navegación tipo LinkedIn

## Descripción
Este ejemplo demuestra cómo crear una barra de navegación horizontal estilo LinkedIn usando Flexbox, con logo, barra de búsqueda y menú de navegación.

## Archivos

### `index.html`
Header de navegación con dos secciones:

1. **Sección izquierda** (`encabezado_icon_search`):
   - Logo de LinkedIn
   - Barra de búsqueda con icono

2. **Sección derecha** (`encabezado-menu`):
   - Enlaces de navegación con iconos y texto:
     - Inicio
     - Mi Red
     - Empleos
     - Mensajes
     - Notificaciones

### `css/styles.css`
Estilos Flexbox para navegación:

```css
/* Header principal - distribución horizontal */
.encabezado1 {
    align-items: center;
    display: flex;
    justify-content: space-between;  /* Separa logo/búsqueda del menú */
    height: 10vh;
    padding: 0 10vw;
    width: 100%;
}

/* Sección logo + búsqueda */
.encabezado_icon_search {
    align-items: center;
    display: flex;
    width: 340px;
}

/* Barra de búsqueda */
.encabezado_icon_search > div {
    align-items: center;
    border: solid 1px gray;
    border-radius: 30px;
    display: flex;
    justify-content: flex-start;
    padding: 10px;
}

/* Menú de navegación */
.encabezado-menu {
    align-items: center;
    display: flex;
    justify-content: space-between;
    width: 420px;
}

/* Items del menú - flex vertical */
.encabezado-menu > a {
    align-items: center;
    display: flex;
    flex-direction: column;    /* Icono arriba, texto abajo */
    justify-content: center;
    text-decoration: none;
    width: 75px;
}
```

## Estructura de Carpetas
```
8.clase7_flex_b/
├── index.html
├── css/
│   └── styles.css
└── img/
    └── [iconos de navegación]
```

## Conceptos Aprendidos
- **Flexbox anidado**: Contenedores flex dentro de otros contenedores flex
- **justify-content: space-between**: Distribuye elementos con espacio máximo entre ellos
- **flex-direction: column**: Apila elementos verticalmente (para iconos con texto)
- **Unidades viewport**: `vh` (viewport height), `vw` (viewport width)
- **Estilos de input**: Remover bordes y outline
- **Border-radius**: Crear elementos redondeados
- **Estructura de navegación**: Patrón común en aplicaciones web modernas
