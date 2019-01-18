## Clima

## Endpoint

`/map_items/weather`

## Devuelve

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
