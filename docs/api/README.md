# API del SMN

Lista de endpoints de la API del Servicio Meteorologico Nacional Argentino.

* ID de la substacion segun lat y long: `https://www.smn.gob.ar/smn/app/location/geo/:lat,:lon`
* Dirección base: ` https://ws.smn.gob.ar/`

Endpoints conocidos:

* Lista de el estado del clima actual + pronostico ? : `map_items/weather` 
* Pronosticos : `forecast`
* Lista del pronostico para 1 dia: `map_items/forecast/1`
* Lista del pronostico para 1 dia: `map_items/forecast/2`
* Lista del pronostico para 1 dia: `map_items/forecast/3`
* Lista del pronostico para 1 dia: `map_items/forecast/4`
* Alertas: `alerts`
* Alertas Vigentes: `alerts/type/AL`
* Alertas corto plazo: `alerts/type/AC`
* Alertas informe especial: `alerts/type/IE`
* Nefoanálisis: `images`
