This is a multi taskable system which includes following important tasks:
--> Mapping current location.
--> Routing paths from source to destination.
--> Calculating distance from source to destination.
--> Mapping temperature of specific regions.


Here we try to avoid using the Google API's to not to be reliant on. Following are the libraries and methods followed for making this project.
1. For mapping current location
import requests
result = requests.get('https://ipinfo.io/')

2. For calculating optimal routes
from geopy.exc import GeocoderTimedOut 
from geopy.geocoders import Nominatim    #For calcualting latitudes and longitudes
import gmplot                            #For routing

3. For calculating distance
Here we use haversine distance formula

4. For temperature mapping
Since there is no specific library aor Google API(considering), we try to scrape the data from Google itself using beautiful soup.
We try to map these temperatures then using Plotly Choropleth Map (still researching)
