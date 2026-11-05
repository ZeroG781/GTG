# Data sources, licences and usage rules

GTG Converter only connects to services that are free and need **no API key or account**. It ships no map data itself; your browser loads it directly when you use the tool.
Licences apply to **the data**, and therefore to the maps you build from it. Every export ZIP includes `ATTRIBUTION.txt` with the text for your map credits.

## OpenStreetMap – vectors, surface masks, place names
- **Service:** Overpass API (`overpass-api.de`, fallback `overpass.kumi.systems`)
- **Licence:** Open Database License (ODbL) 1.0
- **Credit:** `© OpenStreetMap contributors` – https://www.openstreetmap.org/copyright
- **Share-alike:** a published database derived from OSM (e.g. the shapefiles) must stay under the ODbL. A finished game map is usually a "produced work" – credit is required.
- **Usage:** one query per scan; results are cached for 7 days in the browser.

## Mapzen Terrain Tiles on AWS – elevation
- **Service:** `s3.amazonaws.com/elevation-tiles-prod/terrarium` – https://registry.opendata.aws/terrain-tiles
- **Required attribution (core sources):**
  - 3DEP (formerly NED), GMTED2010 and SRTM terrain data courtesy of the U.S. Geological Survey
  - ETOPO1 terrain data U.S. National Oceanic and Atmospheric Administration
  - Europe terrain data produced using Copernicus data and information funded by the European Union – EU-DEM layers
  - Further regional sources: https://github.com/tilezen/joerd/blob/master/docs/attribution.md

## Sentinel-2 cloudless (EOX) – satellite colour (default)
- **Service:** `tiles.maps.eox.at` – https://s2maps.eu
- **2016 layer:** CC BY 4.0 – commercial use allowed with attribution
- **2018 and later:** CC BY-NC-SA 4.0 – **non-commercial use only**
- **Credit:** `Sentinel-2 cloudless – https://s2maps.eu by EOX IT Services GmbH (Contains modified Copernicus Sentinel data <years>)`

## OpenTopoMap – rendered topographic map (default background, optional export)
- **Service:** `tile.opentopomap.org`
- **Licence:** CC BY-SA
- **Credit:** `Map data: © OpenStreetMap contributors, SRTM | Map style: © OpenTopoMap (CC-BY-SA)`
- **Rule:** keep exports small – https://opentopomap.org/about

## OpenStreetMap standard tiles – background only
- **Service:** `tile.openstreetmap.org` – shown as a map background, never exported (the tile usage policy forbids bulk download).

## Your own sources (XYZ, WMS, local DEM)
You enter these yourself and are responsible for their licence and any access key. Many national mapping agencies publish open orthophotos and DEMs (e.g. German state DOP/DGM under dl-de/by-2-0 or dl-de/zero-2-0).

## Not included
- **Place-name search:** removed. The public geocoders either need a key or do not allow use from apps like this. Search by coordinates instead.
- **Esri World Imagery:** removed. Its licence is tied to Esri's own terms and platform.
