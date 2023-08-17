# Bloques de elementos

Los bloques de elementos son una forma de mostrar una vista previa o lo más destacado de su colección, sin tener que exponer al usuario a toda la complejidad de la colección. [Lista de elementos con búsqueda por aspectos](/es-mx/tainacan-pages#páginas-de-elementos-de-una-colección). Actualmente, hay 4 bloques relacionados con artículos de Tainacan:

1. [Lista de elementos de la colección](#lista-de-elementos-de-la-colección) _(Dinâmico)_
2. [Carrusel de elementos](#carrusel-de-elementos)
3. [Barra de búsqueda Tainacan](#barra-de-búsqueda)
4. [Búsqueda por aspectos](#búsqueda-por-aspectos) _(A Lista de Itens Completa)_

---

## Lista de elementos de la colección

Este es uno de los bloques más importantes que ofrece Tainacan. Con él configuras una "Búsqueda de elementos" para que se muestren. Pero, ¿qué se entiende por búsqueda? En lugar de seleccionar los elementos uno por uno, usted determina los parámetros que filtrarán una lista de elementos. Por eso llamamos a este bloque una lista "dinámica" de elementos, porque si se añaden nuevos elementos a esa lista, tu bloque seguirá actualizándose. Véase más abajo:

### Ajustes iniciales del Bloque

![Seleccionar la colección en el bloque](/_assets/gifs/blocks-collection-items-1.gif)

En cuanto inserto el bloque, tengo que configurar mi búsqueda. Este proceso comienza determinando en qué colección concreta voy a buscar elementos. Una vez hecha esta elección, se me presenta mi lista de elementos, la misma que veo en el panel de administración de _Tainacan_. Los elementos que aparezcan en esta lista serán los que busque mi bloque. Aquí puedo cambiar, por ejemplo **filtros, orden de búsqueda, número de elementos buscados y ya aplicar una búsqueda textual simple**. Una vez hecho esto, esta información se guardará en la configuración de mi bloque y se mostrará la lista.

<div style="float: right; margin-left: 32px;">

![Lista de ajustes relacionadas con la cabecera de la colección](/_assets/images/blocks_collection_items_1.jpg ":size=200")

</div>

Con los elementos cargados, podemos realizar una serie de ajustes que estarán disponibles en el panel lateral cuando tengamos el bloque activo.

### Cabecera de colección

La primera opción le permite decorar un poco su bloque añadiendo una cabecera para su colección en la parte superior de la lista. Debería ser similar a lo que se ve en la página de elementos, pero una versión reducida, con la miniatura de la colección en el centro, la imagen de cabecera a la derecha y el nombre de la colección a la izquierda. Puede configurar el color de fondo de la cabecera, el texto y elegir si desea mostrar o no una etiqueta "Colección" antes del nombre de la colección.

### Barra de búsqueda Tainacan

Si ofreces una vista previa de tu lista de elementos pero no quieres impedir que el usuario siga explorándola, puedes ofrecer una barra de búsqueda en el propio bloque. Esta barra filtrará los elementos mostrados, cargando siempre como máximo la cantidad configurada para la búsqueda. Recuerde que los filtros que se hayan aplicado anteriormente seguirán aplicándose a esta lista, por lo que puede restringir lo que se muestra. La barra también le permite alternar la dirección de ordenación que haya elegido, como _ascendente_ o _descendente_, y cambiar de página si hay más elementos resultantes de su búsqueda.

![Cabecera de bloque y barra de búsqueda](/_assets/gifs/blocks-collection-items-2.gif)

### Ajustes de visualización de elementos

Por último, puede elegir cuántos elementos se mostrarán como máximo. El valor por defecto en los listados de Tainacan es siempre 12. A continuación, hay nuevos ajustes disponibles, y están directamente relacionados con el **cómo se muestran los elementos**. Sí, en los bloques también tenemos diferentes formas de visualizar la lista cargada de elementos. Esto se puede cambiar en el propio bloque, en la barra superior. Este bloque ofrece tres modos:

<!-- tabs:start -->

#### ** Rejilla de elementos **

El modo por defecto es la rejilla de artículos, que mostrará las miniaturas de los artículos (185px _x_ 185px), con sus títulos debajo. En este modo, puede configurar si desea mostrar o no el título del elemento y si desea más espacio entre los elementos. Recuerde que cuanto mayor sea el espaciado, menos elementos cabrán por línea.

![Configurar el bloque en modo cuadrícula](/_assets/gifs/blocks-collection-items-3.gif)

#### ** Lista de Elementos **

La lista de elementos permite una vista más simplificada, con miniaturas más pequeñas (54px _x_ 54px) y los títulos junto a ellas. En este modo, puedes elegir no mostrar la miniatura, lo que es ideal para colecciones que no tienen imágenes.

![Configuración del bloque en modo lista](/_assets/gifs/blocks-collection-items-4.gif)

#### ** Mosaico de elementos **

Desde [Tainacan 0.14 :link:](https://tainacan.org/blog/2019/11/22/tainacan-beta-0-14-e-tainacan-interface-1-6-novo-modo-mosaico-do-bloco-de-itens-e-suporte-ao-wordpress-5-3/ ":ignore"), también presentamos el modo mosaico. Este modo tiene varios ajustes adicionales. Es ideal para aquellos que desean ofrecer una visión más "artística" de su lista de colecciones. La composición montada por el mosaico es más irregular y no se limita a cortar las imágenes para montar varios **grupos de cuadrículas de artículos**. Los títulos sólo aparecen cuando se pasa el ratón por encima del artículo, pero pueden ocultarse del mismo modo que en el modo cuadriculado, al igual que el espaciado entre los artículos.

![Ajustando el bloque en modo mosaico](/_assets/gifs/blocks-collection-items-5.gif)

También puede configurar los siguientes detalles en el modo mosaico:

- La altura del bloque, a través del panel lateral o redimensionando el bloque;
- La cuadrícula utilizada para montar cada grupo del bloque (cuadrículas más grandes significan más elementos por grupo, por lo tanto más imágenes pequeñas);
- La densidad del grupo, es decir, el número de elementos por columna en cada grupo;

Estos detalles influirán en el tamaño del mosaico. Recuerde que cuantos más elementos, más densa será la composición.

![Más ajustes del bloque en el modo mosaico](/_assets/gifs/blocks-collection-items-6.gif)

Finalmente, un último detalle: al cortar las imágenes para encajarlas en sus cuadrículas, el mosaico siempre centra la imagen, vertical y horizontalmente. Quizá no quieras esto y prefieras, por ejemplo, que las imágenes se vean siempre en la parte superior (supongamos que tienes una colección de bustos de varias personas). Para ello, existe la opción _Punto focal de la imagen de fondo_.

<!-- tabs:end -->

---

## Carrusel de elementos

El salto de línea que la [Lista de elementos de la colección](#lista-de-elementos-de-la-colección) puede no ser del gusto de todos. Para presentar varios artículos en secuencia y dar a su publicación un aspecto más "dinámico", el bloque carrusel puede ser ideal.

### Ajustes iniciales del Bloque

![Selección de la colección en el bloque](/_assets/gifs/blocks-items-carousel-1.gif)

Al igual que con los ajustes del Bloque [Lista de elementos de la colección](#lista-de-elementos-de-la-colección#ajustes-iniciales-del-bloque) puede configurar una búsqueda para mostrar sus elementos en el carrusel. De esta forma, se buscarán dinámicamente según determinados parámetros de búsqueda, ordenación y filtrado que tú definas. Pero en este bloque también existe la posibilidad de elegir "a mano" qué elementos quieres mostrar. Tenga en cuenta que las opciones son excluyentes. Tiene que utilizar una estrategia u otra. En el caso de la selección manual de elementos, añades elementos a través del modal y los eliminas en la propia lista haciendo clic en el botón "X" que aparece encima del elemento insertado.

Con los elementos cargados, puede observar que el carrusel no se mueve. De hecho, sólo se activa en la versión publicada o de previsualización del post o página. Aquí, en el editor, verás una lista desplazable normal y corriente. Ahora podemos realizar una serie de ajustes que están disponibles en el panel lateral cuando tenemos el bloque activo.

### Cabecera de la colección

![Ver el carrusel en acción en el tema](/_assets/gifs/blocks-items-carousel-2.gif)

<div style="float: right; margin-left: 32px;">

![Lista de ajustes del carrusel de elementos](/_assets/images/blocks_items_carousel_1.png ":size=200")

</div>

La primera opción le permite decorar un poco su bloque añadiendo una cabecera para su colección en la parte superior de la lista. Debería ser similar a lo que se ve en la página de elementos, pero una versión reducida, con la miniatura de la colección en el centro, la imagen de cabecera a la derecha y el nombre de la colección a la izquierda. Puede configurar el color de fondo de la cabecera, el texto y elegir si desea mostrar o no una etiqueta "Colección" antes del nombre de la colección.

### Opciones del carrusel

Como em outros blocos, você pode escolher exibir ou não o título dos itens abaixo da miniatura. As demais opções disponiveis pelo carrossel estão relacionadas à sua reprodução. São elas:

- Loop Slides - Fazer com que, ao atingir o final da lista, o carrossel volte para o início;
- Auto Play - Reproduzir automaticamente o carrossel;
- Intervalo de tempo entre cada troca de item;
- Posição das Setas: De que maneira as setas de navegação do carrossel devem estar dispostas;

<br>

---

## Barra de Busca

Este bloco é um pouco diferente dos anteriores. Ao invés de mostrar uma prévia da lista completa de itens, ele te leva para a lista. Pode ser pensado como um atalho para a lista, com uma busca textual. O bloco te oferece basicamente uma barra de busca para estar disponível em sua publicação. Mas o interessante é que você pode configurar esta barra de diversas maneiras.

### Configurações Iniciais do Bloco

Para configurar o bloco é bem simples: Basta você escolher qual será o destino da sua busca: lista de itens do repositório ou lista de itens de uma coleção específica.

![Selecionando a origem da busca no bloco](/_assets/gifs/blocks-search-bar-1.gif)

### Alinhamento da Barra

Logo na parte de cima do bloco, ao lado das tradicionais opções de largura e disposição do bloco, temos três opções de allinhamento, que dizem respeito ao alinhamento da barra dentro do bloco. Por padrão, a barr está centralizada, mas pode ficar alinhada à esquerda ou direita.

### Estilos de Barra

Já no painel lateral, nas configurações do bloco, temos 3 estilos que podem ser aplicados.

- O estilo Padrão oferece uma barra simples de borda cinza e fundo branco;
- O estilo Alternativo, começa sem borda e com um fundo claro transparente. Seu tamanho é menor no início e fica maior ao se passar o mouse sobre a barra ou com um clique. Ao ficar ativa, uma borda branca é exibida;
- Por fim, o modesto estilo "Estiloso" começa apenas com um ícone e um botão largo arredondado, que se expande para mostrar o campo de busca;

![Estilos e alinhamento da barra de busca](/_assets/gifs/blocks-search-bar-2.gif)

### Opções Gerais da Barra

Escolhido o estilo, é possível determinar o quão larga a barra irá ficar em sua versão expandida (o valor é em porcentagem). Também podemos mudar o rótulo exibido na parte de dentro da barra para algo mais específico como "Digite aqui para procurar pinturas...".

Mas não precisamos parar por aí. De maneira similar ao Bloco [Lista de Itens da Coleção](#lista-de-itens-da-coleção) e [Carrossel de Itens](#carrossel-de-itens), neste bloco você pode exibir um cabeçalho da coleção. Você pode configurar a altura e a cor de fundo do cabeçalho, além da cor e tamanho do texto. Note que combinando estilos e alinhamentos diferentes, a sua barra e o cabeçalho sofrerão algumas alterações:

![Configurações do Cabeçalho da Coleção](/_assets/gifs/blocks-search-bar-3.gif)

!> A Barra de Busca é um dos raros blocos que não permite que haja mais de um do seu tipo inserido no documento. Quando criada uma, a opção de inserir nova estará desabilitada.

---

## Busca Facetada

A **Busca Facetada** é o bloco mais complexo que o plugin oferece. Com ele você exibe, em qualquer pagina ou post, a Lista de Itens completa tal como é vista na [Páginas de Itens](/es-mx/tainacan-pages#as-páginas-especiais-do-tainacan) do Tainacan, incluindo aí a possibilidade de aplicar filtros, fazer a busca avançada, trocar modos de visualização e ordenação, além de paginação. É uma maneira prática de oferecer todos estes recursos em uma página caso você esteja usando um Tema que não implementou suporte para estas páginas especiais que o plugin registra, ou queria customizar bastante o restante do template. Também é uma alternativa mais versátil ao `shortcode` que antes era sugerido para renderizar esta lista. Veja a seguir:

### Configurações Iniciais do Bloco

![Selecionando a coleção no bloco](/_assets/gifs/blocks-faceted-search-1.gif)

Ao inserir o bloco, devo configurar o origem da busca. Ela pode ser a lsita de todos os itens do repositório, a lista de itens de uma coleção ou a lista de itens associados a um termo. Nos dois últimos casos, um modal oferecerá as opções disponíveis para escolha. Feita esta configuração, uma figura ilustrativa irá aparecer onde a Lista será renderizada. Esta é apenas uma demonstração porque a lista completa é muito complexa para ser exibida dentro do editor, mas você pode ver os resultados pré-visualizando a página ou publicando-a.

De imediato é possível que você deseje dar mais espaço para a sua lista, o que pode ser configurado ajustando o bloco para ter **Largura Completa** ou **Largura Ampla**. No painel lateral dezenas de configurações podem ser encontradas. Detalhamos estas à seguir e damos abaixo três exemplos de resultados podem ser alcançados apenas fazendo estes ajustes neste bloco:

<div style="display: flex; align-items: center; justify-contents: space-evenly;">
<div style="margin: 0 12px">

![Exemplo da lista configurada 1](/_assets/images/blocks-faceted-search-2.jpg)

</div>
<div style="margin: 0 12px">

![Exemplo da lista configurada 2](/_assets/images/blocks-faceted-search-3.jpg)

</div>
<div>

![Exemplo da lista configurada 3](/_assets/images/blocks-faceted-search-4.jpg)

</div>
</div>

<!-- tabs:start -->

#### ** Área de Controle da Busca **

A área de controle da busca é como é chamada a barra horizontal que fica acima da região dos filtros e da lista de itens em si. Como vários controles ali disponíveis podem ser demais para o que você deseja mostrar neste bloco, a maioria das opções possibilita limitar alguns destes controles:

- **Esconder o campo de buscar**: esta opção esconde a barra de busca textual e o link de busca avançada juntos.
- **Esconder a busca avançada**: não mostra o link para a busca avançada.
- **Esconder o botão de "Metadados exibidos"**: deixa oculto o botão de "Metadados Exibidos". Vale notar que este botão só está visível na lista caso o modo de visualização atual permita esta exibição, como por exemplo a Tabela e as Fichas.
- **Esconder a região de ordenação**: esconde os _dropdowns_ relacionados ao sentido de ordenação e ao metadado pelo qual a lista é ordenada.
- **Esconder o botão "Ordenar por"**: esconde apenas o _dropdown_ onde são listados diferentes metadados pelos quais se ordena a busca.
- **Mostrar opções de Modos de Visualização em linha**: Ao invés de exibir um _dropdown_ com as opções dos modos de visualização, com esta configuração são exibidos apenas ícones um ao lado do outro para o usuário escolher.
- **Mostrar o modo de visualização "Galeria" (tela cheia) junto com os demais modos de visualização**: por padrão este modo fica listado como um botão ao lado das opções de visualização. Com esta configuração esta diferenciação deixa de existir.
- **Esconder botão "Ver como..."**: faz com que o botão "Ver como..." também chamado de botão de expositores ou links alternativos não apareça. Este botão é responsável por abrir um modal com opções de compartilhamento e acesso da lista de itens em diferentes formatos.
- **Modo de visualização padrão forçado para listas de itens de termos ou repositório**: Diferentemente das coleções, lista de itens de termos ou do repositório possuem um modo de visualização padrão definido pelo sistema: o Mosaico. Com esta opção pode se configurar qual será o modo de visualização inicial.
- **Modos de visualização disponíveis na lista**: Nas coleções, estas opções vem da própria configuração da coleção, e nos temos e repositório, vem do sistema. Aqui podem ser habilitados ou desabilidados por completo alguns modos de visualização para seu tema. Se apenas um modo permanecer ativo, este será o padrão e nenhum botão de selecionar modo de visualização será disponibilizado.
- **Mostrar o botão de filtros na barra de controle**: Exibe o botão de mostrar ou esconder filtros dentro da própria barra de controle da busca.

#### ** Área dos Filtros **

A área de filtros, por padrão, é um painel lateral presente ao lado da lista de itens. Estas opções permitem alterar um pouco do seu comportamento.

- **Esconder filtros**: oculta por completo a barra, sem ter como acessá-la neste bloco.
- **Esconder o botão "Esconder filtros"**: não oferece a opção de ocultar a barra de filtros para o usuário.
- **Começar com filtros escondidos**: faz com que de início o painel de filtros comece escondido, mas ainda podendo ser chamado pelo botão de "Exibir/esconder filtros";
- **Renderizar lista de filtros como uma modal**: mostra os filtros como uma modal de tela cheia ao invés de um painel lateral, sobrepondo-se a lista de itens.

#### ** Área de Paginação **

A paginação é essencial para não pesar a busca com listas de resultados muito grandes. Por padrão, é controlada na barra que fica abaixo da lista de itens, mostrando 12 itens por vez, à menos que configurada de maneira diferente pelo usuário.

- **Esconder a área de paginação**: esconde por completo os controles de paginação, permitindo que apenas uma página seja vista neste bloco, a inicial.
- **Esconder botão "Itens por página"**: oculta o botão onde se seleciona quantos itens por página devem ser exibidos.
- **Esconde o botão "Ir para a página:"**: esconde o botão que permite pular facilmente de uma página para a outra.
- **Número padrão de itens por página**: útil especialmente se alguns dos controles acima foi escondido, aqui pode ser definida a quantidade de itens por página que é carregada, forçando o valor sobre aquele configurado pelo usuário.

#### ** Cores e Tamanhos **

Para além do comportamento e presença de certos elementos no bloco, é possível também configurar a cor de vários componentes da interface, e outras configurações mais estéticas:

- **Tamanho base da fonte**: por padrão todos os elementos da interface são escalados a partir de uma fonte de _16px_. Nesta opção pode-se aumentar ou diminuir este valor para se melhorar a legibilidade da sua lista.
- **Largura do painel de filtros**: O painel de filtros ocupa uma largura máxima de _20%_ da lista de itens (e mínima de _154px_). Nesta configuração pode-se alterar este valor, dando mais ou menos espaço para os filtros.
- **Cor de fundo**: A cor de fundo da lista de itens como um todo;
- **Cor de links e estados ativos**: Na interface, links e alguns ícones aparecem coloridos com uma cor para indicar seu estado ativo. Por padrão esta cor é o _Azul Turquesa_ do Tainacan, mas pode ser configurado por temas para outras cores. Com esta configuração você pode sobrescrever este valor;
- **Cor de fundo de tooltips**: Em geral a cor de links é muito escura para mostrar os tooltips (os balõezinhos que possuem ficas ou resumos de conteúdo). Nesta configuração, pode ser escolhida uma cor mais clara, que sirva para esta função. Isso também afeta o botão de "Esconder Filtros".
- **Cor de fundo dos campos**: esta é a cor que aparecerá no fundo de campos de texto e outros elementos da interface relacionados à entrada de dados. Por padrão é a mesma do plano de fundo e pode ser alterada para uma cor de maior destaque.
- - **Cor de texto dos campos**: esta é a cor que aparecerá no conteúdo de campos de texto e outros elementos da interface relacionados à entrada de dados.
- **Cor da borda dos campos**: a cor da borda de campos de texto, checkbox e similares.
- **Cor dos rótulos**: a cor dos rótulos de campos na interface, tais como os nomes dos filtros.
- **Cor dos cabeçalhos**: a cor dos cabeçalhos, ou seja, dos rótulos principais, tais como os nomes do itens e o indicador da sessão dos filtros.
- **Cor geral de informações**: esta cor por padrão é um cinza utilizado para informações secundárias na interface. Por exemplo, os valores de metadados de menor importância e os ícones dos botões de controle da busca.
- **Cor de fundo dos itens**: a cor de cada unidade item na lista, por padrão é a mesma da cor de fundo.
- **Cor de fundo dos itens com o mouse em cima**: a cor de cada unidade item da lista quando o mouse está sobre ele.
- **Cor de fundo do cabeçalho do item com o mouse em cima**: alguns itens possuem uma cor de destaque para o cabeçalho do seu modo de visualização (como o cartões, por exemplo). Nestes casos, esta será a cor que aparecerá nesta região do item com o mouse acima do mesmo.

<!-- tabs:end -->

!> A Busca Facetada é um dos blocos que não permite que haja mais de um do seu tipo inserido no documento. Quando criada uma, a opção de inserir nova estará desabilitada. Isto ocorre porque ao se realizar qualquer busca a URL do site é complementada com os parâmetros que causariam conflito entre diferentes listas.

---
