# Assignment3 Group2
Part-1:

### Proposed names: 
ManitobaFireAPI.com
### List: 
Return locations of fires
### Parameters: 
Lat1, Lon1, Lat2, Lon2, Date

list areas
past fires
risk/fire danger

Assignment Requirements:

**API Description:  This API will allow users to query different locations in Manitoba for their past and present Fire Danger ratings.**

List of endpoints with parameters:
  APi clearly described
  Suitable for a general audience
  Endpoints, parameters and resources clearly describe
  
  **Parameters:
    Lat1: The latitude of the upper-left corner of the area to query
    Lon1: The longitude of the upper-left corner of the area to query
    Lat2: The latitude of the bottom-right corner of the area to query
    Lon2: The longitude of the bottom-right corner of the area to query
    Date (optional): The date about which information is returned. Defaults to most recent data.**
    
 **Resource: The data returned is queried from time stamped 2d true/false arrays of current Manitoba fire reports. The array axes are latitude and longitude coordinates in Manitoba.**
    
Description  of resources—formatted as JSON:
Sample request with Sample response:
A response is received as:
##  
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
      "NearbyRisk": "low",
      "underControl": "yes"
    },
    "msg": ""
  }
]
```


Example request
  ManitobaFireAPI.com/?Lat1(50)?Lon1(-97)?Lat2(52)?Lon2(-93)?severity
  Reutrns 
  {
    "onFire": "Yes",
    "severity": "Extreme"
  }
