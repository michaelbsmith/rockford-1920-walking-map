# Rockford 1920 Walking Reach

How far you could walk from any point in Rockford, Illinois, in a given time, and which 1920 businesses fall inside that reach. Same page and controls as the Rockford Walking Reach map, with the businesses of *McCoy's Rockford City Directory* (1920) in place of today's amenities.

## Features

- Click the map or drag the marker to set a start point; set the time budget and walking speed.
- Search 1920 businesses by name, type (for example "grocer", "tailor") or address; search any present-day Rockford address to use it as the start point.
- Click a dot for its directory listing. Tick or untick a kind of business to show or hide it.
- Counts of each kind of business within 1, 2 and 3 miles (straight line) of the start point, with rings on the map.

## Run locally

`python3 -m http.server 8000` in this folder, then open http://localhost:8000 (opening index.html directly does not work).

## Rebuild the business points

`python3 build_pois.py ../Rockford_1920_Businesses.xlsx` (needs `openpyxl`). Only directory listings the Census geocoder matched get a point. Home-based listings (private nurses, dressmakers, music teachers, ministers) are left out.

## Today's addresses

`MAPBOX_TOKEN` near the top of `index.html` holds a public Mapbox token restricted to this site's address. If it is empty the page falls back to the free Photon service.

## Limits

The street network is today's OpenStreetMap network, not 1920's. Public transport, slope and lighting are not included. About a quarter of the directory listings could not be matched to a modern address and do not appear.

## Credits

Street data © OpenStreetMap contributors (ODbL); basemap © OpenFreeMap, © OpenMapTiles; based on "15 minutes. For whom?" by Martin Bangratz (MIT, see LICENSE). Business listings: McCoy's Rockford City Directory (1920), geocoded with the U.S. Census Bureau geocoder.
