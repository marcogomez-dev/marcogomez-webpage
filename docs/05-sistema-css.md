# Sistema de Diseño CSS

Este directorio contiene el sistema de diseño CSS para el portafolio de Marco Gómez. La metodología se basa en una arquitectura de capas inspirada en ITCSS, utilizando características nativas de CSS como `@layer` y Custom Properties para crear un sistema mantenible, escalable y consistente.

## Filosofía Principal

1.  **HTML Nativo Primero**: Se prioriza el uso de elementos HTML semánticos y sus estilos base para la mayoría del contenido. Las clases personalizadas se reservan para componentes de UI que no tienen un equivalente nativo en HTML.
2.  **Unidades de Espaciado Contextuales**:
    *   **`rem` para la Estructura Global**: Se utilizan unidades `rem` para márgenes de página, espaciado entre secciones y rejillas principales. Esto asegura que la estructura general responda de manera consistente a las preferencias de tamaño de fuente del usuario.
    *   **`em` para Componentes**: Se utilizan unidades `em` para el espaciado interno de los componentes (ej. `padding` de un botón). Esto permite que los componentes escalen proporcionalmente a su propio contenido y tamaño de fuente.

## Arquitectura de Capas (`@layer`)

El sistema organiza los estilos en tres capas de cascada explícitas para gestionar la especificidad y el orden de aplicación. Las capas se definen en `main.css` en el siguiente orden:

1.  **`@layer base`**: La capa más genérica y de menor especificidad.
    *   **Propósito**: Contiene resets, normalizaciones, variables CSS globales (`:root`) y estilos por defecto para elementos HTML puros (`body`, `h1`, `p`, `a`, etc.).
    *   **Archivos**: `base.css`, `content.css`, `layout.css`, `form.css`, `table.css`, `syntax.css`.

2.  **`@layer component`**: Capa para componentes de UI específicos y reutilizables.
    *   **Propósito**: Define los estilos para bloques de UI autocontenidos como botones, diálogos, tarjetas o notificaciones.
    *   **Archivos**: `button.css`, `dialog.css`, `components.css`, `document.css`.

3.  **`@layer modifier`**: La capa de mayor especificidad, diseñada para anular otros estilos.
    *   **Propósito**: Contiene clases de utilidad (utilities) que aplican una sola regla o una pequeña modificación visual (ej. `.wide`, `.thin`).
    *   **Archivos**: `modifier.css`.

## Políticas y Reglas de Diseño

### 1. Variables (Custom Properties)

Todo el sistema de diseño se articula a través de variables definidas en `:root` dentro de `src/styles/design/base.css`.

*   **Colores**: Está estrictamente prohibido usar colores "hardcodeados" (ej. `#FFF`, `rgb(0,0,0)`). Todos los valores de color deben ser referenciados a través de las variables de color existentes. Si se necesita un nuevo color, debe ser añadido primero a `base.css`.
    *   `--base-*`: Paleta de colores base (grises, fondos).
    *   `--accent-*`: Colores de acento para la marca.
    *   `--syntax-*`: Colores para el resaltado de sintaxis.
*   **Tipografía y Espaciado**:
    *   `--m`, `--l`, `--xl`: Variables para el espaciado y la rejilla tipográfica.
    *   `--max-line-width`: Define el ancho máximo de línea para mejorar la legibilidad del texto.

### 2. Creación de Estilos

*   **No Redundancia**: Si un elemento HTML ya tiene un estilo base adecuado definido en la capa `base`, no se debe redefinir ese estilo dentro de una clase de componente. Las clases de componente deben centrarse únicamente en el layout y la apariencia que es única para ese componente.
*   **Nuevos Componentes**: Cualquier nuevo componente de UI debe crearse en su propio archivo dentro de `src/styles/design/` y ser importado en `main.css`. El contenido del archivo debe estar encapsulado en la capa `@layer component`.
*   **Prohibición de Estilos en Componentes Svelte**: Está estrictamente prohibido el uso de la etiqueta `<style>` dentro de los archivos `.svelte`. Todos los estilos deben ser definidos en archivos CSS separados dentro de `src/styles/design/` y seguir las reglas del sistema CSS, priorizando el uso de clases existentes o la creación de nuevas clases bajo la capa `@layer component` o `@layer modifier` según corresponda.
*   **Modificadores**: Para variaciones de un componente (ej. un botón secundario), utiliza una clase modificadora (ej. `.button.secondary`) en lugar de crear un componente completamente nuevo.

### 3. Iconografía y Gráficos

*   Los íconos deben ser consistentes, preferiblemente sólidos y con bordes ligeramente redondeados, utilizando los colores de la paleta base (`--base-800`) o de acento (`--accent-primary`).
*   Los patrones gráficos, como formas geométricas o líneas sutiles, deben usarse para añadir estructura y orden visual, siempre de forma que no distraigan del contenido principal.
