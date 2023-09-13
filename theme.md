# Temas

Una de las razones por las que _WordPress_ es tan famoso y versátil es su diversidad de [temas](https://wordpress.org/themes/ ":ignorar"). Hay miles de temas que usted puede atribuir a su estilo del sitio y la estructura más formal, atractivo o minimalista. La gran mayoría son gratuitos y se instalan con un solo clic.

?> **Es posible utilizar el plugin Tainacan con cualquier tema activado**, pero la experiencia puede ser mejor con temas que ofrezcan compatibilidad para tus páginas.

En esta página hablamos de:

- Cuáles son [los temas que ofrecen la mejor compatibilidad](#temas-compatibles) para Tainacan y,
- [Cómo instalar y gestionar temas](#manage-themes) en tu _WordPress_.

## Temas compatibles

Además de insertar un nuevo campo en tu panel de administración de _WordPress_, desde donde se accede al propio panel de administración de Tainacan, el plugin Tainacan también genera [páginas especiales](/es-mx/tainacan-pages.md) en tu sitio. Si tu tema ha sido pensado para presentar estas páginas, los listados de artículos y colecciones se mostrarán con todas las características de navegación de la colección como búsqueda de artículos, filtros, diferentes modos de vista, etc. De lo contrario, estos listados deberían ser muy parecidos a la forma en que el tema muestra las entradas del blog.

Desarrollar un tema compatible no es complicado y tampoco es necesario hacerlo desde cero, ya que muchos se pueden generar a partir de [temas hijo](https://developer.wordpress.org/themes/advanced-topics/child-themes/) de otros que ya existen. Aquí en la Wiki tenemos [una sesión entera](/es-mx/dev/creating-compatible-themes.md) dedicada a enseñar esto a los desarrolladores.

Actualmente, hay un tema desarrollado por la comunidad Tainacan y publicado en [repositorio oficial de WordPress](https://wordpress.org/themes/). Los demás están disponibles a través de GitHub. Para instalar los temas, accede al panel de instalación de temas de WordPress y sigue los pasos de la [sección de instalación](#manage-themes).

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

![Algunas pantallas del tema Interfaz Tainacan](/_assets/gifs/themes-tainacan-interface.gif)

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

![Algunas pantallas del tema Blocksy](/pt-br/_assets/gifs/themes-blocksy.gif)

### Identidad gubernamental (IDG-WP)

This WordPress theme was developed by a team of volunteers linked to the former Brazilian Ministry of Culture, with the objective of standardizing several WordPress sites used by the federal government. One example is the [Secretariat of Culture](http://cultura.gov.br/) website itself. The [original theme](https://github.com/culturagovbr/IDG-WP) itself does not have support to Tainacan, but with the demand of several museums linked to Ibram to use it, was created a _fork_, a variation of the theme, in [another repository](https://github.com/medialab-ufg/IDG-WP ":ignore"). Unfortunately, this project is in need of maintainers and may present some problems. We highlight its characteristics:

- Specific templates for the Repository, Collection and Term item lists but no header images;
- Specific templates for the item page, including attachment carousel;
- Standard integration with the Federal Government's link bar and accessibility;
- Support for most gutenberg blocks;
- Two menu locations: the main bar and the hidden panel next to it;
- News carousel on the home page;
- Customization of sessions on the home page via plugins;

![Some screens from IDG-WP theme](/pt-br/_assets/gifs/themes-idg-wp.gif)

### Veganos (Child Theme)

Created for the project [Covid-19 - UnB in Action](http://repositoriocovid19.unb.br/ ":ignore"), this is a theme son of the theme [Veganos](https://wordpress.org/themes/veganos/ ":ignore"), therefore, besides downloading it from its [repository](https://github.com/tainacan/tainacan-unb-covid-19 ":ignore") it is also necessary to install the parent theme. Its most remarkable feature is the "wavy" format of the header images, among others:

- Specific templates for the Repository, Collection and Term item lists including header and stylized images with some borders and shadows;
- Item page specific templates, with metadata listed before the Document and attachments;
- Listing of posts in blocks, in a two-column list;
- Stylized buttons with wavy effect;
- Customizable color palette
- Standard integration with the Federal Government's link holder and accessibility;
- Integration with the UnB menu bar (if you don't want to use it, just pull from the [branch 'not-unb'](https://github.com/tainacan/tainacan-unb-covid-19/tree/not-unb ":ignore") of GitHub);

![Some screens from Veganos theme](/pt-br/_assets/gifs/themes-veganos.gif)

### Rife Free (Child theme)

This is a [child theme](https://github.com/tainacan/rife-free-child ":ignore") from the popular [Rife Free theme](https://wordpress.org/themes/rife-free/ ":ignore"). It has a dependency on an installed plugin, [Apollo13 Framework extensions](https://apollo13themes.com/rife/free ":ignore"), but in compensation, it brings many customization options, from page and post format to header behavior. Other highlights are

- Specific templates for the Repository, Collection and Term item lists including header images;
- Specific templates for the item page, including next and previous buttons, which show their thumbnails;
- Scroll button to the top;
- Diverse and customizable color palette;
- Animations and transition effects;
- List of posts in blocks, optionally in a list of three columns;

![Algumas telas do Tema Rife Free](/pt-br/_assets/gifs/themes-rife-free.gif)

### Twenty Twenty (Child theme)

Every year WordPress releases an "official theme", which is activated by default in its installations and usually has a popular design, with good application of gutenberg blocks in addition to accessibility and responsiveness tests. To validate our tests with the plugin, we created a child theme of [TwentyTweny](https://wordpress.org/themes/twentytwenty/ ":ignore"), available [at this link](https://github.com/tainacan/TwentyTwentyChild ":ignore").

![Algumas telas do Tema Twenty Twenty](/pt-br/_assets/gifs/themes-twentytwenty.gif)

---

## Manage themes on Wordpress

### Video Tutorial: Installing Themes (Portuguese only)

<iframe
    width="560"
    height="513" 
    src="https://www.youtube.com/embed/oEl9bWe_rWI?start=780"
    frameborder="0"
    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
</iframe>

> See also how to install the [Tainacan plugin](/tainacan) for WordPress.

### Update a theme

1. Access the _WordPress_ Control Panel;
2. In the left side menu, click on **Appearance**;
3. Select the submenu **Theme**;
4. In the block of each theme the message "_New version available. Update now_" is displayed whenever a new version is released;
5. Click **Update Now** to receive the last stable version of the Theme.

### Change or Delete the Theme

1. Access the _WordPress_ Control Panel
2. In the left side menu, click on `Appearance`
3. Select the `Theme submenu`
4. To change the current theme, activate another theme of your choice
5. To delete the theme click on theme information in the desired theme block
6. In the lower right corner click `Delete`

!> **Warning**: To preserve the settings and navigability of items and collections, use themes compatible with good development practices for Tainacan.

!> **Warning**: Disabling the Tainacan theme affects the display and navigability settings for items and collections in the repository. This operation can only be undone by administrators.

!> **Warning**: For safety, it is always recommended to backup the installation before any modification. Delete the subject only if you are sure that there will be no serious loss of information. This operation can only be reversed by restoring backups of the installation.
