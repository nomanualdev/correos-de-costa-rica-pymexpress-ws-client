# correos-de-costa-rica-pymexpress-ws-client

PHP WS Client Based on Mojito Shipping

Clase de conexión para el nuevo Web Service de Correos de Costa Rica (Pymexpress). Requiere de datos de conexión, si usted no cuenta con estos datos puede solicitarlos al correo jmora {arroba} correos.go.cr


**Inicializar**
```
$pymexpress = new Pymexpress\Pymexpress_WSC( $username, $password, $user_id, $service_id, $client_code, $environment );
```



**Asignar Proxy [ Opcional ]**
```
$pymexpress->set_proxy( array(
	'hostname' => 'My Host',
	'username' => 'My Username',
	'password' => 'My Password',
	'port'     => 'My Host port',
));
```



**Obtener número de guía**
```
$guia = $pymexpress->generar_guia();
```



**Obtener provicias**
```
$provincias = $pymexpress->get_provincias();
```



**Obtener cantones de una provincia**
- 1 = San José
```
$cantones = $pymexpress->get_cantones( '1' );
```



**Obtener distritos de un cantón**
- 1 = San José
- 01 = San José
```
$distritos = $pymexpress->get_distritos( '1', '01' );
```



**Obtener distritos de un cantón**
- 1 = San José
- 01 = San José
- 01 = Carmen
```
$barrios = $pymexpress->get_barrios( '1', '01', '01' );
```



**Obtener código postal**
- 1 = San José
- 01 = San José
- 01 = Carmen
```
$codigo_postal = $pymexpress->get_codigo_postal( '1', '01', '01' );
```



**Obtener tarifa**
- Envío desde San José, Carmen a San José, Carmen 1 kg de peso
```
$tarifa = $pymexpress->get_tarifa( '1', '01', '1', '01', '1000' );
```
