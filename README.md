# Pressure Points: map data

The map data in the game Pressure Points, offered under the **Open Database License (ODbL) 1.0**:
https://opendatacommons.org/licenses/odbl/1-0/

It's a derived database: built from OpenStreetMap and Overture Maps data, which are under the ODbL,
by the scripts listed below (in the game's source; on request where they aren't published). The
game itself is a Produced Work under its own terms.

## Credits

- **Map data © OpenStreetMap contributors**, available under the Open Database License:
  https://www.openstreetmap.org/copyright
- **Buildings and heights from Overture Maps Foundation** (its buildings theme: OpenStreetMap,
  Microsoft ML Buildings, Google Open Buildings and Esri Community Maps contributors, CC BY 4.0), under the ODbL: https://docs.overturemaps.org/attribution/
- **Washington building heights: Building Heights 1999**, Government of the District of Columbia,
  Open Data DC, under Creative Commons Attribution 4.0 (CC BY 4.0).
- **Bar categories in `places/`: Overture Maps Foundation's places theme**, overturemaps.org, under the
  Community Data License Agreement, Permissive 2.0 (https://cdla.dev/permissive-2-0/), with any
  Foursquare records under Apache 2.0.

## What's here

- **`locations/`** (21 files): Each map's ground, buildings (OSM and Overture's buildings), streets, areas, trees, signals, crossings, lamps, stops, entrances, seats and police stations. Building heights also from Overture and, in Washington, DC GIS's Building Heights 1999 (CC BY 4.0, Government of the District of Columbia). Built by `tools/fetch_location_data.py`, `tools/osm/`.
- **`places/`** (19 files): Places with signs (shops, bars, offices, worship, culture), from OSM's points of interest. Built by `tools/pois/fetch_pois.py`.
- **`transit/`** (19 files): Rail and subway lines, stations and entrances, from OSM. Built by `tools/transit/build_transit.py`, `tools/transit/build_trams.py`, `tools/transit/build_service.py`, `tools/transit/build_path_service.py`.
- **`underground/`** (13 files): The subway stations' platforms and passages, from OSM. Built by `tools/transit/build_underground.py`.
- **`buses/`** (10 files): Bus routes, stops and mapped intervals from OSM's route relations (the DC maps' WMATA Metrobus); maps whose buses come from an agency's own feed aren't here. Built by `tools/transit/build_buses_osm.py`, `tools/transit/build_buses.py`.
- **`board/`** (1 file): The campaign board's maps, drawn from the same OSM data. Built by `tools/board/build_boards.py`.
- **`cameras/`** (1 file): 2,111 surveillance cameras mapped in OSM, by map, with their kind, mount and direction where tagged. Built by `tools/cctv/` (docs/CCTV.md).

Built 2026-11-19. Each file is JSON; coordinates are metres on a local plane centred on the map
(`center_latlon` in each location file gives its origin).

## Your rights and obligations

You may copy, distribute, use and adapt this data, including commercially, under the terms of the
ODbL 1.0: credit OpenStreetMap contributors and the other sources above, and if you publicly use an
adapted version of this database, offer it under the ODbL too. The full terms are at the link above.
