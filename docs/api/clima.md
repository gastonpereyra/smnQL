## Clima

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/Weather-sun-thorm-shower.svg/1024px-Weather-sun-thorm-shower.svg.png" width="200">

## Endpoint

`/map_items/weather`

## Devuelve

* array: `[items]`
* length: 217 ?

## Items

* `_id : String` # (Serialieze ID ?)
* `dist : Float` # (distancia a la estación)
* `lid : Int` # (Localition ID) <- ID de la estacion
* `fid : Int` # (Forecast ID)
* `int_number : Int` # (?)
* `name : string` # (nombre del lugar, localidad)
* `province: String` # (provincia)
* `lat: Float` # (latitud)
* `lon: Float` # (longitud)
* `zoom: Int` # (?)
* `updated: Int` # UNIX (miliseconds desde 1970)
* `weather: Weather` # Condición climaticas Actuales
* `forecast: Forecast` # Pronostico

## Weather

* `humidity: Int` # (Humedad, %) 
* `pressure: Float` # (Presion, hPa)
* `st : Float` # (sensacion termica, °C)
* `temp : Float` # (temperatura, °C)
* `tempDesc: String` # (temperatura modo texto)
* `visibility: Int` # (visibilidad, km)
* `wind_speed: Int` # (Vel de Vient, km/h)
* `wind_deg: String` # (direccion del viento, ["Este","Oeste","Sur","Norte", etc..]
* `id: Int` # ([weather_Id](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/clima_id.md) - tipo de clima)
* `description: String` # (descripcion - Leyenda)

## Forecast
* `_id: ID` # ?
* `timestamp: String` # (fecha de emisión ?)
* `date_time: String` # (YYYY-mm-DD HH:MM)
* `location_id: Int` # (id de la estación - lid / fid)
* `forecast: [Forecasts]` # ( **ATENCION**, no es un ARRAY es un Objecto con numeros como keys, es mejor transformarlo a ARRAY)

## Forecasts

Viene en "0" el pronostico del dia vigente, y a partir de "1" los proximos dias.

* `date: String` # (YYYY-mm-DD)
* `temp_min: Float` # (Temperatura Minima °C) <- Manaña?
* `temp_max: Float` # (Tempertura Maxima °C) <- Tarde ?
* `temp_min_sub: Float` # <- ?
* `temp_noc: Float` <- Noche ? 
* `radiation: (?)` # (Radiacion solar) <- Unidad: UV ?
* `morning: Morning`
* `afternoon: Afternoon`

### Morning

* `weather_id: Int` # ([weather_id](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/clima_id.md) )
* `description`

### Afternon
* `weather_id: Int` # ([weather_id](https://github.com/gastonpereyra/smnQL/blob/master/docs/api/clima_id.md) )
* `description`
