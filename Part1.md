# Assignment3Group2
Part-1:

Proposed names: ManitobaFireAPI.com
List: Return locations of fires
Parameters: Lat, Lon1, Lat2, Lon2, Date

list areas
past fires
risk/fire danger

Assignment Requirements:

API Description:  This API will allow users to query different locations in Manitoba for their past and present Fire Danger ratings.

List of endpoints with parameters:
  APi clearly described
  Suitable for a general audience
  Endpoints, parameters and resources clearly describe
Description  of resources—formatted as JSON:
Sample request with Sample response:

Example request
  ManitobaFireAPI.com/?Lat1(50)?Lon1(-97)?Lat2(52)?Lon2(-93)?severity
  Reutrns 
  {
    "onFire": "Yes",
    "severity": "Extreme"
  }
