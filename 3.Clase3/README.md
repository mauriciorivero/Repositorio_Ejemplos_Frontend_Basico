# Clase 3 - Formularios HTML

## Descripción
Este ejemplo demuestra la creación de un formulario completo con diferentes tipos de campos de entrada y validación básica.

## Archivo

### `index.html`
Formulario de registro que incluye:

#### Campos del Formulario
- **Select (Tipo de documento)**: Menú desplegable con opciones:
  - Cédula (CC)
  - Tarjeta de identidad (TI)
  - Permiso de trabajo (PT)
  - Pasaporte (P)

- **Inputs de texto**: 
  - Número de documento
  - Primer nombre
  - Segundo nombre
  - Primer apellido
  - Segundo apellido

- **Radio buttons (Sexo)**: Selección única entre Hombre/Mujer usando el atributo `name` para agruparlos

- **Input email**: Campo específico para correo electrónico con validación automática del navegador

- **Checkboxes (Intereses)**: Selección múltiple de intereses:
  - Videojuegos
  - Deportes
  - Política
  - Arte

- **Submit button**: Botón para enviar el formulario

#### Atributos Importantes
- `required`: Campos obligatorios
- `placeholder`: Texto de ayuda dentro del campo
- `id` y `for`: Asociación entre labels e inputs para accesibilidad
- `name`: Agrupación de radio buttons
- `value`: Valor que se envía al servidor

## Conceptos Aprendidos
- Estructura de formularios HTML (`<form>`)
- Diferentes tipos de inputs: text, email, radio, checkbox, submit
- Elemento `<select>` con `<option>`
- Uso de `<label>` para accesibilidad
- Validación HTML5 con atributo `required`
- Agrupación de elementos con `<div>`
