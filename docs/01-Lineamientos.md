# 01-Lineamientos.md

Este documento consolida los lineamientos de diseño web (UI/UX), la pila tecnológica propuesta, los cambios esenciales de sintaxis para Svelte 5 y la arquitectura del sistema CSS.

---

## 1. Lineamientos de Diseño Web (UI/UX)

Estos principios son cruciales para el diseño del sitio web, asegurando que no solo sea atractivo, sino también funcional y fácil de usar.

*   **Patrones Gráficos y Elementos de Marca:**
    *   **Formas Geométricas y Cuadros:** Para honrar el aspecto de "contador estratégico", se creará un sistema de formas geométricas simples (cuadros, rectángulos) que se pueden superponer o usar para enmarcar texto e imágenes. Estas formas se usarán para crear un sentido de orden y estructura, sin ser demasiado rígidas. El color de acento, el **Azul Cerúleo**, se utilizará para resaltar estos elementos. static\marca\formas.png 
    *   **Iconografía Consistente:** Los íconos que representen servicios o procesos serán **sólidos y con bordes ligeramente redondeados**. Estarán en un solo color (preferiblemente el Gris Carbón Intenso o el Azul Cerúleo) para mantener la coherencia y la legibilidad. Se asegurará que todos los íconos pertenezcan al mismo set o estilo para una apariencia profesional.

*   **Principios de Diseño Web (UI/UX):**
    *   **Diseño Limpio y Minimalista:** Se utilizará el **Blanco Nube** como el lienzo principal. El espacio en blanco será un elemento de diseño clave, ya que ayuda a que el contenido respire y a que la información importante se destaque.
    *   **Jerarquía Visual Clara:** El uso estratégico de la **tipografía (Poppins para títulos, Inter para texto)** y el color de acento es fundamental para guiar la mirada del usuario. Los títulos, subtítulos y llamados a la acción (CTAs) tendrán un tamaño y color que faciliten la navegación y la comprensión.
    *   **Animaciones Sutiles:** Las animaciones y transiciones deben ser mínimas y elegantes. Por ejemplo, un fade-in sutil para las imágenes o un ligero movimiento en los íconos al pasar el cursor, que añada un toque de dinamismo sin distraer del mensaje.
    *   **Diseño Móvil (Mobile-First):** El sitio web se diseñará pensando primero en los usuarios de dispositivos móviles. El diseño se adaptará perfectamente a pantallas más pequeñas, con menús de navegación claros y botones grandes y fáciles de presionar.

---

## 2. Tecnología Web Propuesta para el Portafolio de Marco Gómez

Para la construcción del portafolio web, se propone la siguiente pila tecnológica, seleccionada para garantizar un desarrollo moderno, eficiente y escalable, alineado con los principios de innovación y precisión de la marca.

### Framework Frontend: SvelteKit v5

*   **Descripción:** SvelteKit es un framework de desarrollo web que utiliza Svelte, un compilador que convierte los componentes en código JavaScript vainilla altamente optimizado en tiempo de compilación. Esto resulta en aplicaciones extremadamente rápidas y con un tamaño de bundle mínimo. SvelteKit, la capa de framework sobre Svelte, proporciona enrutamiento, renderizado del lado del servidor (SSR), generación de sitios estáticos (SSG) y otras características esenciales para aplicaciones web modernas.
*   **Ventajas Clave:**
    *   **Rendimiento Superior:** Al compilar el código, Svelte elimina la necesidad de un "runtime" en el navegador, lo que se traduce en una experiencia de usuario más fluida y rápida.
    *   **Desarrollo Intuitivo:** Svelte reduce la cantidad de código boilerplate, haciendo el desarrollo más directo y legible.
    *   **SSR y SSG:** Facilita la optimización SEO y mejora el tiempo de carga inicial.

### Lenguaje de Programación: TypeScript

*   **Descripción:** TypeScript es un superconjunto de JavaScript que añade tipado estático opcional. Esto permite detectar errores en tiempo de desarrollo, mejorar la legibilidad del código y facilitar el mantenimiento de proyectos grandes.
*   **Ventajas Clave:**
    *   **Fiabilidad:** Reduce la probabilidad de errores en producción al atrapar problemas de tipo antes de la ejecución.
    *   **Mantenibilidad:** Facilita la refactorización y la comprensión del código, especialmente en equipos o proyectos a largo plazo.
    *   **Mejor Experiencia de Desarrollo:** Proporciona autocompletado y sugerencias de código en editores como VS Code.

### Entorno de Ejecución y Gestor de Paquetes: Bun

*   **Descripción:** Bun es un nuevo entorno de ejecución de JavaScript y TypeScript, gestor de paquetes y bundler todo en uno, diseñado para ser extremadamente rápido. Es una alternativa moderna a Node.js y npm/Yarn.
*   **Ventajas Clave:**
    *   **Velocidad:** Ofrece un rendimiento significativamente superior en la instalación de paquetes, ejecución de scripts y bundling.
    *   **Simplicidad:** Combina múltiples herramientas en una sola, simplificando el flujo de trabajo de desarrollo.

### Librería de Componentes UI: Bits UI

*   **Descripción:** Bits UI es una librería de componentes UI sin estilos, diseñada para ser altamente accesible y personalizable. Proporciona la lógica y la accesibilidad necesarias para construir componentes complejos (como modales, acordeones, tooltips) sin imponer un estilo visual, lo que permite una integración perfecta con el sistema de diseño CSS nativo.
*   **Ventajas Clave:**
    *   **Flexibilidad de Estilo:** Permite implementar el sistema de diseño OOCSS + ITCSS con CSS nativo sin conflictos de estilos predefinidos.
    *   **Accesibilidad (A11y):** Asegura que los componentes sean utilizables por todos los usuarios, siguiendo las mejores prácticas de accesibilidad web.
*   **Reutilización:** Proporciona una base sólida y probada para componentes interactivos.

### Librería de Iconos: Lucide (`@lucide/svelte`)

*   **Descripción:** Lucide es una librería de íconos de código abierto, moderna y personalizable, diseñada para ser ligera y fácil de integrar. Para SvelteKit v5, se utiliza la implementación `@lucide/svelte`, que permite importar íconos individualmente para optimizar el tamaño del bundle. Ofrece una amplia gama de íconos con un estilo de línea consistente y limpio, ideal para interfaces de usuario.
*   **Ventajas Clave:**
    *   **Estilo Coherente:** Sus íconos minimalistas y de línea se alinean perfectamente con la estética de diseño propuesta (limpia, moderna, con bordes redondeados).
    *   **Personalización:** Permite ajustar fácilmente el tamaño, el color y el grosor del trazo, lo que facilita la integración con la paleta de colores de la marca.
    *   **Optimización:** Al ser SVG, son escalables sin pérdida de calidad y pueden ser optimizados para un rendimiento web rápido.
    *   **Importación Individual:** Permite importar solo los íconos necesarios (ej. `import Home from '@lucide/svelte/icons/home';`), reduciendo el tamaño final del bundle.

### Consideraciones Adicionales:

*   **Prohibición de Frameworks CSS:** Se evitará el uso de frameworks CSS como TailwindCSS, Bootstrap o similares. El estilo se construirá utilizando CSS nativo, siguiendo las metodologías OOCSS e ITCSS, aprovechando las últimas características de CSS como el nesting y `@apply` (si es soportado por el preprocesador o el entorno de compilación). Esto garantiza un control total sobre el CSS, un tamaño de archivo optimizado y una mayor alineación con los principios de diseño minimalista y ordenado.

---

## 3. Svelte 5: Cambios de Sintaxis Esenciales

Svelte 5 introduce una sintaxis revisada y un nuevo sistema de reactividad basado en "runes", que son instrucciones del compilador que comienzan con un signo de dólar (`$`). La sintaxis antigua de Svelte 4 sigue siendo compatible y se puede mezclar.

### Cambios en la Sintaxis de Reactividad:
*   **Declaración de estado:**
    *   **Antes (Svelte 4):** `let count = 0;` (reactividad implícita)
    *   **Ahora (Svelte 5):** `let count = $state(0);` (reactividad explícita con `$state`)
*   **Derivaciones y efectos secundarios:**
    *   **Antes (Svelte 4):** `$: const double = count * 2;` o `$: alert('...');`
    *   **Ahora (Svelte 5):**
        *   Para derivaciones: `const double = $derived(count * 2);`
        *   Para efectos secundarios: `$effect(() => { /* código */ });`
*   **Propiedades (Props):**
    *   **Antes (Svelte 4):** `export let optional = 'unset';`
    *   **Ahora (Svelte 5):** `let { optional = 'unset', required } = $props();` (declaración mediante desestructuración de `$props()`)
    *   Manejo de `$$restProps` y renombramiento de props se simplifica con la desestructuración de `$props()`.

### Cambios en Eventos:
*   **Manejadores de eventos DOM:**
    *   **Antes (Svelte 4):** `<button on:click={handler}>`
    *   **Ahora (Svelte 5):** `<button onclick={handler}>` (los manejadores son propiedades directas)
*   **Eventos de componentes:**
    *   **Antes (Svelte 4):** Uso de `createEventDispatcher` para emitir eventos.
    *   **Ahora (Svelte 5):** Los componentes deben aceptar funciones de callback como props (ej. `onInflate={(power) => { ... }}`).
*   **Modificadores de eventos:**
    *   **Antes (Svelte 4):** `<button on:click|once|preventDefault={handler}>`
    *   **Ahora (Svelte 5):** Se prefieren funciones wrapper manuales (ej. `onclick={once(preventDefault(handler))}`) o atributos específicos (ej. `onclickcapture`). Los modificadores `capture`, `passive` y `nonpassive` son excepciones.
*   **Múltiples manejadores de eventos:**
    *   **Antes (Svelte 4):** `<button on:click={one} on:click={two}>`
    *   **Ahora (Svelte 5):** `<button onclick={(e) => { one(e); two(e); }}>`

### Snippets en lugar de Slots:
*   **Contenido por defecto:**
    *   **Antes (Svelte 4):** `<slot />`
    *   **Ahora (Svelte 5):** Se usa la prop `children` y se renderiza con `{@render children()}`.
*   **Múltiples placeholders de contenido (slots con nombre):**
    *   **Antes (Svelte 4):** `<slot name="header" />`
    *   **Ahora (Svelte 5):** Se usan props con nombre (ej. `let { header, main, footer } = $props();`) y se renderizan con `{@render header()}`.
*   **Pasar datos hacia arriba (let:):**
    *   **Antes (Svelte 4):** `<List items={...} let:item>`
    *   **Ahora (Svelte 5):** Se usan snippets para pasar datos (ej. `{#snippet item(text)}`).

### Otros Cambios Notables:
*   **Componentes ya no son clases:** Ahora son funciones. La instanciación manual cambia de `new App(...)` a `mount(App, ...)`.
*   **`<svelte:component>` ya no es necesario:** Los componentes dinámicos se pueden renderizar directamente con `<Thing />` si `Thing` es una variable que contiene un componente.
*   **Manejo de espacios en blanco:** Reglas simplificadas (colapsa a un espacio entre nodos, elimina al inicio/final de etiquetas).
*   **Navegador moderno requerido:** Svelte 5 requiere navegadores modernos (no IE) debido al uso de Proxies y otras APIs.
*   **`children` prop reservada:** No se puede tener una prop separada llamada `children`.
*   **Bindings a exports de componentes no permitidos:** Se debe usar `bind:this` y acceder al export a través de la instancia.
*   **Bindings deben ser explícitamente `$bindable()`:** Las props no son bindable por defecto.
*   **`accessors` e `immutable` options ignoradas** en modo runes.
*   **Clases ya no son "auto-reactivas":** La reactividad se define en tiempo de ejecución con `$state` en los campos de la clase.
*   **Atributos/props y estructura HTML más estrictos.**
*   **CSS scoped usa `:where(...)`** para evitar cambios impredecibles de especificidad.
*   **`beforeUpdate`/`afterUpdate`:** Cambios en el comportamiento y deshabilitados en modo runes (usar `$effect.pre` y `$effect`).

---

## 4. Sistema de Diseño CSS

Este sistema de diseño CSS para el portafolio de Marco Gómez se basa en la filosofía de diseño de Nue v2, que posiciona a CSS como el lenguaje central para la construcción de sistemas de diseño. Complementa los lineamientos existentes, priorizando la centralización, la semántica HTML, el uso estratégico de clases para el layout, la organización en capas y el minimalismo.

### Principios Fundamentales del Sistema de Diseño CSS (Basado en Nue v2)

1.  **Centralizado, no disperso:**
    *   El sistema de diseño reside en un único lugar (`src/styles/design/`), permitiendo una visión holística y la comprensión de las relaciones entre componentes.
    *   Evita la dispersión de estilos en archivos de componentes o JavaScript, lo que puede llevar a inconsistencias y dificultades de mantenimiento.

2.  **Semántica primero (HTML Nativo Primero):**
    *   Se prioriza el uso de elementos HTML semánticos (`<button>`, `<nav>`, `<section>`) y se extiende su vocabulario en lugar de reemplazarlo con clases genéricas.
    *   Los estilos base se aplican directamente a estos elementos nativos, aprovechando su significado inherente.

3.  **Nombres de clases para preocupaciones espaciales (Layout):**
    *   Las clases CSS se reservan principalmente para expresar relaciones de diseño espacial y layout, ya que HTML no tiene una semántica para esto. Ejemplos: `.container`, `.stack`, `.grid`, `.columns`.
    *   Los modificadores (`.inverted`, `.compact`, `.emphasized`) se utilizan para expresar variaciones de estos layouts o componentes.
    *   Se busca minimizar la necesidad de clases para otros propósitos, confiando en la semántica HTML y el anidamiento de CSS.

4.  **Todo en capas (Arquitectura `@layer`):**
    *   Se utilizan las `@layer` de CSS para resolver los conflictos de especificidad y establecer un orden predecible en la cascada.
    *   Las capas se organizan con límites y propósitos claros, definidas en `main.css` en el siguiente orden:
        *   **`@layer base`**: La capa más genérica y de menor especificidad. Contiene resets, normalizaciones, variables CSS globales (`:root`) y estilos por defecto para elementos HTML puros (`body`, `h1`, `p`, `a`, etc.). Archivos: `base.css`, `content.css`, `layout.css`, `form.css`, `table.css`, `syntax.css`.
        *   **`@layer component`**: Capa para componentes de UI específicos y reutilizables. Define los estilos para bloques de UI autocontenidos como botones, diálogos, tarjetas o notificaciones. Archivos: `button.css`, `dialog.css`, `components.css`, `document.css`.
        *   **`@layer modifier`**: La capa de mayor especificidad, diseñada para anular otros estilos. Contiene clases de utilidad o modificadores que aplican una sola regla o una pequeña modificación visual (ej. `.wide`, `.thin`). Archivos: `modifiers.css` (anteriormente `modifier.css`).

5.  **Mantenerlo obvio y minimalista:**
    *   El sistema debe ser intuitivo; cambiar un color primario debe ser tan simple como ajustar una variable CSS (`--primary`).
    *   Se promueve un número reducido de clases (idealmente entre 10 y 30) para fomentar la adopción y evitar que los desarrolladores recurran a estilos locales.
    *   Las restricciones guían hacia buenas decisiones de diseño al hacer que el camino hacia la implementación sea directo.

### Políticas y Reglas de Diseño

#### 1. Variables (Custom Properties)

Todo el sistema de diseño se articula a través de variables definidas en `:root` dentro de `src/styles/design/base.css`.

*   **Colores**: Está estrictamente prohibido usar colores "hardcodeados" (ej. `#FFF`, `rgb(0,0,0)`). Todos los valores de color deben ser referenciados a través de las variables de color existentes. Si se necesita un nuevo color, debe ser añadido primero a `base.css`.
    *   `--base-*`: Paleta de colores base (grises, fondos).
    *   `--accent-*`: Colores de acento para la marca.
    *   `--syntax-*`: Colores para el resaltado de sintaxis.
*   **Tipografía y Espaciado**:
    *   `--m`, `--l`, `--xl`: Variables para el espaciado y la rejilla tipográfica.
    *   `--max-line-width`: Define el ancho máximo de línea para mejorar la legibilidad del texto.

#### 2. Unidades de Espaciado Contextuales

*   **`rem` para la Estructura Global**: Se utilizan unidades `rem` para márgenes de página, espaciado entre secciones y rejillas principales. Esto asegura que la estructura general responda de manera consistente a las preferencias de tamaño de fuente del usuario.
*   **`em` para Componentes**: Se utilizan unidades `em` para el espaciado interno de los componentes (ej. `padding` de un botón). Esto permite que los componentes escalen proporcionalmente a su propio contenido y tamaño de fuente.

#### 3. Creación de Estilos

*   **No Redundancia**: Si un elemento HTML ya tiene un estilo base adecuado definido en la capa `base`, no se debe redefinir ese estilo dentro de una clase de componente. Las clases de componente deben centrarse únicamente en el layout y la apariencia que es única para ese componente.
*   **Nuevos Componentes**: Cualquier nuevo componente de UI debe crearse en su propio archivo dentro de `src/styles/design/` y ser importado en `main.css`. El contenido del archivo debe estar encapsulado en la capa `@layer component`.
*   **Prohibición de Estilos en Componentes Svelte**: Está estrictamente prohibido el uso de la etiqueta `<style>` dentro de los archivos `.svelte`. Todos los estilos deben ser definidos en archivos CSS separados dentro de `src/styles/design/` y seguir las reglas del sistema CSS, priorizando el uso de clases existentes o la creación de nuevas clases bajo la capa `@layer component` o `@layer modifier` según corresponda.
*   **Modificadores**: Para variaciones de un componente (ej. un botón secundario), utiliza una clase modificadora (ej. `.button.secondary`) en lugar de crear un componente completamente nuevo.

#### 4. Iconografía y Gráficos

*   Los íconos deben ser consistentes, preferiblemente sólidos y con bordes ligeramente redondeados, utilizando los colores de la paleta base (`--base-800`) y como color de acento (`--accent-primary`) o color primario para estatus activo por ejemplo.
*   Los patrones gráficos, como formas geométricas o líneas sutiles, deben usarse para añadir estructura y orden visual, siempre de forma que no distraigan del contenido principal.

### Beneficios Adicionales del Sistema de Diseño

*   **Consistencia de Diseño:** Asegura que todos los elementos visuales del sitio web compartan el mismo lenguaje visual, desde el marketing hasta la aplicación.
*   **Desarrollo Rápido de UI:** Los desarrolladores pueden centrarse en la estructura y los flujos de usuario, ensamblando interfaces con la confianza de que la forma sigue la función.
*   **Mantenibilidad a Escala:** Un sistema unificado y predecible facilita la incorporación de nuevos miembros al equipo y simplifica las actualizaciones de diseño, reduciendo la deuda técnica.

### Consideraciones Adicionales

*   **Prohibición de Frameworks CSS:** Se evitará el uso de frameworks CSS como TailwindCSS, Bootstrap o similares. El estilo se construirá utilizando CSS nativo, siguiendo las metodologías OOCSS e ITCSS, aprovechando las últimas características de CSS como el nesting. Esto garantiza un control total sobre el CSS, un tamaño de archivo optimizado y una mayor alineación con los principios de diseño minimalista y ordenado.
*   **Fundación Brutalista:** El uso de principios de diseño "brutalistas" proporciona una capa mínima sobre los valores predeterminados del navegador, sirviendo como un punto de partida sólido y demostrando los principios de HTML semántico y CSS mínimo.
