# Clase 6 - Posicionamiento CSS (Position Fixed)

## Descripción
Este ejemplo demuestra el uso de `position: fixed` para crear un encabezado fijo que permanece visible al hacer scroll.

## Archivos

### `index.html`
Página con contenido extenso que incluye:
- **Header con clase**: `encabezado-1` para aplicar posicionamiento fijo
- **Párrafo con clase**: `parrafo1` con padding superior para compensar el header fijo
- **Múltiples párrafos**: Contenido largo para demostrar el efecto del scroll

### `css/styles.css`
Estilos de posicionamiento:

```css
/* Header fijo */
.encabezado-1 {
    background-color: black;
    height: 200px;
    position: fixed;    /* Fija el elemento en la ventana */
    width: 100%;        /* Ocupa todo el ancho */
}

/* Estilos del título dentro del header */
.encabezado-1 h1 {
    color: white;
    text-align: center;
    padding-top: 100px;
}

/* Compensación para el contenido */
.parrafo1 {
    padding-top: 250px;  /* Evita que el contenido quede detrás del header */
    text-align: center;
}
```

## Estructura de Carpetas
```
6.Clase6/
├── index.html
└── css/
    └── styles.css
```

## Conceptos Aprendidos
- **`position: fixed`**: El elemento se posiciona relativo a la ventana del navegador
- **Compensación de contenido**: Uso de padding-top para evitar que el contenido quede oculto detrás del header fijo
- **`width: 100%`**: Hacer que un elemento ocupe todo el ancho disponible
- **Selector descendiente**: `.encabezado-1 h1` selecciona h1 dentro de encabezado-1
- **Centrado de texto**: `text-align: center`
- **Colores de fondo**: `background-color`

## Comportamiento
1. El header negro permanece fijo en la parte superior
2. Al hacer scroll, el contenido pasa por debajo del header
3. El primer párrafo tiene padding extra para no quedar oculto inicialmente
