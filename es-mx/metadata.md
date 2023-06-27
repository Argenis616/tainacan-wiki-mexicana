<div style="float: right; margin-left: 1rem;">
	<img 
		alt="Ícone de Metadados" 
		src="/_assets/images/icon_metadata.png"
		width="42"
		height="42">
</div>

?> _TODO_ Esta página está en _portugués brasileño_ solo hasta ahora. **Si puede, ayúdenos a traducirlo al _español_.**

# Metadatos

En Tainacan, los _"elementos"_ se organizan a través de _"colecciones"_ y cada _"colección"_, puede tener _"metadatos"_ específicos o compartir _"metadatos"_ entre sí.  Los "metadatos" se utilizan para describir los _"elementos"_ con vistas a la recuperación.

>Los _"metadatos"_ definen las características, parámetros y especificidades de la información que se insertará junto con el documento digital durante el envío de _"elementos"_ a las _"colecciones"_. Es similar, por ejemplo, a la configuración de los campos que formarán parte de un _“formulario"_, o a los campos de una _“ficha de museo”_.

Cada _“metadato”_ tiene un conjunto de configuraciones posibles: ¿Es un _“metadato obligatorio”_? ¿Sus _"valores"_ son únicos para cada _"elemento"_ (como en el caso del número de inventario, por ejemplo)? ¿Acepta _“valores múltiples”_ (varios autores, por ejemplo)?

En este artículo, describimos:

- Las [características generales de los metadatos](#características-gerais-de-metadados), presentes em todos os tipos;
- Cómo crear metadatos, ya sea [nivel de repositório](#criar-metadados) o [nivel de colección](#criar-metadados-à-nível-de-coleções);
- Los [tipos de metadatos](#tipos-de-metadados) y sus particularidades;
- Cómo [editar metadatos](#editar-metadados) existentes;
- Cómo [eliminar metadatos](#excluir-metadados);

En otros artículos, también puedes ver información relevante como:

- Cómo organizar largas listas de metadatos con la función [Secciones de metadatos](/es-mx/metadata-sections.md);
- Cómo editar varios metadatos a la vez con [Acciones Masivas](/es-mx/bulk-actions.md);
- Cómo importar y exportar _“metadatos predefinidos”_. [Ver Importadores](/es-mx/importers.md);

---

## Características generales de los metadatos

- Por defecto, todas las _"colecciones"_ tienen los _"metadatos"_ de _"Título"_ y _"Descripción"_, que no se pueden borrar, pero pueden _"editarse" o"deshabilitarse"_. Estos _"metadatos"_ se utilizan en algunos listados dentro de Tainacan para representar el _"elemento"_;
- _“Metadatos heredados”_ que pueden ser _“habilitados"_ o _"deshabilitados"_, lo que implica que se van a mostrar para ser llenados al enviar un nuevo _"elemento"_ o no, y también su presencia o ausencia (con sus respectivos datos) durante la visualización de las _"colecciones"_ y de los _"elementos"_;
- **Los _“metadatos a nivel de repositorio”_ son heredados por todas las _"colecciones"_** del repositorio. Aparecen marcados con “_heredado_” delante del nombre;
- Una vez que se ha creado un metadato, no se puede cambiar su tipo. Por ejemplo, no se puede cambiar un metadato del tipo _"Texto"_ a _"Texto largo"_, o _"Numérico"_ o a _"Fecha"_, después de su creación;
- Los _"metadatos"_ que no han sido heredados del repositorio se pueden eliminar y muestran un "icono de papelera" delante de ellos. Ver [eliminar metadatos](#excluir-metadados) para obtener más información.

Tainacan no tiene una _“plantilla o modelo de metadatos predeterminado”_, sino diferentes _"tipos de metadatos"_ que pueden elegirse para satisfacer las necesidades del usuario durante la configuración de su colección digital. La correcta elección del _“tipo de metadato”_ ayudará al llenado de la información y, en consecuencia, en la recuperación más precisa de los _"elementos"_.

Los _"metadatos"_ pueden crearse automáticamente durante la importación masiva de datos, o manualmente durante la creación de la _"colección"_ mediante el _"panel administrativo"_.

## Crear metadatos

Los _"metadatos"_ pueden crearse manualmente a nivel de ""repositorio" o a nivel de "colección"". Los _"metadatos"_ creados a nivel de _"repositorio"_ son heredados por todas las _"colecciones"_.

Los _“metadatos a nivel de repositorio"_ deben estar pensados para permitir la inserción de información global, es decir, común al menos a una gran parte del repositorio. Por ejemplo: _“Número de registro”_, _“Tipo de archivo”_, _“Fecha de registro del elemento”_, _“Estado de conservación”_, etc.

Las nuevas _"colecciones"_ también pueden crearse con una plantilla de _"metadatos predefinidos"_ o importarse de fuentes externas. Las _"colecciones"_ creadas con _"metadatos predefinidos"_ se basan en un conjunto de _"metadatos predefinidos"_ durante su creación, y pueden gestionarse del mismo modo que otras _"colecciones"_.

​Desde la versión 0.6 de Tainacan, hay una opción para crear _"colecciones"_ con un conjunto de _"metadatos"_ del modelo _“Dublin Core”_.

Se pueden desarrollar nuevos conjuntos de _"metadatos"_ según las necesidades individuales de cada instalación, y/o añadirlos a Tainacan. Consulta [Desarrollo de plugins](/dev/) para conocer más información sobre el desarrollo de Tainacan.

1. Inicia sesión en WordPress con tu _"nombre de usuario"_ y _"contraseña"_;

   ![Acesse o painel de controle](_assets\images\050.png)

2. En el _“panel administrativo”_ da clic en _“Tainacan”_;

   ![Acesse o painel de controle](_assets\images\051.png)

3. Da clic en _“Metadatos del repositorio”_;

   ![Acesse o painel de controle](_assets\images\070.png)

4. Para crear un nuevo metadato, simplemente elige el _“tipo de metadato”_ del listado que aparece en la columna de la derecha, arrástralo y suéltalo al final de la lista de metadatos que ya están creados. El nuevo metadato aparecerá en último lugar de la lista de metadatos del repositorio.  También puedes utilizar la función de arrastrar y soltar para _“ordenar los metadatos”_ durante su creación.

## Crear metadatos a nivel de colección

- Los "metadatos" a nivel de "colección" solo se aplican a los "elementos" creados en esta "colección". Se aplican también en las colecciones "hijas" de esta colección;
- Crea o elige la "colección" en la que deseas "crear nuevos metadatos". Consulta Crear colección para obtener más información;

1. Inicia sesión en WordPress con tu _"nombre de usuario"_ y _"contraseña"_;

   ![Acesse o painel de controle](_assets\images\050.png)

2. En el _“panel administrativo”_ da clic en _“Tainacan”_;

   ![Acesse o painel de controle](_assets\images\051.png)

3. Crea una _"colección"_ como se indica en la sección _“Crear colecciones”_;

4. Entra a la _“colección”_ que creaste y haz clic en _“Metadatos”_;

   ![Acesse o painel de controle](_assets\images\064.png)

5. Para _"crear nuevos metadatos"_, simplemente elige el tipo de metadato que quieres crear y arrástralo a la lista de la izquierda, donde ya están los _“metadatos por defecto”_ de la colección.  El nuevo metadato aparecerá en último lugar en esta lista. También puedes utilizar la función de arrastrar y soltar para acomodar los metadatos en el orden que prefieras. Ver [tipos de metadatos](https://tainacan.github.io/tainacan-wiki/#/es-mx/metadata?id=tipos-de-metadados)[Tipos de metadados](https://tainacan.github.io/tainacan-wiki/#/es-mx/metadata?id=tipos-de-metadados) para conocer cuál es el _“metadato”_ más adecuado para cada tipo de información;

6. Cada _“metadato”_ tiene que configurarse individualmente, eligiendo los ajustes y funciones posibles. A continuación describimos las funciones generales que se pueden configurar en prácticamente todos los metadatos. Consulta el área de metadatos para aprender a utilizar ajustes específicos (enlace);

   ![Acesse o painel de controle](_assets\images\071.png)

   **“Nombre”**: Aquí hay que escribir el nombre del metadato, por ejemplo: _“Título”_, _“Creador”_, _"Estado de conservación"_, etc;

   **“Descripción”**: Breve descripción, útil para describir o explicar cómo debe llenarse este metadato. Durante el llenado, quien esté capturando la información podrá ver la descripción si pasa el cursor sobre el signo de interrogación que está al lado del metadato;

   ![Acesse o painel de controle](_assets\images\descricao_metadado.png)

   **“Marcador de posición”**: Campo utilizado por metadatos con campo de texto para dar una breve instrucción sobre cómo llenarlo. Se trata de un mensaje sencillo que aparecerá dentro del campo de texto y que puede indicar al usuario qué tipo de información se espera. Por ejemplo: _“Escriba su nombre completo aquí…”_.

   **“Estado”**: Determina el nivel de privacidad del metadato, es decir, nos permite configurar metadatos que solo estarán visibles para los administradores de la colección, pero no para los visitantes. Es muy útil cuando se registra información sensible (por ejemplo, avalúos, datos de localización de las otras, etc.) También nos sirve para configurar información que solo podrán ver quienes tengan un rol específico en la colección. Ver [Permisos de usuario](https://tainacan.github.io/tainacan-wiki/#/es-mx/users)[Permissões de Usuários](https://tainacan.github.io/tainacan-wiki/#/es-mx/users) para más detalle. Los dos estados que pueden configurarse son;

   ​ ■ “Público”: Se muestran junto con el _“elemento”_, dependiendo del nivel de privacidad de este _“elemento”_ y de la _“colección”_ a la que pertenece;

   ​ ■ “Privado”: solo se muestra a los administradores, editores y moderadores de la _"colección"_. Ver [Permisos de usuario](https://tainacan.github.io/tainacan-wiki/#/es-mx/users)[Permissões de Usuários](https://tainacan.github.io/tainacan-wiki/#/es-mx/users) para conocer más detalle.

   **“Mostrar en listado”**: Determina si el _“metadato”_ se muestran por defecto en la vista previa de los ítems:

   ​ ■ “Mostrar por defecto”: los _“metadatos”_ se muestran por defecto en la página de vista de la _“colección”_ (dependiendo del tipo de vista previa) y en la vista previa del _“elemento”_;

   ​ ■ “No mostrar por defecto”: los _“metadatos”_ no se muestran de forma predeterminada en la vista de _“colección”_, pero el usuario puede seleccionarlos para que se muestren en la página de la colección (dependiendo del tipo de vista) y también en la vista previa del _“elemento"_;

   ​ ■ “No mostrar nunca”: los _“metadatos”_ no se muestran en la vista previa de la _“colección”_ ni pueden ser selecciondos por el usuario para mostrarse en esta vista previa. De cualquier forma, los metadatos son visibles en la vista previa del elemento. Hay que cambiar el _“estado del metadato”_ para cambiar su nivel de privacidad.

   **“Opciones de llenado”**:

   ​ ■ “Obligatorio”: determina si es obligatorio llenar este “metadato”. Si no se ha llenado un metadato obligatorio, no se puede enviar el elemento a la colección;

   ​ ■ “Único o Múltiple”: Determina si los “metadatos” permiten la inserción de un solo valor o de múltiples valores, como, por ejemplo, “metadatos” sobre “Color”, “Material”, etc;

   ​ ■ “Valor único”: indica que el valor ingresado en este metadato no debe repetirse en otros “elementos” del repositorio (para “metadatos” creados a nivel de repositorio) o en la misma “colección” (para “metadatos creados a nivel de colección”).

   **“URL semántica”**: URL de la descripción semántica del _“metadato”_. Su configuración es opcional;

   Dependiendo del _“tipo de metadato”_, puede haber otras especificaciones para configurar. Ver[tipos de metadatos](https://tainacan.github.io/tainacan-wiki/#/es-mx/metadata?id=tipos-de-metadados) para más detalles.

7. Después de completar y configurar los metadatos, da clic en _“Guardar”_, o en _"Cancelar"_ para abortar la misión. Una vez guardados, los _“metadadatos”_ creados aparecerán como un campo a rellenar al enviar y editar nuevos _"elementos"_.

## Tipos de Metadatos

A continuación, describimos cada uno de los _"tipos de metadatos"_ disponibles y sus configuraciones.

### Texto sin formato

Conocido también como _“texto corto”_, se recomienda el uso de este metadato para información que consista en un texto breve en formato libre y sin saltos de línea. No tiene un número límite de caracteres, pero solo permite insertar un texto corrido, sin separación de párrafos;

![Acesse o painel de controle](_assets\images\066.png)

### Área de texto

Conocido también como _“texto largo”_, este metadato se usa para insertar texto en formato libre. Permite la inserción de párrafos;

![Acesse o painel de controle](_assets\images\067.png)

### Fecha

Para _"metadatos"_ de fechas completas en el formato _“DD/MM/AAAA”_. Si no tiene la fecha completa, se sugiere elegir otros campos para ingresar fechas, como _"metadato numérico"_ o _"metadato de texto corto"_. Cuando se usa el metadato de tipo _“fecha”_, permite la recuperación de _"elementos"_ por intervalos de tiempo en dos tipos de filtros. Revisa los filtros disponibles para cada tipo de metadatos para obtener más información;

![Acesse o painel de controle](_assets\images\076.png)

### Numérico

Para _"metadatos"_ que contienen solo números. Este tipo de _“metadato”_ permite la recuperación de _"elementos"_ por intervalos. Revisa los filtros disponibles para cada tipo de metadatos para obtener más información;

​■**Ajustes adicionales**

Intervalos: Puede configurar la cantidad a incrementar/decrementar haciendo clic en los botones de control mientras completa el formulario del _“metadado”_. Por ejemplo: si utilizas un _“metadato numérico”_ como "Década", puedes establecer el cambio de intervalo en 10. En el llenado, al hacer clic en las flechas, el valor se incrementará de 10 en 10.

<iframe    width="560"    height="513"     src="https://www.youtube.com/embed/_hRrB6wVY7k" title="YouTube video player"    frameborder="0"    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"    allowfullscreen></iframe>

### Lista de selección

Se usa para _"metadatos"_ que tienen un pequeño conjunto de términos controlados. A diferencia de la _"taxonomía"_, los términos no se convierten en un enlace en la página del _"elemento"_ y no tienen su propia página;

​■**Ajustes adicionales**:

​Los términos se añaden en el campo _"Opciones"_. Para añadir más valores, basta con escribir el término y hacer clic en **“enter”**.

<iframe    width="560"    height="513"     src="https://www.youtube.com/embed/-UoNKi7KfBw" title="YouTube video player"    frameborder="0"    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"    allowfullscreen></iframe>

!>**Atención**: Para crear nuevos términos en la lista de selección, es necesario que el usuario tenga permiso para editar los “metadatos” en cuestión. Los “metadatos” de la lista de selección no permiten la creación de nuevos términos durante el llenado, estos términos necesitan ser configurados previamente.

### Taxonomías

“\*Metadados do tipo Taxonomia**\*”** usam uma _“taxonomia”_ criada previamente. Este tipo de _“metadado”_ é especialmente útil para informações estruturadas a partir de um _“vocabulário controlado”_, permitindo inclusive a hierarquização de termos. Abaixo, apresentamos os passos para configurar um metadado do tipo _“Taxonomia”_.

​■**Configurações adicionais:**

​Como informado acima, é necessário criar primeiro uma _“Taxonomia”_. Esta será usada durante o processo de criação de um _“Metadado de Taxonomia”_:

1.Crie uma _“taxonomia”_. Consulte[ ](https://tainacan.github.io/tainacan-wiki/#/es-mx/taxonomies?id=criar-taxonomias)[Criar Taxonomias](https://tainacan.github.io/tainacan-wiki/#/es-mx/taxonomies?id=criar-taxonomias) para conhecer mais;

2.Crie um _“metadado”_ do tipo _“Taxonomia”_. Consulte Criar Metadados para saber mais;

3.Na área de _“edição do metadado”_, selecione a _“taxonomia”_ desejada para o preenchimento dos valores no _“metadado”_;

<iframe    width="560"    height="513"     src="https://www.youtube.com/embed/bDy0FQFolAs" title="YouTube video player"    frameborder="0"    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"    allowfullscreen></iframe>

4.Escolha o tipo de entrada de informações durante o preenchimento dos valores no _“metadado”_;

![Acesse o painel de controle](_assets\images\077.png)

​■**Entrada do tipo** **“Tag input”**:

Neste tipo de entrada, é oferecido ao usuário somente uma caixa de busca. Os termos podem ser explorados por meio de digitação e busca;

<iframe    width="560"    height="513"     src="https://www.youtube.com/embed/RUaAFqM_XmE" title="YouTube video player"    frameborder="0"    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"    allowfullscreen></iframe>

■**Entrada do tipo** **"Checkbox”:**

Este tipo de entrada ajuda o usuário a saber quais são os termos disponíveis para escolha em uma determinada _“Taxonomia”_. Os termos podem ser explorados em ordem alfabética ou por meio de digitação e busca;

<iframe    width="560"    height="513"     src="https://www.youtube.com/embed/6-3nRtvMvXQ" title="YouTube video player"    frameborder="0"    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"    allowfullscreen></iframe>

5.Marque a opção _“Lista de opções sempre visível”_ se você está exibindo uma lista de caixa de seleção ou entrada de rádio e deseja que, durante o preenchimento, a lista de opções esteja sempre visível. Esta opção só está disponível para a entrada do tipo _“Checkbox”;_

![Acesse o painel de controle](_assets\images\080.png)

6.Se necessário, habilite _“Permitir termos novos”_ para autorizar que novos termos de _“Taxonomia”_ sejam criados durante o envio de _“itens”_.

![Acesse o painel de controle](_assets\images\081.png)

■**“Link filtrado para a coleção”**

Os termos de _“Taxonomia”_ se transformam em itens na página do _“Item”_. Isto dá ao usuário a possibilidade de visitar uma faceta ou recorte do acervo. Por exemplo: em uma ficha de uma moeda de ouro, ao clicar no link referente ao termo _"ouro"_ o visitante terá acesso a todos os _“itens”_ que foram classificados com o mesmo material. Como uma _“Taxonomia”_ pode ser compartilhada entre diferentes _“coleções”_ no Tainacan, você pode configurar se o link do _“item”_ vai dar acesso a itens de outras coleções ou somente da coleção em que o item está inserido.

![Acesse o painel de controle](_assets\images\082.png)

### Relacionamento

_“Metadados de Relacionamento”_ permitem fazer a conexão entre itens de uma mesma coleção ou entre itens de coleções distintas, ou seja, atribuem um item de uma coleção como valor para seu preenchimento;

​■**“Configurações adicionais”**

1.Selecione a _“coleção relacionada”_ para apontar a origem da lista de _“itens”_ no preenchimento do _“metadado”_;

2.Quando uma _“coleção”_ é selecionada, a seção _“Metadados para busca”_ permite escolher os metadados desta _“coleção”_ que irão auxiliar na localização de _“itens”_ durante o preenchimento deste _“metadado”_;

3.Habilite _“permitir itens repetidos”_ para que um mesmo _“item”_ da _“coleção relacionada”_ seja atribuído como valor do _“metadado”_ em diferentes _“itens”_.

<iframe
      width="560"
      height="513" 
      src="https://www.youtube.com/embed/z1lc9X9GMTE" title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen>
</iframe>

### Composto

_“Metadados Compostos”_ são aqueles cujo valor não pode ser representado de maneira isolada por um único campo. Por exemplo, um endereço residencial pode ser composto por campos de _“texto”_, _“número”_ e até _“listas de seleção”_. Estes campos ou _“metadados”_ internos ao composto são chamados _“Metadados Filhos”_.

É importante diferenciar este conceito de uma [_“Sessão de Metadados”_](/es-mx/metadata-sections.md), cujo propósito é apenas de organizar dados _“agrupados”_. **Para simples separação visual, não o use**. No caso do _“metadado composto”_, é possível ter multivalores compostos, ou seja, uma lista de valores constituídos por diferentes sub-valores que se relacionam.

Note que, ao usá-los:

● Não é possível ter uma “Taxonomia” como “Metadado filho”;

● Um “metadado composto” não pode ser marcado como “Obrigatório” ou “Valor Único”. Esse atributo será marcado nos filhos. Se o “metadado composto”, porém, está marcado como “Aceita múltiplos valores”, seus filhos não poderão ser marcados como “Obrigatório”;

● Os “metadados filhos” não podem ser marcados como “Multivalorados”, e não possuem opções de visualização (“Ver na lista”), estas configurações correspondem ao pai;

● “Metadados compostos” não estão disponíveis como opção para “Busca Avançada” ou “Edição em Massa”, apenas seus filhos.

​■**Configurações adicionais:**

1.Logo ao se criar um _“metadado composto”_, uma área de criação dos filhos é formada abaixo de seu formulário. Arraste os tipos de _“metadados”_ desejados para dentro desta área para criar filhos;

2.Note que a ordenação funciona internamente entre filhos, mas, uma vez criados, não é possível promover os _“metadados”_ para _“não filhos”_.

<iframe
      width="560"
      height="513" 
      src="https://www.youtube.com/embed/x-iUm3pbOmQ" title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen>
</iframe>

### Usuário

“_Metadados”_ do tipo _“Usuário”_ atribuem um usuário WordPress como valor para seu preenchimento. Com ele você pode vincular usuários à _“itens”_ e definir um significado para tal vínculo, em geral desejado para fins de gestão.

§ Caso deseje que o campo seja de início preenchido com o valor do atual “Autor do item” (o usuário que o criou), marque a opção “Por padrão é o autor do item”.

> **Nota:** Marcar a opção acima não faz com que itens _“já existentes”_ tenham seus valores deste _“metadado”_ automaticamente preenchidos. Para isso, é possível usar o método _“Copiar”_ da edição em massa, passando dados para o _“metadado tipo usuário”_, vindos do atributo _“Criado por”_, que equivale ao _“autor do item”_.

Atualmente o Tainacan tem nove tipos de _“metadados por padrão”_, mas novos conjuntos[ ](https://tainacan.github.io/tainacan-wiki/#/dev/creating-metadata-type)[podem ser desenvolvidos](https://tainacan.github.io/tainacan-wiki/#/dev/creating-metadata-type) de acordo com a necessidade individual de cada instalação e/ou adicionados ao core do Tainacan. Consulte o artigo sobre o[ ](https://tainacan.github.io/tainacan-wiki/#/dev/)[Desenvolvimento do Plugin](https://tainacan.github.io/tainacan-wiki/#/dev/) para saber mais.

## Editar Metadados

Como detalhado na seção de criação de metadados, os _“metadados”_ podem ser criados tanto no _“nível de repositório”_ (serão herdados por todas as coleções), quanto no nível de uma determinada _“coleção”_. Por isso, os _“metadados”_ podem ser editados nestes dois níveis.

### Edição no Nível do repositório

1. Acesse o _“painel de controle”_ do WordPress;

   ![Acesse o painel de controle](_assets\images\050.png)

2. Na barra lateral esquerda, clique em _“Tainacan”_;

   ![Acesse o painel de controle](_assets\images\051.png)

3. Clique em _"Metadados de Repositório"_ (metadados que são herdados por todas as coleções);

   ![Acesse o painel de controle](_assets\images\085.png)

   !>**Atenção**: As modificações em configurações de _“metadados a nível de repositório”_ podem afetar dados já preenchidos e informações em itens que serão ou já foram criados em todo o repositório.

4. Clique no _“ícone de lápis”_ à direita do _“metadado”_ que deseja editar;

   ![Acesse o painel de controle](_assets\images\086.png)

5. Ao concluir as alterações, clique em _“Salvar”_ ou clique em _“Cancelar”_ para abortar a missão;

   !>**Atenção**: Não é possível alterar o _“Tipo de Metadado”._ Por exemplo, alterar um _“metadado”_ do tipo _“Texto”_ para _“Texto Longo”_, ou _“Numérico”_ para _“Data”_.

### Edição no nível da coleção

1. Acesse o _“painel de controle”_ do WordPress;

   ![Acesse o painel de controle](_assets\images\050.png)

2. Na barra lateral esquerda, clique em _“Tainacan”_;

   ![Acesse o painel de controle](_assets\images\051.png)

3. Clique na _“coleção”_ que você deseja editar;

   ![Acesse o painel de controle](_assets\images\087.png)

4. Clique em _“metadados”_;

![Acesse o painel de controle](_assets\images\088.png)

5. Clique no _“ícone lápis”_ para editar o _“metadado”;_

   ![Acesse o painel de controle](_assets\images\089.png)

!>**Atenção**: Não é possível alterar o _“Tipo de Metadado”_. Por exemplo, alterar um _“metadado”_ do tipo “_Texto”_ para “_Texto Longo”_, ou “_Numérico”_ para _“Data”_.

## Excluir Metadados

Excluir _“Metadados a nível de Repositório”_:

1. Acesse o _“painel de controle”_ do WordPress;

   ![Acesse o painel de controle](_assets\images\050.png)

2. Na barra lateral esquerda, clique em _“Tainacan”_;

   ![Acesse o painel de controle](_assets\images\051.png)

3. Clique em _"Metadados de Repositório"_ (metadados que são herdados por todas as coleções);

   ![Acesse o painel de controle](_assets\images\085.png)

4. Clique no “_ícone de lixeira”_ à direita do _“metadado”_ que deseja excluir;

   ![Acesse o painel de controle](_assets\images\090.png)

!>**Atenção**: Ao clicar no _“ícone de lixeira”_, o metadado é excluído imediatamente. Esta operação não poderá ser desfeita. A exclusão de _“metadados a nível de repositório”_ afetam **todos** os dados já preenchidos e informações em _“itens”_ que já foram criados em todo o repositório. Antes da exclusão do _“metadado”_, recomenda-se que este seja somente desabilitado (até que haja certeza de que a exclusão não implicará na perda de informações). Exclua o _“metadado”_ somente se tiver certeza de que não haverá perdas graves de informação. Consulte [Registro de atividades](/es-mx/activities) para saber mais.

### Excluir Metadados a nível de _“Coleções”_

1. Acesse o _“painel de controle”_ do WordPress;

   ![Acesse o painel de controle](_assets\images\050.png)

2. Na barra lateral esquerda, clique em _“Tainacan”_;

   ![Acesse o painel de controle](_assets\images\051.png)

3. Clique na _“coleção”_ que você deseja editar;

   ![Acesse o painel de controle](_assets\images\087.png)

4. Clique em _“metadados”;_

   ![Acesse o painel de controle](_assets\images\088.png)

5. Clique no _“ícone lixeira”_ para excluir o _“metadado”_;

   ![Acesse o painel de controle](_assets\images\091.png)

!>**Atenção:** Excluir _“Metadados a nível de coleção”_ afeta as informações de todos os _“itens”_ criados nesta _“coleção”_; Na tela de edição de _“Metadados”_ (a nível de repositório ou a nível de coleção), é possível visualizar os _“metadados já criados”_ (ou herdados) na coluna à esquerda; A exclusão do _“metadado”_ implica, também, na exclusão de seus valores em todos os _“itens”_ aos quais se aplica. Antes da exclusão do _“metadado”_, recomenda-se que este seja somente desabilitado (até que haja certeza de que a exclusão não implicará na perda de informações). Para _“desabilitar um metadado”_, basta clicar no botão ao lado da _“caneta de edição”_.

![Acesse o painel de controle](_assets\images\092.png)
