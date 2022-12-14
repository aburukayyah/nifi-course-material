Download the template and upload into NiFi instance

### Configuring Processors

***GenerateFlowFile*** 

Configuring `GenerateFlowFile` processor is simple. Just copy below data to `Custom Text` property of GenerateFlowFile Processor

```json
[
  {
    "id": 6523,
    "ident": "00A",
    "type": "heliport",
    "name": "Total Rf Heliport",
    "latitude_deg": 40.07080078125,
    "longitude_deg": -74.93360137939453,
    "elevation_ft": 11,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-PA",
    "municipality": "Bensalem",
    "scheduled_service": "no",
    "gps_code": "00A",
    "iata_code": "",
    "local_code": "00A",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 323361,
    "ident": "00AA",
    "type": "small_airport",
    "name": "Aero B Ranch Airport",
    "latitude_deg": 38.704022,
    "longitude_deg": -101.473911,
    "elevation_ft": 3435,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-KS",
    "municipality": "Leoti",
    "scheduled_service": "no",
    "gps_code": "00AA",
    "iata_code": "",
    "local_code": "00AA",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6524,
    "ident": "00AK",
    "type": "small_airport",
    "name": "Lowell Field",
    "latitude_deg": 59.947733,
    "longitude_deg": -151.692524,
    "elevation_ft": 450,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-AK",
    "municipality": "Anchor Point",
    "scheduled_service": "no",
    "gps_code": "00AK",
    "iata_code": "",
    "local_code": "00AK",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6525,
    "ident": "00AL",
    "type": "small_airport",
    "name": "Epps Airpark",
    "latitude_deg": 34.86479949951172,
    "longitude_deg": -86.77030181884766,
    "elevation_ft": 820,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-AL",
    "municipality": "Harvest",
    "scheduled_service": "no",
    "gps_code": "00AL",
    "iata_code": "",
    "local_code": "00AL",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6526,
    "ident": "00AR",
    "type": "closed",
    "name": "Newport Hospital & Clinic Heliport",
    "latitude_deg": 35.6087,
    "longitude_deg": -91.254898,
    "elevation_ft": 237,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-AR",
    "municipality": "Newport",
    "scheduled_service": "no",
    "gps_code": "",
    "iata_code": "",
    "local_code": "",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": "00AR"
  },
  {
    "id": 322127,
    "ident": "00AS",
    "type": "small_airport",
    "name": "Fulton Airport",
    "latitude_deg": 34.9428028,
    "longitude_deg": -97.8180194,
    "elevation_ft": 1100,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-OK",
    "municipality": "Alex",
    "scheduled_service": "no",
    "gps_code": "00AS",
    "iata_code": "",
    "local_code": "00AS",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6527,
    "ident": "00AZ",
    "type": "small_airport",
    "name": "Cordes Airport",
    "latitude_deg": 34.305599212646484,
    "longitude_deg": -112.16500091552734,
    "elevation_ft": 3810,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-AZ",
    "municipality": "Cordes",
    "scheduled_service": "no",
    "gps_code": "00AZ",
    "iata_code": "",
    "local_code": "00AZ",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6528,
    "ident": "00CA",
    "type": "small_airport",
    "name": "Goldstone (GTS) Airport",
    "latitude_deg": 35.35474,
    "longitude_deg": -116.885329,
    "elevation_ft": 3038,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-CA",
    "municipality": "Barstow",
    "scheduled_service": "no",
    "gps_code": "00CA",
    "iata_code": "",
    "local_code": "00CA",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 324424,
    "ident": "00CL",
    "type": "small_airport",
    "name": "Williams Ag Airport",
    "latitude_deg": 39.427188,
    "longitude_deg": -121.763427,
    "elevation_ft": 87,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-CA",
    "municipality": "Biggs",
    "scheduled_service": "no",
    "gps_code": "00CL",
    "iata_code": "",
    "local_code": "00CL",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 322658,
    "ident": "00CN",
    "type": "heliport",
    "name": "Kitchen Creek Helibase Heliport",
    "latitude_deg": 32.7273736,
    "longitude_deg": -116.4597417,
    "elevation_ft": 3350,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-CA",
    "municipality": "Pine Valley",
    "scheduled_service": "no",
    "gps_code": "00CN",
    "iata_code": "",
    "local_code": "00CN",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6529,
    "ident": "00CO",
    "type": "closed",
    "name": "Cass Field",
    "latitude_deg": 40.622202,
    "longitude_deg": -104.344002,
    "elevation_ft": 4830,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-CO",
    "municipality": "Briggsdale",
    "scheduled_service": "no",
    "gps_code": "",
    "iata_code": "",
    "local_code": "",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": "00CO"
  },
  {
    "id": 6531,
    "ident": "00FA",
    "type": "small_airport",
    "name": "Grass Patch Airport",
    "latitude_deg": 28.64550018310547,
    "longitude_deg": -82.21900177001953,
    "elevation_ft": 53,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-FL",
    "municipality": "Bushnell",
    "scheduled_service": "no",
    "gps_code": "00FA",
    "iata_code": "",
    "local_code": "00FA",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6532,
    "ident": "00FD",
    "type": "heliport",
    "name": "Ringhaver Heliport",
    "latitude_deg": 28.846599578857422,
    "longitude_deg": -82.34539794921875,
    "elevation_ft": 25,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-FL",
    "municipality": "Riverview",
    "scheduled_service": "no",
    "gps_code": "00FD",
    "iata_code": "",
    "local_code": "00FD",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6533,
    "ident": "00FL",
    "type": "small_airport",
    "name": "River Oak Airport",
    "latitude_deg": 27.230899810791016,
    "longitude_deg": -80.96920013427734,
    "elevation_ft": 35,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-FL",
    "municipality": "Okeechobee",
    "scheduled_service": "no",
    "gps_code": "00FL",
    "iata_code": "",
    "local_code": "00FL",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6534,
    "ident": "00GA",
    "type": "small_airport",
    "name": "Lt World Airport",
    "latitude_deg": 33.76750183105469,
    "longitude_deg": -84.06829833984375,
    "elevation_ft": 700,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-GA",
    "municipality": "Lithonia",
    "scheduled_service": "no",
    "gps_code": "00GA",
    "iata_code": "",
    "local_code": "00GA",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6535,
    "ident": "00GE",
    "type": "heliport",
    "name": "Caffrey Heliport",
    "latitude_deg": 33.889245,
    "longitude_deg": -84.73793,
    "elevation_ft": 957,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-GA",
    "municipality": "Hiram",
    "scheduled_service": "no",
    "gps_code": "00GE",
    "iata_code": "",
    "local_code": "00GE",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6536,
    "ident": "00HI",
    "type": "heliport",
    "name": "Kaupulehu Heliport",
    "latitude_deg": 19.832715,
    "longitude_deg": -155.980233,
    "elevation_ft": 43,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-HI",
    "municipality": "Kailua-Kona",
    "scheduled_service": "no",
    "gps_code": "00HI",
    "iata_code": "",
    "local_code": "00HI",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6537,
    "ident": "00ID",
    "type": "small_airport",
    "name": "Delta Shores Airport",
    "latitude_deg": 48.145301818847656,
    "longitude_deg": -116.21399688720703,
    "elevation_ft": 2064,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-ID",
    "municipality": "Clark Fork",
    "scheduled_service": "no",
    "gps_code": "00ID",
    "iata_code": "",
    "local_code": "00ID",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 322581,
    "ident": "00IG",
    "type": "small_airport",
    "name": "Goltl Airport",
    "latitude_deg": 39.724028,
    "longitude_deg": -101.395994,
    "elevation_ft": 3359,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-KS",
    "municipality": "McDonald",
    "scheduled_service": "no",
    "gps_code": "00IG",
    "iata_code": "",
    "local_code": "00IG",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6538,
    "ident": "00II",
    "type": "closed",
    "name": "Bailey Generation Station Heliport",
    "latitude_deg": 41.644501,
    "longitude_deg": -87.122803,
    "elevation_ft": 600,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-IN",
    "municipality": "Chesterton",
    "scheduled_service": "no",
    "gps_code": "",
    "iata_code": "",
    "local_code": "",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": "00II"
  },
  {
    "id": 6539,
    "ident": "00IL",
    "type": "small_airport",
    "name": "Hammer Airport",
    "latitude_deg": 41.97840118408203,
    "longitude_deg": -89.5604019165039,
    "elevation_ft": 840,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-IL",
    "municipality": "Polo",
    "scheduled_service": "no",
    "gps_code": "00IL",
    "iata_code": "",
    "local_code": "00IL",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6540,
    "ident": "00IN",
    "type": "heliport",
    "name": "St Mary Medical Center Heliport",
    "latitude_deg": 41.51139831542969,
    "longitude_deg": -87.2605972290039,
    "elevation_ft": 634,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-IN",
    "municipality": "Hobart",
    "scheduled_service": "no",
    "gps_code": "00IN",
    "iata_code": "",
    "local_code": "00IN",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6541,
    "ident": "00IS",
    "type": "small_airport",
    "name": "Hayenga's Cant Find Farms Airport",
    "latitude_deg": 40.02560043334961,
    "longitude_deg": -89.1229019165039,
    "elevation_ft": 820,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-IL",
    "municipality": "Kings",
    "scheduled_service": "no",
    "gps_code": "00IS",
    "iata_code": "",
    "local_code": "00IS",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6542,
    "ident": "00KS",
    "type": "small_airport",
    "name": "Hayden Farm Airport",
    "latitude_deg": 38.72779846191406,
    "longitude_deg": -94.93049621582031,
    "elevation_ft": 1100,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-KS",
    "municipality": "Gardner",
    "scheduled_service": "no",
    "gps_code": "00KS",
    "iata_code": "",
    "local_code": "00KS",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6543,
    "ident": "00KY",
    "type": "small_airport",
    "name": "Robbins Roost Airport",
    "latitude_deg": 37.409400939941406,
    "longitude_deg": -84.61969757080078,
    "elevation_ft": 1265,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-KY",
    "municipality": "Stanford",
    "scheduled_service": "no",
    "gps_code": "00KY",
    "iata_code": "",
    "local_code": "00KY",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 45437,
    "ident": "00LA",
    "type": "heliport",
    "name": "Shell Chemical East Site Heliport",
    "latitude_deg": 30.191944,
    "longitude_deg": -90.980833,
    "elevation_ft": 15,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-LA",
    "municipality": "Gonzales",
    "scheduled_service": "no",
    "gps_code": "00LA",
    "iata_code": "",
    "local_code": "00LA",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  },
  {
    "id": 6544,
    "ident": "00LL",
    "type": "heliport",
    "name": "Ac & R Components Heliport",
    "latitude_deg": 39.66529846191406,
    "longitude_deg": -89.70559692382812,
    "elevation_ft": 600,
    "continent": "NA",
    "iso_country": "US",
    "iso_region": "US-IL",
    "municipality": "Chatham",
    "scheduled_service": "no",
    "gps_code": "00LL",
    "iata_code": "",
    "local_code": "00LL",
    "home_link": "",
    "wikipedia_link": "",
    "keywords": ""
  }
]
```

***SplitJSON***

| Name | Value |
| ---- | ----- |
| JsonPath Expression | `$` |
| Remove Trailing Newlines | `false` |

***ReplaceText***

| Name | Value |
| ---- | ----- |
| Search Value | `small_airport` |
| Replacement Value | `airport` |

***MergeContent***

| Name | Value |
| ---- | ----- |
| Merge Strategy | `Defragment` |