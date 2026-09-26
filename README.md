# Actividad 4 - HTML Semántico, Accesibilidad y CSS

Maqueta de una página con encabezado, artículos, formulario de contacto, tabla de puntajes y pie de página, basada en la plantilla entregada.

- **Autor:** Samir Rosero Armero
- **Curso:** Desarrollo de Aplicaciones Web
- **Repositorio:** [github.com/samirrosero/actividad-4](https://github.com/samirrosero/actividad-4)

## Requisitos de la actividad

- [x] Aplicar HTML semántico.
- [x] Usar etiquetas de formulario, imagen, botones, tablas y demás etiquetas necesarias.
- [x] Investigar y poner en práctica la accesibilidad.
- [x] Agregar CSS externo básico que se acerque al diseño de la imagen.

## Estructura del proyecto

```
actividad-4/
├── index.html          # Estructura de la página
├── README.md           # Este archivo
├── css/
│   └── styles.css      # Hoja de estilos externa
└── img/
    └── placeholder.svg # Imagen de ejemplo (80 × 80) de los artículos
```

## Secciones de la página

1. **Encabezado:** logo y menú de navegación (Home, About, Contact).
2. **Artículos:** dos tarjetas con imagen, título y texto.
3. **Formulario de contacto:** nombre, correo, mensaje y botón de envío.
4. **Tabla de puntajes:** notas de HTML y CSS por estudiante, con fila de total.
5. **Pie de página:** correo de contacto.

## HTML semántico

- `header`, `nav`, `main`, `section`, `article`, `figure`, `footer` y `address`.
- Jerarquía de encabezados ordenada (`h1` → `h2`).

## Etiquetas usadas

- **Formulario:** `form`, `label`, `input` (`text`, `email`), `textarea`, `button`.
- **Imagen:** `img` dentro de `figure`, con `alt`, `width` y `height`.
- **Tabla:** `table`, `caption`, `thead`, `tbody`, `tfoot`, `tr`, `th`, `td` y `colspan`.

## Accesibilidad aplicada

- `lang="es"` en el documento para que los lectores de pantalla usen la pronunciación correcta.
- Enlace **"Saltar al contenido principal"**, visible al navegar con la tecla Tab.
- `aria-label` en la navegación y el logo; `aria-current="page"` en el enlace activo.
- `aria-labelledby` en secciones y artículos para asociarlos a su título.
- Cada campo del formulario tiene su `label` con `for`; se usan `required`, `aria-required`, `aria-describedby` y `autocomplete`.
- Texto alternativo (`alt`) descriptivo en las imágenes.
- Tabla con `caption` y `th` con `scope="col"` / `scope="row"`, para que se lea cada celda con su encabezado.
- Clase `.solo-lectores`: oculta contenido visualmente pero lo deja disponible para lectores de pantalla.
- Indicador de foco visible (`:focus-visible`) y buen contraste de colores.
- Diseño responsive: en pantallas pequeñas las tarjetas se ubican en una sola columna.

## Cómo verlo

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/samirrosero/actividad-4.git
   ```
2. Abrir `index.html` en el navegador.

## Probar la accesibilidad

- Navegar la página solo con **Tab** y **Shift + Tab**: el primer Tab muestra el enlace "Saltar al contenido principal" y cada elemento enfocado se resalta.
- Usar un lector de pantalla (NVDA en Windows o Narrador con `Ctrl + Win + Enter`) para escuchar las etiquetas del formulario y los encabezados de la tabla.
- Revisar con la pestaña **Lighthouse** de las herramientas de desarrollador de Chrome (categoría *Accessibility*).
