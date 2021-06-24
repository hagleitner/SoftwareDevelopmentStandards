global
## Organizations
/standard/v1/organizations/{id}/

## Customers
/standard/v1/customers/{id}/



## Devices

? only active devices?

* /standard/v1/devices/{id}
  * Accesses a specific device, permissions will be checked

* /standard/v1/devices:
  * with device filter(s) in request body, global scope

* /standard/v1/customers/{id}/devices
  * with deviceFilter(s) request body

* /standard/v1/organizations/{id}/devices
  * with deviceFilter(s) request body

### Dto
* DeviceId
* DeviceTypeId
* Compound members
* Device type name
* Devide type alias
* Serial number
* Mac
* Installation date
* Customer number
* Mount Point information
* Location information

## Standard API Session parameters
* Timezone
* Language
* Culture

