### **Tecnología Web Propuesta para el Portafolio de Marco Gómez**

Para la construcción del portafolio web, se propone la siguiente pila tecnológica, seleccionada para garantizar un desarrollo moderno, eficiente y escalable, alineado con los principios de innovación y precisión de la marca.

#### **1. Framework Frontend: SvelteKit v5**

*   **Descripción:** SvelteKit es un framework de desarrollo web que utiliza Svelte, un compilador que convierte los componentes en código JavaScript vainilla altamente optimizado en tiempo de compilación. Esto resulta en aplicaciones extremadamente rápidas y con un tamaño de bundle mínimo. SvelteKit, la capa de framework sobre Svelte, proporciona enrutamiento, renderizado del lado del servidor (SSR), generación de sitios estáticos (SSG) y otras características esenciales para aplicaciones web modernas.
*   **Ventajas Clave:**
    *   **Rendimiento Superior:** Al compilar el código, Svelte elimina la necesidad de un "runtime" en el navegador, lo que se traduce en una experiencia de usuario más fluida y rápida.
    *   **Desarrollo Intuitivo:** Svelte reduce la cantidad de código boilerplate, haciendo el desarrollo más directo y legible.
    *   **SSR y SSG:** Facilita la optimización SEO y mejora el tiempo de carga inicial.

#### **2. Lenguaje de Programación: TypeScript**

*   **Descripción:** TypeScript es un superconjunto de JavaScript que añade tipado estático opcional. Esto permite detectar errores en tiempo de desarrollo, mejorar la legibilidad del código y facilitar el mantenimiento de proyectos grandes.
*   **Ventajas Clave:**
    *   **Fiabilidad:** Reduce la probabilidad de errores en producción al atrapar problemas de tipo antes de la ejecución.
    *   **Mantenibilidad:** Facilita la refactorización y la comprensión del código, especialmente en equipos o proyectos a largo plazo.
    *   **Mejor Experiencia de Desarrollo:** Proporciona autocompletado y sugerencias de código en editores como VS Code.

#### **3. Entorno de Ejecución y Gestor de Paquetes: Bun**

*   **Descripción:** Bun es un nuevo entorno de ejecución de JavaScript y TypeScript, gestor de paquetes y bundler todo en uno, diseñado para ser extremadamente rápido. Es una alternativa moderna a Node.js y npm/Yarn.
*   **Ventajas Clave:**
    *   **Velocidad:** Ofrece un rendimiento significativamente superior en la instalación de paquetes, ejecución de scripts y bundling.
    *   **Simplicidad:** Combina múltiples herramientas en una sola, simplificando el flujo de trabajo de desarrollo.

#### **4. Librería de Componentes UI: Bits UI**

*   **Descripción:** Bits UI es una librería de componentes UI sin estilos, diseñada para ser altamente accesible y personalizable. Proporciona la lógica y la accesibilidad necesarias para construir componentes complejos (como modales, acordeones, tooltips) sin imponer un estilo visual, lo que permite una integración perfecta con el sistema de diseño CSS nativo.
*   **Ventajas Clave:**
    *   **Flexibilidad de Estilo:** Permite implementar el sistema de diseño OOCSS + ITCSS con CSS nativo sin conflictos de estilos predefinidos.
    *   **Accesibilidad (A11y):** Asegura que los componentes sean utilizables por todos los usuarios, siguiendo las mejores prácticas de accesibilidad web.
*   **Reutilización:** Proporciona una base sólida y probada para componentes interactivos.

#### **5. Librería de Iconos: Lucide (`@lucide/svelte`)**

*   **Descripción:** Lucide es una librería de íconos de código abierto, moderna y personalizable, diseñada para ser ligera y fácil de integrar. Para SvelteKit v5, se utiliza la implementación `@lucide/svelte`, que permite importar íconos individualmente para optimizar el tamaño del bundle. Ofrece una amplia gama de íconos con un estilo de línea consistente y limpio, ideal para interfaces de usuario.
*   **Ventajas Clave:**
    *   **Estilo Coherente:** Sus íconos minimalistas y de línea se alinean perfectamente con la estética de diseño propuesta (limpia, moderna, con bordes redondeados).
    *   **Personalización:** Permite ajustar fácilmente el tamaño, el color y el grosor del trazo, lo que facilita la integración con la paleta de colores de la marca.
    *   **Optimización:** Al ser SVG, son escalables sin pérdida de calidad y pueden ser optimizados para un rendimiento web rápido.
    *   **Importación Individual:** Permite importar solo los íconos necesarios (ej. `import Home from '@lucide/svelte/icons/home';`), reduciendo el tamaño final del bundle.

#### **Consideraciones Adicionales:**

*   **Prohibición de Frameworks CSS:** Se evitará el uso de frameworks CSS como TailwindCSS, Bootstrap o similares. El estilo se construirá utilizando CSS nativo, siguiendo las metodologías OOCSS e ITCSS, aprovechando las últimas características de CSS como el nesting y `@apply` (si es soportado por el preprocesador o el entorno de compilación). Esto garantiza un control total sobre el CSS, un tamaño de archivo optimizado y una mayor alineación con los principios de diseño minimalista y ordenado.
