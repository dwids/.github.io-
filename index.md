# Welcome to my MD webpage
## Overview
This page is for lots of things.

# Open Street Map nominatim - Geolocation - json reply parsing

### First test with hard-coded URL 
```python
# https://www.geeksforgeeks.org/how-to-read-a-json-response-from-a-link-in-python/
import json
from urllib.request import urlopen
url = "https://nominatim.openstreetmap.org/reverse?format=json&lat=-37.53523861228984&lon=145.75341831179136"
data = urlopen(url)
data_json = json.loads(data.read())
print(data_json)
```

Results in:
```
{'place_id': 18791685, 'licence': 'Data © OpenStreetMap contributors, ODbL 1.0. [https://osm.org/copyright',](https://osm.org/copyright',) 'osm_type': 'node', 'osm_id': 1917067712, 'lat': '-37.535448', 'lon': '145.753439', 'display_name': 'Keppel Lookout, Keppel Lookout Trail, Marysville, Shire of Murrindindi, Victoria, 3779, Australia', 'address': {'tourism': 'Keppel Lookout', 'road': 'Keppel Lookout Trail', 'suburb': 'Marysville', 'municipality': 'Shire of Murrindindi', 'state': 'Victoria', 'postcode': '3779', 'country': 'Australia', 'country_code': 'au'}, 'boundingbox': ['-37.535498', '-37.535398', '145.753389', '145.753489']}
```

Now extract and print the ones we are interested in:
```python
addrTourism = data_json['address']['tourism']
addrRoad = data_json['address']['road']
addrSuburb = data_json['address']['suburb']
addrMunicipality = data_json['address']['municipality']
addrState = data_json['address']['state']
lat = data_json['lat']
lon = data_json['lon']
# 
print("Tourism Address:",addrTourism)
print("Road:",addrRoad)
print("Suburb:",addrSuburb)
print("Municipality:",addrMunicipality)
print("State:",addrState)
print("Latitude:",lat)
print("Longitude:",lon)
```
Gives us:
```
Tourism Address: Keppel Lookout
Road: Keppel Lookout Trail
Suburb: Marysville
Municipality: Shire of Murrindindi
State: Victoria
Latitude: -37.535448
Longitude: 145.753439
```

#todo

#### The 'No Tourism' problem
My 2nd attempt to use the above crashed; the location had no `addrTourism = data_json['address']['tourism']` .  It may not have had a `road` too, viz think of a photo taken on Mallacoota Lakes or in the middle of Wyperfeld.  Try those.



