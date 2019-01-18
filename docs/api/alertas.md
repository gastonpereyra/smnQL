# Alerts

Alertas en general, Corto Plazo, Vigentes, Informes Especiales

## Endpoints

* Alertas: `alerts`
* Alertas Vigentes: `alerts/type/AL`
* Alertas corto plazo: `alerts/type/AC`
* Alertas informe especial: `alerts/type/IE`

## Devuelve

* `_id: ID`
* `idAlert: Int`
* `nReport: Int`
* `type: IE` [IE, AL, AC]
* `title: String`
* `status: String`
* `date: String` (YYYY-mm-DD)
* `hour: String` (HH-MM-SS)
* `description: String`
* `zones : {Zones}`
  * `:numero : String`
* `severity: String`
* `polygon: ?`
* `update: String` (HH-MM-SS)
