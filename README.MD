# Marco Gómez - Portafolio y Documentación

Bienvenido al repositorio del portafolio y la documentación de Marco Gómez. Aquí encontrarás información detallada sobre mi marca personal, mi enfoque profesional, los servicios que ofrezco, mis proyectos y la tecnología utilizada en este sitio web.

## Índice de Documentación

Esta sección te guiará a través de los documentos clave que describen la visión y la implementación de mi marca y portafolio digital.

*   [**00-briefing.md: Briefing Completo de Marca Personal y Web**](docs/00-briefing.md)
    *   Detalla la lógica y esencia de mi marca, valores fundamentales, propuesta de valor, personalidad, público objetivo y los objetivos principales de la web.
*   [**01-contenido.md: Contenido Principal de la Web**](docs/01-contenido.md)
    *   Presenta el contenido textual para las secciones clave de la web: Inicio, Acerca de Mí, Servicios y Portafolio.
*   [**02-diseño_propuesto.md: Concepto "Impulso Digital" y Elementos de Diseño**](docs/02-diseño_propuesto.md)
    *   Define la paleta de colores, tipografía y estilo visual general que darán vida a la marca.
*   [**03-lineamientos_diseño.md: Patrones Gráficos y Lineamientos de Diseño Web (UI/UX)**](docs/03-lineamientos_diseño.md)
    *   Describe los elementos visuales consistentes y los principios de diseño para asegurar una experiencia de usuario óptima.
*   [**04-tecnologia-web.md: Tecnología Web Propuesta**](docs/04-tecnologia-web.md)
    *   Detalla la pila tecnológica seleccionada para la construcción del portafolio, incluyendo SvelteKit, TypeScript, Bun, Bits UI y Lucide.
*   [**04.1-sveltekit_migracion.md: Guía de Migración a Svelte 5**](docs/04.1-sveltekit_migracion.md)
    *   Guía de migración a Svelte 5, detallando los cambios en la sintaxis de reactividad, eventos, slots y otras actualizaciones importantes.
*   [**05-sistema-css.md: Sistema de Diseño CSS**](docs/05-sistema-css.md)
    *   Explica la implementación de OOCSS + ITCSS con CSS nativo, evitando frameworks externos para un control total del estilo.
*   [**06-Maquetado-teorico.md: Maquetado Teórico de la Web**](docs/06-Maquetado-teorico.md)
    *   Proporciona una estructura detallada y los elementos de diseño clave para cada sección de la web.

## Desarrollo del Proyecto

Este proyecto utiliza **Bun** como entorno de ejecución y gestor de paquetes.

### Instalación de Dependencias

Para instalar las dependencias del proyecto, ejecuta:

```sh
bun install
```

### Desarrollo Local

Para iniciar el servidor de desarrollo:

```sh
bun run dev
```

O para iniciar el servidor y abrir la aplicación en una nueva pestaña del navegador:

```sh
bun run dev -- --open
```

### Construcción para Producción

Para crear una versión de producción de la aplicación:

```sh
bun run build
```

Puedes previsualizar la versión de producción con:

```sh
bun run preview
```

> Para desplegar la aplicación, es posible que necesites instalar un [adaptador](https://svelte.dev/docs/kit/adapters) para tu entorno objetivo.
