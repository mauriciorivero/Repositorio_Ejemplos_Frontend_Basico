# Clase 7C - Flexbox: Propiedades Avanzadas

## Descripción
Este ejemplo demuestra propiedades avanzadas de Flexbox como `flex-direction: column-reverse`, `align-self` y selectores CSS avanzados.

## Archivos

### `index.html`
Estructura simple con 4 cajas numeradas:
```html
<header>
    <div class="caja">1</div>
    <div class="caja">2</div>
    <div class="caja">3</div>
    <div class="caja">4</div>
</header>
```

### `css/styles.css`
Estilos con propiedades Flexbox avanzadas:

```css
/* Contenedor con dirección inversa */
header {
    align-items: center;
    background-color: yellow;
    display: flex;
    flex-direction: column-reverse;  /* Invierte el orden: 4,3,2,1 */
    justify-content: space-between;
    height: 800px;
    width: 800px;
}

/* Selector nth-child para elemento específico */
header > :nth-child(2) {
    align-self: flex-start;    /* Alineación individual diferente */
    background-color: blue;
    display: flex;
    justify-self: flex-end;
}

/* Estilos de las cajas */
.caja {
    align-items: center;
    background-color: red;
    border: solid 1px black;
    display: flex;
    justify-content: center;
    height: 100px;
    width: 100px;
}
```

## Estructura de Carpetas
```
9.clase7_flex_c/
├── index.html
└── css/
    └── styles.css
```

## Conceptos Aprendidos

### flex-direction: column-reverse
- Los elementos se apilan verticalmente pero en orden inverso
- El elemento 1 aparece abajo y el 4 arriba

### align-self
- Permite que un elemento individual tenga una alineación diferente al resto
- Sobrescribe el `align-items` del contenedor para ese elemento específico

### Selector :nth-child()
- `header > :nth-child(2)` selecciona el segundo hijo directo del header
- Útil para aplicar estilos a elementos específicos sin agregar clases

### Centrado con Flexbox
- Las cajas usan `display: flex` con `align-items: center` y `justify-content: center` para centrar su contenido (los números)

## Visualización
```
┌────────────────────────┐
│          4             │  ← Aparece primero (column-reverse)
│                        │
│  ┌───┐                 │  ← Caja 3 (nth-child(2) con align-self)
│  │ 3 │                 │
│  └───┘                 │
│          2             │
│          1             │  ← Aparece último
└────────────────────────┘
```
