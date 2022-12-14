Download the template and upload into NiFi instance

### Configuring Processors

***GenerateFlowFile*** 

Configuring `GenerateFlowFile` processor is simple. Just copy below data to `Custom Text` property of GenerateFlowFile Processor

```json
{
  "id" : 6523,
  "ident" : "00A",
  "type" : "heliport",
  "name" : "Total Rf Heliport",
  "latitude_deg" : 40.07080078125,
  "longitude_deg" : -74.93360137939453,
  "elevation_ft" : 11,
  "continent" : "NA",
  "iso_country" : "US",
  "iso_region" : "Pennsylvania",
  "country_name" : "United States"
}
```

***EvaluateJSONPath***

| Name | Value |
| ---- | ----- |
| Destination | `flowfile-attribute` |

Dynamic Properties

| Name | Value |
| ---- | ----- |
| `country_name` | `$.country_name` |
| `id` | `$.id` |
| `ident` | `$.ident` |
| `iso_region` | `$.iso_region` |
| `name` | `$.name` |
| `type` | `$.type` |

***ReplaceText***

| Name | Value |
| ---- | ----- |
| Replacement Value | {<br>"id" : ${id},<br>"ident" : "${ident}",<br>"type" : "${type}",<br>"name" : "${name}",<br>"iso_region" : "${iso_region}",<br>"country_name" : "${country_name}"<br>} |
| Replacement Strategy | `Always Replace` |
| Evaluation Mode | `Entire text` |