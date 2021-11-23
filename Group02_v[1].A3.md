## Manitoba Fire Risk API [Group 2]

### API Description
This API will allow users to query different locations in Manitoba for their past and present Fire Danger ratings.

### List of endpoints with parameters
#### Endpoint: 
Simple **GET** request to https://ManitobaFireAPI.com. 
#### Parameters:
- **Lat1**(float): The latitude of the first corner of the area to query.
- **Lon1**(float): The longitude of the first corner of the area to query.
- **Lat2**(float): The latitude of the opposite corner of the area to query.
- **Lon2**(float): The longitude of the opposite corner of the area to query
- **Date**(string): (optional) The date about which information is returned. Defaults to most recent data.

### Description of resources
The data returned is queried from time stamped 2d true/false arrays of current Manitoba fire reports. The array axes are latitude and longitude coordinates in Manitoba.
- **currentStatus**(string): If there is ongoing fire or not
- **nearbyRisk**(string): The severity of the fire
- **underControl**(string): If the fire is under control or not

### Sample requests
`https://ManitobaFireAPI.com/?Lat1(49)?Lon1(-100)?Lat2(55)?Lon2(-102)?Date(20210522)`  
`https://ManitobaFireAPI.com/?Lat1(50)?Lon1(-97)?Lat2(52)?Lon2(-93)`

### Sample response
```
[
  {
    "fire": {
      "fireID": "MB21_1_2042",
      "currentStatus":"burning",
      "since": "11-11-2021",
      "until": "now",
      "area": "White Shell",
      "Lat1": -83.01,
      "Lon1": 111.09,
      "Lat2": -82.71,
      "Lon2": 111.49,
      "Moving": "SE",
      "Speed": "1.5km/h",
      "windSpeed":12km/h,
      "nearbyRisk": "low",
      "underControl": "yes"
    },
    "msg": ""
  }
  {
    "risk": {
      "fireID": "N/A",
      "currentStatus":"potential",
      "since": "11-11-2021",
      "until": "now",
      "area": "White Shell",
      "Lat1": -83.01,
      "Lon1": 111.09,
      "Lat2": -82.71,
      "Lon2": 111.49,
      "Moving": "N/A",
      "Speed": "N/A",
      "windSpeed":12km/h,
      "nearbyRisk": "dangerous",
      "underControl": "following"
    },
    "msg": ""
  }
]
```

