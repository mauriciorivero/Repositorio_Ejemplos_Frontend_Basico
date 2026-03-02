# Clase 2 - Estructura HTML Básica y Multimedia

## Descripción
Este ejemplo demuestra la creación de un sitio web multipágina con estructura HTML básica, navegación entre páginas y elementos multimedia.

## Archivos

### `index.html`
Página principal que contiene:
- **Estructura semántica**: Uso de etiquetas `<header>`, `<main>` y `<footer>`
- **Navegación**: Lista ordenada (`<ol>`) con enlaces a las diferentes páginas del sitio
- **Logo**: Imagen con atributo `width` para controlar el tamaño
- **Enlace a documento PDF**: Uso de `target="_blank"` para abrir en nueva pestaña
- **Tabla HTML**: Tabla con `<thead>` y `<tbody>` que incluye:
  - Inputs tipo `radio` para selección única (SI/NO)
  - Inputs tipo `text` para observaciones
  - Inputs tipo `file` para subir archivos

### `cancion.html`
Página de audio que demuestra:
- **Elemento `<audio>`**: Reproductor de audio con atributo `controls` para mostrar controles de reproducción
- **Navegación consistente**: Misma estructura de menú que las otras páginas

### `pelicula.html`
Página de video que demuestra:
- **Elemento `<video>`**: Reproductor de video con atributos `controls` y `autoplay`
- **Navegación consistente**: Misma estructura de menú

## Estructura de Carpetas
```
2.Clase2/
├── index.html
├── cancion.html
├── pelicula.html
├── docs/           # Documentos PDF
├── img/            # Imágenes (logo)
└── media/          # Archivos multimedia (audio y video)
```

## Conceptos Aprendidos
- Estructura básica de un documento HTML5
- Navegación entre múltiples páginas
- Tablas HTML con encabezados y cuerpo
- Formularios con diferentes tipos de inputs
- Elementos multimedia: `<audio>` y `<video>`
- Enlaces a documentos externos
