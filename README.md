# GTG Converter – GIS to Game

A browser tool that turns real-world terrain into game-ready map data.
Pick a map sector, then export heightmaps, satellite images, surface masks and shapefiles for Arma Reforger (Enfusion), Unreal Engine, Unity and other engines.

No install, no account, no API keys.

**[▶ Open the tool](https://USERNAME.github.io/gtg-converter/)** · [Changelog](CHANGELOG.md) · [Data sources](DATA_SOURCES.md) · [Privacy](PRIVACY.md)

<!-- Add a screenshot as docs/screenshot.png, then remove this comment line -->
![Screenshot](docs/screenshot.png)

## Features

- **Map sector** – presets from 1 km² to 1,074 km², free size, 1:1 lock, UTM grid
- **Heightmap** – AWS terrain tiles, your own DEM (GeoTIFF/ASC) or WMS; exports `.asc`, 16-bit `.png`, `.raw`, `.r32`, GeoTIFF
- **Satellite map** – Sentinel-2 cloudless, OpenTopoMap, or your own XYZ/WMS orthophotos
- **Shapefiles** – roads, rails, water, land use, buildings from OpenStreetMap; edit, rename, draw your own
- **Special zones** – craters, trenches, berms, dams, quarries, dunes, terraces and more, applied to the heightmap
- **Surface masks** – per-surface PNGs with Enfusion block check
- **Engine profiles** – import values for Arma Reforger, Unreal and Unity
- **12 languages**, guided wizard, built-in manual, undo/redo, session autosave

## Quick start

1. Open the tool in a current Chrome, Edge or Firefox (desktop).
2. Type coordinates into the search box (e.g. `39.92, 25.23`) and press Enter.
   Tip: right-click a place in Google Maps or OpenStreetMap to copy its coordinates.
3. Set the sector size in **1 · Map sector dimension & resolution**.
4. Press **Export sector with default settings** – or export each part from sections 2–4.
5. Use **Export params** (section 1) for the engine import values, and copy `ATTRIBUTION.txt` from the ZIP into your map credits.

## Run it locally

It is a single HTML file. Download `index.html` and open it in your browser.
An internet connection is still needed for map tiles, OpenStreetMap data and the libraries loaded from CDNs.

## Data and attribution – read before you publish a map

The tool only uses free services that need no key. **You** are responsible for following their licences in the maps you build.
Every export ZIP contains an `ATTRIBUTION.txt` with the required credits.

| Data | Licence | What you must do |
|---|---|---|
| OpenStreetMap (vectors, masks, names) | ODbL 1.0 | Credit "© OpenStreetMap contributors"; derived data stays ODbL |
| Mapzen Terrain Tiles (elevation) | Source-dependent | Credit USGS, NOAA, Copernicus EU-DEM etc. (see DATA_SOURCES.md) |
| Sentinel-2 cloudless 2016 | CC BY 4.0 | Credit EOX + Copernicus |
| Sentinel-2 cloudless 2018+ | CC BY-NC-SA 4.0 | Non-commercial use only |
| OpenTopoMap | CC BY-SA | Credit; derived images stay CC BY-SA |

Full details: [DATA_SOURCES.md](DATA_SOURCES.md)

## Privacy

No account, no server, no tracking. Settings are stored in your browser only. See [PRIVACY.md](PRIVACY.md).

## Licence

Code: [MIT](LICENSE). Third-party libraries and fonts: [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

Not affiliated with Bohemia Interactive, EOX, the OpenStreetMap Foundation or any data provider. "Arma" and "Enfusion" are trademarks of Bohemia Interactive a.s.

## Feedback

Report bugs and ideas under [Issues](../../issues). Include the browser, the sector coordinates and the exported params `.json`.
