# Marco Gómez - Portafolio y Documentación

Bienvenido al repositorio del portafolio y la documentación de Marco Gómez. Aquí encontrarás información detallada sobre mi marca personal, mi enfoque profesional, los servicios que ofrezco, mis proyectos y la tecnología utilizada en este sitio web.

## Índice de Documentación

Esta sección te guiará a través de los documentos clave que describen la visión y la implementación de mi marca y portafolio digital.

*   [**00-Marca.md: Marca Personal y Web**](docs/00-Marca.md)
    *   Consolida el briefing completo de la marca, la lógica y esencia, propuesta de valor, público objetivo, objetivos de la web, requisitos de contenido, diseño estético y la propuesta de diseño visual.
*   [**01-Lineamientos.md: Lineamientos de Diseño y Tecnología**](docs/01-Lineamientos.md)
    *   Detalla los lineamientos de diseño web (UI/UX), la pila tecnológica propuesta (SvelteKit v5, TypeScript, Bun, Bits UI, Lucide), los cambios esenciales de sintaxis para Svelte 5 y la arquitectura del sistema CSS.
*   [**02-Maquetado.md: Maquetado Teórico de la Web**](docs/02-Maquetado.md)
    *   Proporciona la estructura detallada, el contenido y los elementos de diseño clave para cada sección de la web, consolidando la información de los documentos de marca y lineamientos.

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
