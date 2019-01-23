# API GraphQL

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/17/GraphQL_Logo.svg/2000px-GraphQL_Logo.svg.png" width="200">

Esta API la construí yo usando GrahpQL, obviamente, **Node** y alojada en **Glitch** para usarla. 

No pretende perseguir fines comerciales, ni de lucro, solo a manera de aprendizaje, como ejemplo de "Wrapping REST API".

### En Desarrollo

## Dirección Base

`https://climaql-server.glitch.me/graphql`

## Query

* `getWeahterById(id!): WeatherReport` / Dado un ID de una subestación, devuelve los datos de la misma y del clima del lugar
* `getWeahterByCoords(lat!,lon!): WeatherReport` / Dado unas Coordenadas devuelve los datos de la misma y del clima del lugar dela Subestación mas cercana
* `getWeathers: [WeatherReport]` / Devuelve un objecto con los datos de la substación y los datos del clima del lugar, todos los disponibles
* `getForecasts: [Forecast]` / Devuelve todos los pronosticos disponibles de todas las subestaciones
* `getForecast(id!): Forecast` Dado un ID de una subestación, devuelve los pronosticos disponibles

## Mutations

No posee

## Schemas

### WeatherReport

SubEstación Regional Clima Actual.

* `_id : ID` # id del reporte cambia en cada informe
* `dist : Float`
* `lid : Int` # ID de la Estación
* `fid : Int` # ID de la Estación
* `int_number : Int`
* `name : String` # Nombre del Lugar
* `province: String` # Provincia
* `lat: Float`
* `lon: Float`
* `zoom: Int`
* `updated: Int` # UNIX
* `weather: Weather`
* `forecast: Forecast`

### Weather 

* `temp : Float` # Temperatura en °C   
* `tempDesc: String` # Temperatura en Texto
* `st : Float` # Sensación Térmica en °C
* `humidity: Int` # Humedad en %
* `pressure: Float` # Presión Atmosferica en hPa
* `visibility: Int` # Visibilidad en km
* `wind_speed: Int` # Velocidad del Viente en km/h
* `wind_deg: String` # Velocidad del Viente en km/h | ["Este","Oeste","Sur","Norte", etc..]
* `id: Int` # ID del icono del clima
* `description: String` #  Solo Español
* `forecast: Forecast` # Pronostico

### Forecast 

* `_id: ID`
* `timestamp: String`
* `date_time: String` # (YYYY-mm-DD HH:MM)
* `location_id: Int`
* `forecast: [Forecasts]`

### Forecasts 

* `date: String` # (YYYY-mm-DD)
* `temp_min: Float`
* `temp_max: Float`
* `temp_min_sub: Float`
* `temp_noc: Float` 
* `radiation: String `
* `morning: Morning`
* `afternoon: Afternoon`

### Morning 

* `weather_id: Int`
* `description: String`

### Afternoon 

* `weather_id: Int`
* `description: String`
