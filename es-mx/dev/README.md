# Tainacan para desarrolladores

Como saben, **Tainacan es un plugin de [WordPress](https://wordpress.org)** y está construido sobre esta conocida plataforma. Si estás familiarizado con _WordPress_ debería serte fácil entender cómo está organizado Tainacan, cómo interactúa con la base de datos y cómo construir tus propias funcionalidades a partir de él.

## Bueno, pero yo soy nuevo en WordPress

Si no tienes experiencia con WordPress y te gustaría desarrollar un plugin para Tainacan, o incluso contribuir al plugin, es una buena idea aprender algunos fundamentos. Éstos serán útiles para todo lo que tratará mientras trabaja con Tainacan.

Esta es una lista no exhaustiva de los temas más importantes que deberías investigar:

<div class="two-columns-list">

- [WP_Query](https://developer.wordpress.org/reference/classes/wp_query/ ":ignore") clase - Este es el corazón de WordPress, la clase que le da la interfaz para consultar las entradas en la base de datos. Toda la interacción con la base de datos en Tainacan utiliza esta clase.
- [Custom Post types](https://wordpress.org/support/article/post-types/ ":ignore") y [taxonomías](https://codex.wordpress.org/Taxonomies ":ignore") - Todas las entidades de Tainacan, como las colecciones, los metadatos y los artículos, son tipos de entrada personalizados de WordPress, por lo que resulta útil comprender cómo se gestionan.
- [The Loop](https://developer.wordpress.org/themes/basics/the-loop/ ":ignore") - Uno de los principales elementos de WordPress utilizado para interactuar a través de los mensajes. Útil sobre todo si está retocando con temas.
- [Template Tags](https://developer.wordpress.org/themes/basics/template-tags/ ":ignore") - Funciones simples utilizadas por los desarrolladores de temas para mostrar contenido dinámico. Por lo general, estas funciones se utilizan dentro de "The Loop" y Tainacan implementa [sus propias etiquetas].(/dev/template-tags.md).
- [Template Hierarchy](https://developer.wordpress.org/themes/basics/template-hierarchy/ ":ignore") - Crucial si trabajas con temas.

</div>

---

## Development Resources

### Development Basics {docsify-ignore}

<div class="two-columns-list">

- [Setting up local environment](/dev/setup-local.md) - If you want to contribute to Tainacan core, you must set up your local environment. Alternatively, you can use our [Docker repository](https://github.com/tainacan/tainacan-docker ":ignore"). **If you want to develop themes or plugins, you don't need this**.
- [Key Concepts](/dev/key-concepts.md) - First things first. Let's understand what is what in Tainacan.
- [Tainacan Internals](/dev/internal-api.md) - Reference on Tainacan main classes and how to use them.
- [Tainacan Hooks](/dev/hooks.md) - Expand or modify different sections of code without modifying the plugin, using Actions and Filters, both in backend and frontend.
- [Tainacan API](https://tainacan.org/api-docs/ ":ignore") - A Rest JSON API which you can use to get content from a Tainacan database.
- [Roles and Capabilities](/dev/roles-capabilities.md) - Basic information about data privacy and access levels in Tainacan.

</div>

### More on Plugin Development {docsify-ignore}

<div class="three-columns-list">

- [Exporting and Exposing](/dev/exporting-and-exposing.md)
- [CSV Importer](/dev/csv-importer.md)
- [Vocabulary Importer](/dev/vocabulary-importer.md)
- [Mapping Standards](/dev/mapping-standards.md)
- [Repository Methods](/dev/repository-methods.md)

</div>

### Plugin Extension {docsify-ignore}

<div class="two-columns-list">

- [Creating a new Metadata Type](/dev/creating-metadata-type.md) - A guide for creating your custom Metadata Type
- [Creating a new Filters Type](/dev/creating-filters-type.md) - A guide for creating your custom Filters Type
- How to create [Exporters](/dev/exporter-flow.md), [Importers](/dev/importer-flow.md) and [Exposers](/dev/exposers.md)
- [Registering New Vue Components](/dev/registering-custom-vue-components.md) - Registering new Vue components that can be used by your plugin, such as metadata and filter types or extra view modes.
- [The Vue Items List Component](/dev/the-vue-items-list-component.md) - The clientside rendered items list that provides all power to faceted search.
- [Tweaking the Tainacan Admin UI](/dev/admin-ui-options.md) - Using a filter to set variables for customizing the Tainacan Admin panel.

</div>

### Theme Development or Extension {docsify-ignore}

<div class="two-columns-list">

- [Creating compatible themes](/dev/creating-compatible-themes.md) - An Introduction on how to create a theme that fully support Tainacan features
- [Tainacan Custom templates](/dev/custom-templates.md) - Custom templates for those that Tainacan adds to WordPress Template Hierarchy
- [Customizing the Items List](/dev/customizing-the-items-list.md) - Tweaking the appearence of the items list
- [Creating Extra View Modes](/dev/extra-view-modes) - How to create Extra View Modes that will be avaialble for displaying items list
- [Theme Gutenberg Support](/dev/theme-gutenberg-support.md) - Details to offer better support to the latest content block editor

</div>

### Configuration and performance {docsify-ignore}

<div class="three-columns-list">

- [Faceted Search](/dev/faceted-search.md)
- [Search Engine](/dev/search-engine.md)
- [Garbage Collector](/dev/garbage-collector.md)

</div>

---

## Other development contributions

<div class="three-columns-list">

- [Contributing Guidelines](/dev/CONTRIBUTING.md)
- [Tainacan release process](/dev/release.md)

</div>
