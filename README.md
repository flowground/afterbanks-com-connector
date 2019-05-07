# ![LOGO](logo.png) Afterbanks **flow**ground Connector

## Description

A generated **flow**ground connector for the Afterbanks API (version 3.0.0).

Generated from: https://api.apis.guru/v2/specs/afterbanks.com/3.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:34:49+03:00

## API Description

La estandarización de la conexión con cualquier banco en tiempo real.

## Authorization

This API does not require authorization.

## Actions

### Lista de bancos soportados

> Obten una lista completa de los bancos soportados, asi como los nombres de los campos necesarios para dibujar un formulario de login similar al oritinal del banco.

*Tags:* `forms`

#### Input Parameters
* `country_code` - _optional_ - Codigo del pais, formato ISO 3166-1 alpha-2 (https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). Por ejemplo ES para Espana. Si no se proporciona ningun codigo, se devolvera la lista completa.

### Informacion de uso de mi licencia

> Devuelve informacion sobre mi licencia y uso de llamadas

*Tags:* `User`

#### Input Parameters
* `servicekey` - _required_ - Licencia que identifica al cliente. Si no tienes una, puedes solicitarla en https://www.afterbanks.com

### Posicion global y movimientos hasta una fecha dada.

> Este endpoint devuelve el listado de productos y los movimientos para cada uno de los productos desde la fecha solicidata hasta el dia actual. Existe un sandbox donde probar llamadas: https://www.afterbanks.com/sandbox/

*Tags:* `serviceV3`

#### Input Parameters
* `servicekey` - _required_ - Licencia que identifica al cliente. Si no tienes una, puedes solicitarla en https://www.afterbanks.com
* `service` - _required_ - Identificador unico para cada banco. El listado de bancos soportados se obtiene de https://www.afterbanks.com/forms/
* `documentType` - _optional_ - Algunos bancos, en su formulario de login, solicitan el tipo de documento. En estos casos, se debera identificar un numero entero (de 0 a 4), que corresponde con su posicion en el formulario de login del banco.
* `user` - _required_ - Usuario
* `pass` - _required_ - Contrasena
* `pass2` - _optional_ - Algunos bancos utilizan una segunda contrasena.
* `products` - _optional_ - Nombres de productos bancarios (cuentas corrientes, tarjetas, etc), separados por coma. Cabe destacar que en la primera llamada a la API, aun no conocemos los nombres de los productos que el usuario tiene contratados, por lo que este parametro estara vacio.
* `startdate` - _required_ - Fecha desde la que queremos obtener los movimientos en formato dd-mm-aaaa. Obligatorio cuando el valor de "products" es distinto de GLOBAL.

## License

**flow**ground :- Telekom iPaaS / afterbanks-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
