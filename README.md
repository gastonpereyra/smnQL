# SMN-QL

Proyecto para crear una app que informe el estado actual del clima y el pronostico para los proximos dias.
[EN DESARROLLO]

# API del SMN

* Dirección base: ` https://ws.smn.gob.ar/`
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

* ID de la substacion segun lat y long: `https://www.smn.gob.ar/smn/app/location/geo/:lat,:lon`


## /map_items/weather

* array: `[items]`
* length: 217 ?

## Items

* `_id : String` (Serialieze ID ?)
* `dist : Float`  (distancia ? a que ?)
* `lid : Int` (Localition ID) <- ID de la estacion
* `fid : Int` (Forecast ID)
* `int_number : Int` (?)
* `name : string` (nombre del lugar)
* `province: String` (provincia)
* `lat: Float` (latitud)
* `lon: Float` (longitud)
* `zoom: Int` (?)
* `updated: Int` UNIX (miliseconds desde 1970)
* `weather: Weather`
* `forecast: Forecast`

## Weather

* `humidity: Int` (Humedad, %)
* `pressure: Float` (Presion, hPa)
* `st : Float` (sensacion termica, °C)
* `temp : Float` (temperatura, °C)
* `tempDesc: String` (temperatura modo texto)
* `visibility: Int` (visibilidad, km)
* `wind_speed: Int` (Vel de Vient, km/h)
* `wind_deg: String` (direccion del viento, ["Este","Oeste","Sur","Norte", etc..]
* `id: Int` (ID del icono del clima)
* `description: String` (descripcion)

## Forecast
* `_id: ID`
* `timestamp: String`
* `date_time: String` (YYYY-mm-DD HH:MM)
* `location_id: Int`
* `forecast: [Forecasts]`

## Forecasts

* `date: String` (YYYY-mm-DD)
* `temp_min: Float` (Temperatura Minima °C) <- Manaña?
* `temp_max: Float` (Tempertura Maxima °C) <- Tarde ?
* `temp_min_sub: Float`  <- ?
* `temp_noc: Float` <- Noche? 
* `radiation: (?)` (Radiacion solar) <- Unidad: UV ?
* `morning: Morning`
* `afternoon: Afternoon`

## Morning
* `weather_id: Int`
* `description`

## Afternon
* `weather_id: Int`
* `description`

## Weather ID

* 1 - Sol-1 Nube | Algo Nublado
* 2 - Sol-2 Nubes | Algo Nublado a Parcialmente
* 10 - Nubes | Cubierto
