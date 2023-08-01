<div style="float: right; margin-left: 1rem;">
	<img 
		alt="Ícone de Ver no Tema" 
		src="/es-mx/_assets/images/icon_see.png"
		width="42"
		height="42">
</div>

?> _TODO_ Esta página está en _portugués brasileño_ solo hasta ahora. **Si puede, ayúdenos a traducirlo al _español_.**

# Páginas de Tainacan

Con el plugin Tainacan activado en el WordPress, el propio plugin crea las siguientes páginas especiales:

- Página de colecciones `/colecciones`;
- Página de Todos los elementos del repositorio `/elementos`;
- Páginas de elementos de una colección slug nombre-de-la-colección `/nombre-de-la-colección`;
- Páginas de elementos con algunos metadatos de taxonomía de slug _nombre-de-taxonomía_ que tienen un término de slug _nombre-de-término_ `/nombre-de-taxonomía/nombre-de-término`;

A medida que vayas creando colecciones, elementos y términos podrás acceder, automáticamente a estas direcciones desde el sitio web. Por lo general, en el panel administrativo de Tainacan, encontrará los enlaces a estas páginas en botones con íconos de ojos (como el que se encuentra en la parte superior derecha de esta página). Además, también es posible crear tus propias páginas presentando las colecciones o explicando algo sobre tu repositorio. Son dos caminos diferentes, pero que están a tu disposición gracias a la **integración de Tainacan con WordPress**. Más información a continuación:

- [Páginas Especiales Generadas por Tainacan](#as-páginas-especiais-do-Tainacan)
- [Creando tus propias páginas con bloques de Gutenberg](/es-mx/gutenberg-blocks)

## Las páginas especiales de Tainacan

![Conjunto de captura de telas exemplificando as páginas especiais do Tainacan, no  tema Tainacan Interface](/_assets/images/paginas_especiais_tainacan.png)

### Página de colecciones

`/colecciones` o `/collections`, si su instalación está en inglés.

Disponible en su sitio desde el momento en que se crea una colección, esta página enumera sus colecciones con opciones para ordenar, buscar, paginar y ver en tablas o tarjetas. Es una buena manera de brindarle al público una vista sistemática de las colecciones que existen en su repositorio.

### Página de elementos del repositorio

`/elementos` o `/items`, si su instalación está en inglés.

Disponible en su sitio desde el momento en que se crea un elemento en cualquier colección, esta página enumera **todos los elementos de todas las colecciones en el repositorio**. Presentará algunas vistas predeterminadas, opciones de clasificación por metadatos de nivel de repositorio y una lista de todos los filtros para todas las colecciones, además de un filtro de colecciones. Si bien el acceso a todos  los elementos es potente, _recomendamos que se utilice con precaución_. Filtrar por un metadato específico dentro de una colección, por ejemplo, ocultará de la lista los elementos que no tengan ese metadato, lo que puede resultar confuso para quienes no estén familiarizados con la organización de su repositorio.

### Páginas de elementos en una colección

`/nombre-de-la-colección`

Esta es generalmente la página más importante de una instalación de Tainacan. En él se tiene acceso a la búsqueda por facetas de elementos dentro de una colección. Destacamos los recursos disponibles:

- Encabezado de la colección (cuya imagen, color y descripción son configurables en el formulario de edición de la colección);
- Filtros (los mismos que están disponibles en el panel administrativo, siempre que sean públicos);
- Búsqueda de texto simple y búsqueda avanzada;
- Ordenar de forma ascendente o descendente en todos los metadatos públicos;
- Modos de visualización, incluido el modo de pantalla completa (también están habilitados o deshabilitados en el formulario de edición de la colección);
- Modal de URLs relacionadas, proporcionando acceso a la misma lista en diferentes formatos como JSON, HTML, CSV, PDF (si el [plugin](/es-mx/plugin-pdf-exposer) está instalado) y con la posibilidad de realizar mapeos;

|||||Observe que a lista de itens é então a página de uma coleção em si. Se você clicar em uma coleção na _Lista de Coleções_ do site ela irá para esta lista. Porém, você pode preferir ter uma [página customizada de apresentação](/es-mx/gutenberg-blocks), por exemplo, para só então redirecionar para sua lista de itens. Isto pode ser modificado também no formulário de configuração da sua coleção, na opção "Página de Capa".

### Páginas de Itens de um Termo

`/nome-da-taxonomia/nome-do-termo`

Similar à lista de itens de uma coleção, esta página mostra todos os itens que possuem algum metadado tipo taxonomia e que tenham neste metadado um termo específico. A principal diferença da lista da coleção é que o cabeçalho terá a imagem e descrição do termo, configurável no seu formulário de edição.

Esta página é uma excelente maneira de trazer o conceito de "Exposições" multi-coleção para o seu repositório. Por exemplo, se você tiver uma coleção de pinturas e uma coleção de arquitetura com diferentes metadados, mas tiver em ambos um metadado da Taxonomia **Movimento artístico**, você pode ver todos os itens do termo **Movimento renascentista** em um só lugar, agregando aí itens das duas coleções.
