# Temas

Una de las razones por las que _WordPress_ es tan famoso y versátil es su diversidad de [temas](https://wordpress.org/themes/ ":ignorar"). Hay miles de temas que usted puede atribuir a su estilo del sitio y la estructura más formal, atractivo o minimalista. La gran mayoría son gratuitos y se instalan con un solo clic.

?> **Es posible utilizar el plugin Tainacan con cualquier tema activado**, pero la experiencia puede ser mejor con temas que ofrezcan compatibilidad para tus páginas.

En esta página hablamos de:

- Cuáles son [los temas que ofrecen la mejor compatibilidad](#temas-compatibles) para Tainacan y,
- [Cómo instalar y gestionar temas](#administración-de-temas-en-wordpress) en tu _WordPress_.

## Temas compatibles

Además de insertar un nuevo campo en tu panel de administración de _WordPress_, desde donde se accede al propio panel de administración de Tainacan, el plugin Tainacan también genera [páginas especiales](/es-mx/tainacan-pages.md) en tu sitio. Si tu tema ha sido pensado para presentar estas páginas, los listados de artículos y colecciones se mostrarán con todas las características de navegación de la colección como búsqueda de artículos, filtros, diferentes modos de vista, etc. De lo contrario, estos listados deberían ser muy parecidos a la forma en que el tema muestra las entradas del blog.

Desarrollar un tema compatible no es complicado y tampoco es necesario hacerlo desde cero, ya que muchos se pueden generar a partir de [temas hijo](https://developer.wordpress.org/themes/advanced-topics/child-themes/) de otros que ya existen. Aquí en la Wiki tenemos [una sesión entera](/es-mx/dev/creating-compatible-themes.md) dedicada a enseñar esto a los desarrolladores.

Actualmente, hay un tema desarrollado por la comunidad Tainacan y publicado en [repositorio oficial de WordPress](https://wordpress.org/themes/). Los demás están disponibles a través de GitHub. Para instalar los temas, accede al panel de instalación de temas de WordPress y sigue los pasos de la [sección de instalación](#administración-de-temas-en-wordpress).

### Interfaz Tainacan

Este es el tema estándar del proyecto Tainacan y está disponible en los repos oficiales de Wordpress [en este enlace](https://br.wordpress.org/themes/tainacan-interface/). Fue desarrollado por el mismo equipo de diseño que desarrolló la interfaz administrativa del plugin Tainacan, por lo que debería aportar la misma formalidad, con buena legibilidad y diseños que soporten grandes cantidades de información mostrada en la misma pantalla. Este tema es ideal para museos, galerías, bibliotecas y cualquiera que tenga un repositorio digital. Destacamos sus principales ventajas:

- Plantillas específicas para las listas de elementos Repositorio, Colección y Término, con varias configuraciones, entre ellas:
  - Sobrescribir el modo de vista por defecto para los listados de términos;
  - Ocultar varios elementos de control de búsqueda;
  - Cambiar el comportamiento de la barra de filtros, como su tamaño o si aparece oculta al principio;
- Plantilla específica para el listado de colecciones, con dos modos de vista, búsqueda por texto y ordenación;
- Plantilla específica para la página del artículo, con varias opciones, entre ellas:
  - Cambiar el orden en que se muestran los archivos adjuntos, los metadatos y el documento;
  - Mostrar la lista de metadatos en más de una columna;
  - Mostrar los archivos adjuntos como un carrusel e integrar el documento en esta misma lista;
  - Mostrar una cabecera personalizada que se asemeje a la colección;
  - Botón de descarga en el documento;
  - Navegación por los elementos (siguiente y anterior);
- Actualizaciones frecuentes y sincronizadas con las nuevas versiones del plugin Tainacan;
- Paleta de colores personalizable;
- Color de cabecera de cada colección personalizable dentro del plugin, cuando el tema está activo;
- Nuevo modo de vista "Miniatura";
- Botones de compartir para Facebook, Twitter, WhatsApp y Telegram en la mayoría de las páginas;
- Bloques Gutenberg estándar estilizados según la identidad visual del tema;
- Soporte de barra lateral;

![Algunas pantallas del tema Interfaz Tainacan](/_assets/themes-tainacan-interface.gif)

### Blocksy

El segundo más recomendado que mencionamos aquí no es un tema hijo, sino un tema popular [disponible en el repositorio de WordPress](https://wordpress.org/themes/blocksy/ ":ignore"). Su integración con Tainacan se realiza a través de un plugin, también disponible en [el repositorio de WordPress](https://wordpress.org/plugins/tainacan-blocksy/ ":ignore"). Teniendo tanto el plugin como el tema (o un tema hijo del mismo) activados, tendrás acceso a una serie de ajustes disponibles para el personalizador. Cubrimos estas opciones en detalle en [el post de lanzamiento](https://tainacan.org/en/blog/2021/06/14/using-the-blocksy-theme-with-tainacan/ ":ignore") y también es una buena idea revisar su [página oficial](https://creativethemes.com/blocksy/ ":ignore"). Para cubrir un poco sus características

- Plantillas específicas para el Repositorio, y listas de elementos de Términos, incluyendo configuraciones separadas para cada Colección, con varias configuraciones incluyendo:
  - Selección de diferentes paletas de colores;
  - Ocultar varios elementos de control de búsqueda;
  - Cambiar el comportamiento de la barra de filtros, como su tamaño o si aparece oculta al principio;
  - Ajustar un poco el diseño de la cabecera;
- Plantilla específica para la página del artículo de cada colección, con varias opciones, entre ellas:
  - Cambiar el orden en que se muestran los archivos adjuntos, los metadatos y el documento, incluyendo la posibilidad de tener dos columnas, con los archivos adjuntos a un lado de los metadatos;
  - Mostrar la lista de metadatos en más de una columna;
  - Dispaly etiquetas de metadatos aparte de sus valores;
  - Mostrar los archivos adjuntos como un carrusel e integrar el documento en esta misma lista;
  - Mostrar una cabecera personalizada que utilice la imagen destacada como banner;
  - Botón de descarga en el documento;
  - Navegación por artículos (siguiente y anterior);
  - Sección de elementos relacionados;
  - Cuadro para compartir personalizado;
- Paleta de colores personalizable;
- Botón desplegable automático "Más" añadido al menú cuando el número de elementos no cabe en la pantalla actual;
- Muchas otras opciones de diseño disponibles gracias a las características del tema;

![Algunas pantallas del tema Blocksy](/_assets/themes-blocksy.gif)

### Identidad gubernamental (IDG-WP)

Este tema de WordPress fue desarrollado por un equipo de voluntarios vinculados a la antigua Secretaría de Cultura de Brasil, con el objetivo de estandarizar varios sitios de WordPress utilizados por el gobierno federal. Un ejemplo es el propio sitio web de la [Secretaría de Cultura](http://cultura.gov.br/). El [tema original](https://github.com/culturagovbr/IDG-WP) en sí no tiene soporte para Tainacan, pero con la demanda de varios museos vinculados a Ibram para utilizarlo, se creó un _fork_, una variación del tema, en [otro repositorio](https://github.com/medialab-ufg/IDG-WP ":ignore"). Desgraciadamente, este proyecto está necesitado de mantenedores y puede presentar algunos problemas. Destacamos sus características:

- Plantillas específicas para las listas de elementos Repositorio, Colección y Término, pero sin imágenes de cabecera;
- Plantillas específicas para la página de artículos, incluido el carrusel de anexos;
- Integración estándar con la barra de enlaces y accesibilidad del Gobierno Federal;
- Compatibilidad con la mayoría de los bloques gutenberg;
- Dos ubicaciones del menú: la barra principal y el panel oculto junto a ella;
- Carrusel de noticias en la página de inicio;
- Personalización de sesiones en la página de inicio mediante plugins;

![Algunas pantallas del tema de IDG-WP](/_assets/themes-idg-wp.gif)

### Veganos (Tema hijo)

Creado para el proyecto [Covid-19 - UnB en Acción](http://repositoriocovid19.unb.br/ ":ignore"), se trata de un tema hijo del tema [Veganos](https://wordpress.org/themes/veganos/ ":ignore"), por lo que además de descargarlo desde su [repositorio](https://github.com/tainacan/tainacan-unb-covid-19 ":ignore") es necesario instalar el tema padre. Su característica más destacable es el formato "ondulado" de las imágenes de cabecera, entre otras:

- Plantillas específicas para las listas de elementos Repositorio, Colección y Término, incluyendo cabecera e imágenes estilizadas con algunos bordes y sombras;
- Plantillas específicas para las páginas de artículos, con metadatos listados antes del Documento y los adjuntos;
- Listado de entradas en bloques, en una lista de dos columnas;
- Botones estilizados con efecto ondulado;
- Paleta de colores personalizable
- Integración estándar con el portaenlaces y la accesibilidad del Gobierno Federal;
- Integración con la barra de menú de UnB (si no quieres usarla, sólo tienes que tirar de la [rama 'not-unb'](https://github.com/tainacan/tainacan-unb-covid-19/tree/not-unb ":ignore") de GitHub);

![Algunas pantallas del tema Veganos](/_assets/themes-veganos.gif)

### Rife Free (tema hijo)

Este es un [tema hijo](https://github.com/tainacan/rife-free-child ":ignore") del popular [tema Rife Free](https://wordpress.org/themes/rife-free/ ":ignore"). Tiene una dependencia de un plugin instalado, [Apollo13 Framework extensions](https://apollo13themes.com/rife/free ":ignore"), pero en compensación, trae muchas opciones de personalización, desde el formato de página y post hasta el comportamiento de la cabecera. Otros aspectos destacados son

- Plantillas específicas para las listas de elementos Repositorio, Colección y Término, incluyendo imágenes de cabecera;
- Plantillas específicas para la página de elementos, incluyendo los botones siguiente y anterior, que muestran sus miniaturas;
- Botón de desplazamiento a la parte superior;
- Paleta de colores diversa y personalizable;
- Animaciones y efectos de transición;
- Lista de artículos en bloques, opcionalmente en una lista de tres columnas;

![Algunas imágenes del Tema Rife Free](/_assets/themes-rife-free.gif)

### Twenty Twenty (tema hijo)

Cada año WordPress lanza un "tema oficial", que se activa por defecto en sus instalaciones y suele tener un diseño popular, con buena aplicación de los bloques gutenberg además de pruebas de accesibilidad y responsiveness. Para validar nuestras pruebas con el plugin, creamos un tema hijo de [TwentyTweny](https://wordpress.org/themes/twentytwenty/ ":ignore"), disponible [en este enlace](https://github.com/tainacan/TwentyTwentyChild ":ignore").

![Algunas imágenes del Tema Twenty Twenty](/_assets/themes-twentytwenty.gif)

---

## Administración de temas en Wordpress

### Video Tutorial: Instalación de temas (sólo en portugués)

<iframe
    width="560"
    height="513" 
    src="https://www.youtube.com/embed/oEl9bWe_rWI?start=780"
    frameborder="0"
    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
</iframe>

> Vea también cómo instalar el [plugin Tainacan](/es-mx/tainacan) para WordPress.

### Actualizar un tema

1. Acceda al panel de control de _WordPress_;
2. En el menú lateral izquierdo, haz clic en **Apariencia**;
3. Seleccione el submenú **Tema**;
4. En el bloque de cada tema aparece el mensaje "_Nueva versión disponible. Actualizar ahora_" aparece cada vez que se publica una nueva versión;
5. Haga clic en **Actualizar ahora** para recibir la última versión estable del Tema.

### Cambiar o eliminar el tema

1. Acceda al panel de control de _WordPress_.
2. En el menú lateral izquierdo, haga clic en `Apariencia`.
3. Selecciona el submenú `Tema`.
4. Para cambiar el tema actual, active otro tema de su elección
5. Para eliminar el tema haga clic en información del tema en el bloque del tema deseado
6. En la esquina inferior derecha, haga clic en `Eliminar`

!> **Warning**: To preserve the settings and navigability of items and collections, use themes compatible with good development practices for Tainacan.

!> **Atención**: Deshabilitar el tema Tainacan afecta a los ajustes de visualización y navegabilidad de los ítems y colecciones del repositorio. Esta operación sólo puede ser deshecha por los administradores.

!> **Atención**: Por seguridad, se recomienda siempre hacer una copia de seguridad de la instalación antes de cualquier modificación. Elimínela sólo si está seguro de que no se producirá una pérdida grave de información. Esta operación sólo puede revertirse restaurando copias de seguridad de la instalación.
