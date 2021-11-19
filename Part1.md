# Assignment3Group2
Part-1:

Proposed names: ManitobaFireAPI.com
List: Return locations of fires
Parameters: Lat1, Lon1, Lat2, Lon2, Date

list areas
past fires
risk/fire danger

Assignment Requirements:

API Description:  This API will allow users to query different locations in Manitoba for their past and present Fire Danger ratings.

List of endpoints with parameters:
  APi clearly described
  Suitable for a general audience
  Endpoints, parameters and resources clearly describe
  
  Parameters:
    Lat1: The latitude of the upper-left corner of the area to query
    Lon1: The longitude of the upper-left corner of the area to query
    Lat2: The latitude of the bottom-right corner of the area to query
    Lon2: The longitude of the bottom-right corner of the area to query
    Date (optional): The date about which information is returned. Defaults to most recent data.
    
Description  of resources—formatted as JSON:
Sample request with Sample response:

Example request
  ManitobaFireAPI.com/?Lat1(50)?Lon1(-97)?Lat2(52)?Lon2(-93)?severity
  Reutrns 
  {
    "onFire": "Yes",
    "severity": "Extreme"
  }
