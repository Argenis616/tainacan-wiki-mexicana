# Tainacan para desarrolladores

Como saben, **Tainacan es un plugin de [WordPress](https://wordpress.org)** y está construido sobre esta conocida plataforma. Si estás familiarizado con _WordPress_ debería serte fácil entender cómo está organizado Tainacan, cómo interactúa con la base de datos y cómo construir tus propias funcionalidades a partir de él.

## Bueno, pero yo soy nuevo en WordPress

Si no tienes experiencia con WordPress y te gustaría desarrollar un plugin para Tainacan, o incluso contribuir al plugin, es una buena idea aprender algunos fundamentos. Éstos serán útiles para todo lo que tratará mientras trabaja con Tainacan.

Esta es una lista no exhaustiva de los temas más importantes que deberías investigar:

<div class="two-columns-list">

- [WP_Query](https://developer.wordpress.org/reference/classes/wp_query/ ":ignore") class - Este es el corazón de WordPress, la clase que le da la interfaz para consultar las entradas en la base de datos. Toda la interacción con la base de datos en Tainacan utiliza esta clase.
- [Custom Post types](https://wordpress.org/support/article/post-types/ ":ignore") y [taxonomías](https://codex.wordpress.org/Taxonomies ":ignore") - Todas las entidades de Tainacan, como las colecciones, los metadatos y los artículos, son tipos de entrada personalizados de WordPress, por lo que resulta útil comprender cómo se gestionan.
- [The Loop](https://developer.wordpress.org/themes/basics/the-loop/ ":ignore") - Uno de los principales elementos de WordPress utilizado para interactuar a través de los mensajes. Útil sobre todo si está retocando con temas.
- [Template Tags](https://developer.wordpress.org/themes/basics/template-tags/ ":ignore") - Funciones simples utilizadas por los desarrolladores de temas para mostrar contenido dinámico. Por lo general, estas funciones se utilizan dentro de "The Loop" y Tainacan implementa [sus propias etiquetas].(/dev/template-tags.md).
- [Template Hierarchy](https://developer.wordpress.org/themes/basics/template-hierarchy/ ":ignore") - Crucial si trabajas con temas.

</div>

---

## Recursos para el desarrollo

### Fundamentos del desarrollo {docsify-ignore}

<div class="two-columns-list">

- [Configuración del entorno local](/dev/setup-local.md) - Si quieres contribuir al núcleo de Tainacan, debes configurar tu entorno local. Alternativamente, puede utilizar nuestro [repositorio Docker](https://github.com/tainacan/tainacan-docker ":ignore"). **Si quieres desarrollar temas o plugins, no necesitas esto**.
- [Conceptos clave](/dev/key-concepts.md) - Lo primero es lo primero. Entendamos qué es qué en Tainacan.
- [Interiores de Tainacan](/dev/internal-api.md) - Referencia sobre las principales clases de Tainacan y cómo utilizarlas.
- [Ganchos de Tainacan](/dev/hooks.md) - Amplíe o modifique diferentes secciones de código sin modificar el plugin, utilizando Acciones y Filtros, tanto en el backend como en el frontend.
- [API de Tainacan](https://tainacan.org/api-docs/ ":ignore") - Una API Rest JSON que puede utilizar para obtener contenido de una base de datos Tainacan.
- [Roles y capacidades](/dev/roles-capabilities.md) - Información básica sobre privacidad de datos y niveles de acceso en Tainacan.

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
