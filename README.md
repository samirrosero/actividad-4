# Actividad 4 - HTML Semántico, Accesibilidad y CSS

**WebLab** es una página de un curso de desarrollo web con presentación, módulos, tabla de puntajes, formulario de contacto y pie de página. Toma como base la plantilla entregada (encabezado y pie oscuros, contenido claro) y la amplía con un diseño sencillo, responsive y accesible.

- **Autor:** Samir Rosero Armero
- **Curso:** Desarrollo de Aplicaciones Web
- **Repositorio:** [github.com/samirrosero/actividad-4](https://github.com/samirrosero/actividad-4)

## Requisitos de la actividad

- [x] Aplicar HTML semántico.
- [x] Usar etiquetas de formulario, imagen, botones, tablas y demás etiquetas necesarias.
- [x] Investigar y poner en práctica la accesibilidad.
- [x] Agregar CSS externo que se acerque al diseño de la imagen.

## Estructura del proyecto

```
actividad-4/
├── index.html              # Estructura de la página
├── README.md               # Este archivo
├── css/
│   └── styles.css          # Hoja de estilos externa
└── img/
    ├── logo.svg            # Logo y favicon
    ├── semantico.svg       # Ilustración del módulo de HTML
    ├── accesibilidad.svg   # Ilustración del módulo de accesibilidad
    └── css.svg             # Ilustración del módulo de CSS
```

## Secciones de la página

1. **Encabezado fijo:** logo y menú de navegación.
2. **Presentación:** título principal y botones hacia las secciones.
3. **Módulos:** tres tarjetas (`article`) con imagen, categoría, título, descripción y enlace a MDN.
4. **Puntajes:** tabla con la nota por módulo, total, estado de cada estudiante y promedio del grupo.
5. **Contacto:** datos de contacto y formulario con validación nativa.
6. **Pie de página:** navegación secundaria, correo de contacto y derechos de autor.

## HTML semántico

- `header`, `nav`, `main`, `section`, `article`, `figure`, `address` y `footer`.
- Lista de definición (`dl`, `dt`, `dd`) para los datos de contacto.
- `time`, `strong` y `small` donde aportan significado.
- Jerarquía de encabezados ordenada: un solo `h1`, luego `h2` por sección y `h3` en las tarjetas.

## Etiquetas usadas

- **Formulario:** `form`, `fieldset`, `legend`, `label`, `input` (`text`, `email`, `checkbox`), `select`, `option`, `textarea` y `button` (`submit` y `reset`).
- **Imagen:** `img` dentro de `figure`, con `alt`, `width`, `height` y `loading="lazy"`.
- **Tabla:** `table`, `caption`, `thead`, `tbody`, `tfoot`, `tr`, `th` y `td`.

## Accesibilidad aplicada

- `lang="es"` para que los lectores de pantalla usen la pronunciación correcta.
- Enlace **"Saltar al contenido principal"**, visible al presionar Tab.
- `aria-label` en las dos navegaciones para diferenciarlas; `aria-current="page"` en el enlace activo.
- `aria-labelledby` en secciones y artículos para asociarlos a su título.
- Formulario:
  - Cada campo tiene su `label` con `for`, y los campos se agrupan con `fieldset` y `legend`.
  - `aria-describedby` asocia los textos de ayuda a cada campo.
  - `autocomplete` en nombre y correo.
  - Validación nativa con `required`, `type="email"` y `minlength`.
  - El asterisco de obligatorio se oculta a lectores de pantalla (`aria-hidden`) y se explica en texto.
  - Los errores se marcan con `:user-invalid`, es decir, solo después de que la persona interactúa con el campo.
- Imágenes con `alt` descriptivo; el logo junto al texto usa `alt=""` porque es decorativo.
- Los enlaces "Leer más" incluyen texto oculto que indica el tema y que se abren en una pestaña nueva.
- Tabla:
  - Tiene `caption` y encabezados con `scope="col"` y `scope="row"`.
  - Está dentro de una región con scroll que se puede usar con teclado (`role="region"`, `tabindex="0"`).
  - El estado de cada estudiante se indica con texto, no solo con color.
- Indicador de foco visible (`:focus-visible`) en todos los elementos interactivos.
- Contraste de colores pensado para cumplir WCAG AA.
- Objetivos táctiles de al menos 44 px en botones.
- Respeta la preferencia del sistema de reducir movimiento (`prefers-reduced-motion`).

## CSS

- Variables (`:root`) para colores, radios, sombras y tiempos de transición.
- Paleta sobria: gris oscuro para encabezado y pie, fondo claro y un azul como color principal.
- Layout con **Grid** y **Flexbox**.
- Nombres de clases en español con estilo BEM (`tarjeta__cuerpo`, `boton--primario`).
- Diseño responsive con puntos de quiebre en 800 px y 560 px.
- Fuentes del sistema, sin dependencias externas.

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
- Reducir el ancho de la ventana para ver cómo se adapta la página al celular.
