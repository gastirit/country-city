# country-city Json List
   Repo contains two json files.
    - One is countries.json which has all ( latest) countries as a json list. Each country has its own code which is generally accepted ISO codes.
    - Other one cities.json which has all cities (most populated cities) per Region/District.
    - It can be imported to mongodb or can be used with other famous database management systems MySQL, Oracle, PostgreSQL, and SQL Server or it can be used as static source.
  
 Cities are dependent to Countries.
 in Country list you have json list. For ex:
   
   json represantation:
  > {
  >    "country" : "Country Name",
  >    "code"     : "Country ISO code"
  > }
    
    
  >[ 
  >  { "name": "United Kingdom", 
  >    **"code": "GB"** 
  >  },
  >  { "name": "United States", 
  >    **"code": "US"** },
  >    ...
  >    ...
  >    ...
  >]
  
  And you can get cities of each Country by country code. For ex:
  
  json representation
   > {
   >    "country"   : "Country code is related to countries.json" ,
   >   "geonameid" : "Geo name id (https://www.geonames.org/)",
   >    "name"      : "Name of City",
   >    "region"    : "Name of Region/District/State which city belongs to"
   > }
  
   >[
   >   {
   >     **"country": "US"**,
   >     "geonameid": 4049979,
   >     "name": "Birmingham",
   >     "region": "Alabama"
   >   },
   >   {
   >     **"country": "US"**,
   >     "geonameid": 4054378,
   >     "name": "Center Point",
   >     "region": "Alabama"
   >   },
   >   {
   >     **"country": "US"**,
   >     "geonameid": 4058219,
   >     "name": "Daphne",
   >     "region": "Alabama"
   >   },
   >   {
   >    **"country": "GB"**,
   >    "geonameid": 2643743,
   >    "name": "London",
   >    "region": "England"
   >  },
   >   ...
   >   ...
   >  ...
   >]
  
  
  
 For instance federal countries such as US,Russia,Brasil .. you can assume **region** is a state of this country and each **name** represents cities in this State.
 For instance Great Britain (GB) which is a bit different than federal countries. In this case each **region** represents a country on this island of Great Britain, such as England, Wales,Scotland and Northern Ireland. And **name** represents name of city which belongs to that country.
 For the other countries, you can assume **region** is a Region/District/State/Largest Administrative City and **name** represents city/town/province of Region/District/State/Largest Administrative City

 
 
Feel free to use it. If you want me to update anything, just let me know.

Happy coding.
      
