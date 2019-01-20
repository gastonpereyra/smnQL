# API del SMN

<img src="https://image.flaticon.com/icons/png/512/297/297396.png" width="200">

Lista de endpoints de la API del Servicio Meteorologico Nacional Argentino.

## Dirección Base

* Dirección base: ` https://ws.smn.gob.ar/`

## Endpoints conocidos:

* Lista de el estado del clima actual + pronostico ? : `map_items/weather` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/clima.md)
* Pronosticos : `forecast` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/pronostico.md)
* Lista del pronostico para 1 dia: `map_items/forecast/1` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/pronostico.md)
* Lista del pronostico para 2 dia: `map_items/forecast/2` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/pronostico.md)
* Lista del pronostico para 3 dia: `map_items/forecast/3` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/pronostico.md)
* Lista del pronostico para 4 dia: `map_items/forecast/4` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/pronostico.md)
* Alertas: `alerts` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/alertas.md)
* Alertas Vigentes: `alerts/type/AL` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/alertas.md)
* Alertas corto plazo: `alerts/type/AC` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/alertas.md)
* Alertas informe especial: `alerts/type/IE` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/alertas.md)
* Nefoanálisis: `images` - [+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/nefoanalisis.md)

## Geolocation

* ID de la substacion segun lat y long: `https://www.smn.gob.ar/smn/app/location/geo/:lat,:lon`
[+ Aqui](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/geoLocation.md)
