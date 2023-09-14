# Registro de componentes Vue personalizados

Cuando crees plugins para extender las funcionalidades de Tainacan, puede que tengas que enfrentarte a código Vue.js, que es el framework JS adoptado por nuestra comunidad para implementar el Panel de Administración de Tainacan. La mayoría de las veces, dispondrás de las herramientas necesarias para realizar el trabajo utilizando las librerías que ya incluye nuestro plugin. Pero en las situaciones en las que eso no es suficiente, surge la necesidad de registrar **componentes VueJS adicionales**. Aquí algunos ejemplos:

* Puede que necesites un [componente Map](https://github.com/vue-leaflet/Vue2Leaflet ':ignore') para crear un [nuevo tipo de metadatos](/es-mx/dev/creating-metadata-type.md) de geolocalización;
* Es posible que desee utilizar un [componente de selector de color](https://github.com/xiaokaike/vue-color ':ignore') para registrar un [nuevo tipo de filtro](/es-mx/dev/creating-filters-type.md) basado en colores, o incluso añadir un hook de formulario adicional para incrementar la configuración de su colección;
* Puede que quieras algún [componente de galería extravagante](https://github.com/KitchenStories/vue-gallery-slideshow ':ignore') para crear un nuevo [modo de vista extra a pantalla completa](/es-mx/dev/extra-view-modes);

Aquí echamos un vistazo a los detalles de:

* Cómo funciona el [registro de componentes globales](#registro-de-componentes-globales) en la instancia Vue de Tainacan.
* Cómo [registrar tu componente personalizado](#registrar-tu-componente-personalizado).
* Cómo [registrar componentes de terceros](#registrar-componentes-de-terceros).

## Registro de componentes globales

Cada componente global en nuestro código Vue.JS está registrado en el archivo `/src/views/admin/js/main.js` (para el panel Administrativo) o dentro del `/src/views/theme-search/theme-main.js` (para el bundle que renderiza la [Lista de Items](/es-mx/dev/the-vue-items-list-component.md)). Estos archivos suelen tener tres secciones:

1. Las importaciones, que cargan librerías del paquete de plugins, como `import VueMasonry from 'vue-masonry-css';` e `import FilterNumeric from '../../admin/components/filter-types/numeric/Numeric.vue';`;
2. Los registros de componentes y plugins en la instancia global de Vue, como `Vue.use(VueMasonry);` y `Vue.component('tainacan-filter-numeric', FilterNumeric);`;
3. La instanciación `new Vue(...)`, pasando todas las configuraciones necesarias.

Debido a este proceso, etiquetas como `<masonry>` o `<component is="tainacan-filter-numeric">` son entendidas por los componentes Vue a través del código fuente y los componentes registrados son renderizados. Para registrar nuestros propios componentes, necesitamos *engancharnos* a los pasos 1 y 2 descritos anteriormente. Ahí es donde la siguiente rutina (presente en las líneas 73-78 del código `/src/views/admin/js/main.js` y en las líneas 46-51 de `/src/views/theme-search/theme-main.js`) resulta útil:

```javascript
/* Registra los componentes extra de Vue pasados a la ventana.tainacan_extra_components  */
if (typeof window.tainacan_extra_components != "undefined") {
    for (let [extraVueComponentName, extraVueComponentObject] of Object.entries(window.tainacan_extra_components))
        Vue.component(extraVueComponentName, extraVueComponentObject);
}
```

You see, Vue Components can be exported as mere JS objects, containing their configuration. So here we're registering any components that are passed to this global array *window.tainacan_extra_components*. For adding any component to this array, we have a special Helper method, available for plugin developers: the `tainacan-register-vuejs-component()`. Let's see how to use it.

## Registering your our Custom Component

Consider the following PHP file, that shall be the main file of your plugin:

```php
<?php
/*
Plugin Name: Some Tainacan Plugin
Plugin URI: https://tainacan.org/new
Description: "Some Tainacan Plugin that registers a third party VueJS component."
Author: "Your Name Here"
Version: 0.1
Text Domain: some-tainacan-plugin
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-3.0.html
*/
add_action("tainacan-register-vuejs-component", "register_vuejs_component");

function register_vuejs_component($helper) {
	$handle = 'some-tainacan-plugin-component';
	$component_script_url = plugin_dir_url(__FILE__) . '/some-tainacan-plugin-component.js';

	$helper->register_vuejs_component($handle, $component_script_url);
}
?>
```

Simple as it looks, this plugin tells Tainacan where is the JS plugin code that should be load before the plugin `main.js` or `theme-main.js` scripts. Here is the content for `some-tainacan-plugin-component.js`:

```javascript
// Getting existing or creating the window.tainacan_extra_components object
var window.tainacan_extra_components = typeof window.tainacan_extra_components != "undefined" ? window.tainacan_extra_components : {};

// Creating your own VueJS component and passing it
const SomeTainacanPluginComponent = {
	name: "SomeTainacanPluginComponent",
	data: {
        // ...
    },
    methods: {
        // ...
    },
	template: `
     <!-- Here goes the template, including any components that we desire -->
	`
}
window.tainacan_extra_components["some-tainacan-plugin-component"] = SomeTainacanPluginComponent;
```

Thanks to the routine seen before the `<some-tainacan-plugin-component>` component shall be available. 

!> Warning: You MUST keep the `window.tainacan_extra_components` name, as it is the one used by the plugin to load custom components, and be careful to don't override it completely. Other plugins might have registered their components there too!

The good news is that, as the component is registered in the same *Vue Instance* of all the Tainacan bundle, any other globally registered plugin or component will be available. That means that, inside your *SomeTainacanPluginComponent* you have access to all of [Buefy](https://buefy.org/ ':ignore') components, to plugins such as [VTooltip](https://akryum.github.io/v-tooltip/#/ ':ignore'), [VueMasonry](https://github.com/paulcollett/vue-masonry-css ':ignore') and [VueDraggable](https://github.com/SortableJS/Vue.Draggable ':ignore'). You can even use some of our utility plugins made for Tainacan, such as the [UserPrefsPlugin](https://github.com/tainacan/tainacan/blob/develop/src/views/admin/js/utilities.js#L126 ':ignore'), which exposes methos for getting and setting user preferences ]]][UserCapabilitiesPlugin](https://github.com/tainacan/tainacan/blob/develop/src/views/admin/js/utilities.js#L346 ':ignore'), which helps us check user capabilities.

## Registering Third Party Components

That seems good, but what if you want some third party components? The process gets a bit more complicated depending on how the plugin is available. If you can't load its content from a CDN to just `require()` it in your JS, you will need some extra work to pass it to the global array. Ideally, it would be like this:

```javascript
// Getting existing or creating the window.tainacan_extra_components object
var window.tainacan_extra_components = window.tainacan_extra_components ? window.tainacan_extra_components : {};

// Importing and Passing a Third Party Component ...
import SomeThirdPartyComponent from 'some-third-party-component';
window.tainacan_extra_components["some-third-party-component"] = SomeThirdPartyComponent;
```

But the '*some-third-party-component*' should be available before, probably thanks to a `npm install some-third-party-component`. This requires our project to have a Bundler and Package Management files. While this can be done with many different libraries, we'll use NPM as *package manager* and Webpack as *bundler*. Your project should have a **package.json** file or you can create one by calling `npm init .`. Now open it and set up some basic dependencies:

```json
{
  "name": "third-party-component",
  "version": "1.0.0",
  "description": "",
  "scripts": {
    "build": "npx webpack some-plugin-component.js" // You can decide the build strategy that you prefer here
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "some-third-party-component": "^0.1.0" // Any third party vue component that you wish
  },
  "devDependencies": {
	"@babel/core": "^7.8.4",
    "babel-loader": "^8.0.6",
    "webpack": "^4.41.6",
    "webpack-cli": "^3.3.11",
    "vue-loader": "^15.9.0",
    "vue-template-compiler": "^2.6.11",
    "webpack-dev-server": "^3.10.3"
  }
}
```

You can either run `npm install` to download the specified dependencies to the recently created `node_modules` folder or manually install one by one of these dependencies (passing `--save-dev` for the devDependencies). Notice that in our example we already installed the desired `some-third-party-component`, which should be de vue component of your preference.

Now, to be able to bundle the JS when running `npx webpack some-plugin-component.js` via `npm run build` we need to configure Webpack. That is usually done in a `webpack.config.js` file:

```js
let path = require('path');
let webpack = require('webpack');
const VueLoaderPlugin = require('vue-loader/lib/plugin');

module.exports = {
    entry: './some-plugin-component.js',
	output: {
		path: path.resolve(__dirname, 'dist'),
		filename: 'some-plugin-component.bundle.js'
	}
	module:{
		rules: [
            {
                test: /\.vue$/,
                loader: 'vue-loader'
            },
            {
                test: /\.js$/,
                loader: 'babel-loader',
            }
		]
	},
	plugins: [
		new VueLoaderPlugin()
	]
}
```

The packages and loaders listed here are completely dependent on the component that you are trying to build. Some components may require, for example, some SASS or LESS loader.

Finally, after executing `npm run build` a `/dist/some-plugin-component.bundle.js` file will be created. It is this file that you now must reference as the `$component_script_url` on the `$helper->register_vuejs_component($handle, $component_script_url)` function.

## Wrapping up

To register Vue components to the same instance of Tainacan plugin, all you have to do is pass a Vue component object to the *window.tainacan_extra_components* global array. This can be referenced from a JS file set up in your plugin using the `tainacan-register-vuejs-component()` Helper method. For registering third party components, although, you need to handle how the import to your JS file will be bundled.

You can see more examples of using this strategy by checking the documentation of:

* How to create a [new Metadata Type](/dev/creating-metadata-type.md);
* How to create a [new Filter Type](/dev/creating-filters-type.md);
* How to create an [Extra View Mode](/dev/extra-view-modes);
