# Cómo crear un Expositor

Los Expositores son clases que implementan un nuevo expositor que puede ser utilizado por Tainacan para exponer el contenido de un repositorio a través de una API.

Para crear un nuevo exposer básicamente tienes que crear una clase Exposer y registrarla.

## Creación de una clase expositora

Crear una clase que extienda `\Tainacan\Exposers\Exposer`.

```php 
<?php 

class MyExposer extends \Tainacan\Exposers\Exposer {
	
}

```

En esta clase tendrás que configurar algunos atributos y métodos:

### Atributos

#### Babosa

**String $slug**

Una versión URL amigable del nombre del expositor, que se utilizará como parámetro en la solicitud de API informando de que desea obtener los datos utilizando este expositor.

```php 
<?php 

class MyExposer extends \Tainacan\Exposers\Exposer {
	
	public $slug = 'my-exposer';
	
}

```

#### Estándar de mapeo soportado

**Array o verdadero $mappers**

Una lista de estándares de mapeo que soporta este expositor. Esto significa que cuando alguien solicite recibir datos a través de este expositor, también podrá elegir qué estándar de mapeo quiere que se sirva el contenido. Si se establece en `true` el expositor aceptará todos los estándares de mapeo.

```php 
<?php 

class MyExposer extends \Tainacan\Exposers\Exposer {
	
	public $slug = 'my-exposer';
	public $mappers = true;
	
}

```

o 

```php 
<?php 

class MyExposer extends \Tainacan\Exposers\Exposer {
	
	public $slug = 'my-exposer';
	public $mappers = ['dublin-core']; // indica que este expositor sólo servirá datos mapeados con dublin core mapper
	
}
```

#### No aceptar normas cartográficas 

**Booleano $accept_no_mapper**

Indica si este expositor acepta servir datos en su forma nativa, sin ningún estándar de mapeo.

```php 
<?php 

class MyExposer extends \Tainacan\Exposers\Exposer {
	
	public $slug = 'my-exposer';
	public $mappers = ['dublin-core']; // indica que este expositor sólo servirá datos mapeados con dublin core mapper
	public $accept_no_mapper = true; 
}
```

### Métodos

Ahora que has declarado los atributos básicos de tu Expositor, hay dos métodos que debes implementar.


#### __construct()

En este método debe llamar a `set_name()` y `set_description()` para identificar su expositor.

```php 
<?php 

class MyExposer extends \Tainacan\Exposers\Exposer {
	
	public $slug = 'my-exposer';
	public $mappers = ['dublin-core']; // indica que este expositor sólo servirá datos mapeados con dublin core mapper
	public $accept_no_mapper = true; 
	
	public function __construct() {
		$this->set_name( __('My Exposer', 'my-test-plugin-namespace') );
		$this->set_description( __('This exposer server the data in a very different way', 'my-test-plugin-namespace') );
	}
	
}
```

**Nota**: La razón por la que Nombre y la Descripción se declaran de esta manera, y no como atributos, es para permitirle localizar sus cadenas a diferentes idiomas. Por favor, consulte la documentación de WordPress para aprender a internacionalizar su plugin.


#### rest_request_after_callbacks()

Aquí es donde ocurre toda la magia.

Este método será llamado justo antes de que la API devuelva los datos al cliente.

Te dará todos los elementos que recibió, en la forma en que estaban a punto de ser servido en el formato JSON por defecto, y le permiten transformarlo.

Recibe 3 parámetros:

* $response: una instancia de `\WP_REST_Response` object 
* $handler: una instancia de `\WP_REST_Server` object 
* $request: una instancia de `\WP_REST_Request` object 

Este método debe devolver la versión modificada del objeto `\WP_REST_Response`.

```php 
<?php 

class MyExposer extends \Tainacan\Exposers\Exposer {
	
	public $slug = 'my-exposer';
	public $mappers = ['dublin-core']; // indica que este expositor sólo servirá datos mapeados con dublin core mapper
	public $accept_no_mapper = true; 
	
	public function __construct() {
		$this->set_name( __('My Exposer', 'my-test-plugin-namespace') );
		$this->set_description( __('This exposer server the data in a very different way', 'my-test-plugin-namespace') );
	}
	
	public function rest_request_after_callbacks( $response, $handler, $request ) {
		
		// Set the headers to another content type, if applicable
		$response->set_headers( ['Content-Type: text/plain; charset=' . get_option( 'blog_charset' )] );
		
		$items = $response->get_data();
		
		// Transform the items somehow ...
		// ...
		
		$response->set_data($items);
		
		return $response;
	}
	
}
```


### Registrar un nuevo expositor

Para registrar un nuevo expositor, la acción necesita ser añadida al hook `tainacan-register-exposers`, como:
```php 
<?php
	function registerMyExposer($exposers) {
		$exposers->register_exposer('MyExposer');
	}
	add_action('tainacan-register-exposers', 'registerMyExposer');
```

### Ejemplo completo

Este es un ejemplo completo de un plugin que implementa un simple expositor de texto

```php 
<?php
/*
Plugin Name: Tainacan TXT Exposer
Description: This is a sample exposer class
*/

function myNewExposer($exposers) {
	
	class TxtExposer extends \Tainacan\Exposers\Exposer {
		
		public $slug = 'txt'; // escriba slug para url segura
		public $name = 'TXT';
		protected $mappers = true;
		public $accept_no_mapper = true;
		
		private $identation = '';
		
		function __construct() {
			$this->set_name( 'TXT' );
			$this->set_description( __('A simple TXT table', 'my-test-plugin-namespace') );
		}
		
		/**
		* 
		* {@inheritDoc}
		* @see \Tainacan\Exposers\Types\Type::rest_request_after_callbacks()
		*/
		public function rest_request_after_callbacks( $response, $handler, $request ) {
			$response->set_headers( ['Content-Type: text/plain; charset=' . get_option( 'blog_charset' )] );
			
			$txt = $this->array_to_txt($response->get_data(), false);
			
			$response->set_data($txt);
			return $response;
		}
		
		/**
		* Convert Array to Txt
		* @param array $data
		* @param string $txt
		* @return string
		*/
		protected function array_to_txt( $data, $addlevel = true ) {
			
			$return = '';
			
			if ($addlevel) {
				$this->identation .= '    ';
			}
			
			foreach( $data as $key => $value ) {
				
				
				$return .= $this->identation . $key . ': ';
				if (is_array($value)) {
					$return .= "\n" . $this->array_to_txt($value);
				} else {
					$return .= $value . "\n";
				}
				
			}
			
			if ($addlevel) {
				$this->identation = substr($this->identation, 0,  strlen($this->identation) - 4  );
			}
			
			return $return;
		}
	}
	
	$exposers->register_exposer('TxtExposer');
}
add_action('tainacan-register-exposers', 'myNewExposer');

```
