# Actividad 4 - HTML Semántico, Accesibilidad y CSS

Maqueta de una página con encabezado, artículos, formulario de contacto, tabla de puntajes y pie de página, basada en la plantilla entregada.

## Archivos

- `index.html`: estructura de la página.
- `styles.css`: hoja de estilos externa.
- `img/placeholder.svg`: imagen de ejemplo (80 × 80) usada en los artículos.

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

Abrir `index.html` en el navegador.
