# Mission Un-choke: My City, My Sujhaav: community data

Sent by residents through the Hyderabad Urban Observatory's form at
https://hyderabad.urbanobservatory.in/contribute/unchoke-hyd/ . Updated every hour.

- `unchoke-hyd-reports.csv` and `unchoke-hyd-reports.geojson` hold the same rows.
- Times are UTC (ISO 8601). Coordinates are WGS 84. `ward` and `zone` are the 2026 corporation wards, worked out
  from the coordinates.
- A small survey the Hyderabad Urban Observatory made for the citizens' group Let's Un-choke Hyderabad, from the group's own form (November 2026). It is kept apart from the Observatory's streets and bus stop data. One row is one place a person told us about.
- `about`: zebra (a bus stop with no zebra crossing), cycle (a bus stop that needs cycle parking), footpath, lights (street lights) or vehicle_free (a street or market to make walking-only). A row has only its own choice's answers; the other columns are empty.
- Bus stop rows (`about` zebra or cycle): `stop_id` is the stop's id in TGSRTC's open GTFS data (June 2026, Open Data Telangana), with `stop_name` and `towards`; `lat`/`lng` are then the stop's. `stop_new` = true: the person added a stop that is not in that data, with the name they gave and the place they marked.
- `crossing` (a crossing near the stop: zebra, signal, foot overbridge or subway, within about 100 metres) yes / no; if yes `crossing_marked` zebra / faded / none; `crossing_can` (can you cross the road here) yes / hard (with difficulty) / no.
- `cycle_stand` (a cycle stand at the stop now) yes / no; `cycle_space` (space for one, without blocking the footpath) yes / little / no; unless no, `cycle_room` (how many cycles could be parked) upto5 / 6to10 / over10.
- `footpath` yes (most of the way) / parts (only in parts) / no; if yes or parts: `broken` and `blocked` no / places / mostly, and if blocked `blocked_by` parked (vehicles) / vendors (or shops) / works (construction or debris) / poles (poles, trees or transformers) / garbage. Several values are separated by `;`. These use the same codes as the streets data.
- `street_lights`: not_working (a street light isn't working) / dark (it's dark, no street lights) / asked (street lights asked for).
- `vf_name`: the street or market, in the person's words; `vf_hours` (when it should be vehicle-free) all_day / hours (certain hours) / market_days.
- `dk` = the person said they don't know. `note`: in the person's words.
- `located`: phone (standing there, the phone's location) / map (standing there, a pin on a map) / memory (not there when sending: marked on a map; `observed_at` is then the time it was sent). `place_type`: gps or map. Published times are rounded down to the hour.
- `photos`: the row's photo files in the `photos/` folder beside this file, separated by `;` (up to 6). The location stored in a photo was removed before it was saved.
- Not checked on the ground by us. `confirmed`: how many other people (one count per device) later said the row is
  still right; `disputed`: how many said something about it is wrong. Rows flagged as spam are left out; photos flagged as unsuitable are left out too.
- The sender's name (needed), email and phone number (optional) are private: kept apart from this data, for
  a while, only to ask about an entry if there are questions, and never published. No IP addresses are collected.

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/) — Hyderabad Urban Observatory, community data.
