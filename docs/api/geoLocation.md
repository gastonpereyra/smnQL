# Geolocalización

<img src="http://cdn.onlinewebfonts.com/svg/img_466912.png" width="200">

## Endpoint

Dirección base: `https://www.smn.gob.ar/smn/app/location/geo/:lat,:lon`

* `lat`: Latitud
* `lon`: Longitud

## Devuelve

En el Body -> .text() -> Texto plano, con un ID.

## Aclaración

El ID que devuelve no siempre coincide con uno existente, es posible que en ciertas zonas como Capital Federal genere ID incorrectos.
Por esta razón es mejor buscar metodos alternativos.
