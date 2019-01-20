# Pronostico

<img src="http://cdn.onlinewebfonts.com/svg/img_561464.png" width="200">

Solo pronosticos, todos, a 1 y hasta 4 dias

## Endpoints

* Pronosticos : `forecast`
* a 1 dia: `map_items/forecast/1`
* a 2 dia: `map_items/forecast/2`
* a 3 dia: `map_items/forecast/3`
* a 4 dia: `map_items/forecast/4`

## Devuelve

* `_id: ID`
* `timestamp: String`
* `date_time: String` # (YYYY-mm-DD HH:MM)
* `location_id: Int`
* `forecast: [Forecasts]` # NO ES UN ARRAY, es un Objeto

### Forecasts

Posición "0", pronostico del dia vigente, a partir del "1" los proximos dias.

* `date: String` # (YYYY-mm-DD)
* `temp_min: Float` # (Temperatura Minima °C) <- Manaña?
* `temp_max: Float` (Tempertura Maxima °C) <- Tarde ?
* `temp_min_sub: Float` #  <- ?
* `temp_noc: Float` # <- Noche? 
* `radiation: (?)` # (Radiacion solar) <- Unidad: UV ?
* `morning: Morning`
* `afternoon: Afternoon`

### Morning

* `weather_id: Int`
* `description`

### Afternon

* `weather_id: Int`
* `description`
