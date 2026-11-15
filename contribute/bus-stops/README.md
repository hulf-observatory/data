# Bus stop contributions: community data

Sent by residents through the Hyderabad Urban Observatory's form at
https://hyderabad.urbanobservatory.in/contribute/bus-stops/ . Updated daily.

- `bus-stops-reports.csv` and `bus-stops-reports.geojson` hold the same rows.
- Times are UTC (ISO 8601). Coordinates are WGS 84. `ward` and `zone` are the 2026 corporation wards, worked out
  from the coordinates.
- One row per contribution about a bus stop. A stop can have many; the newest shows its latest state.
- `stop_id` is the stop's id in TGSRTC's open GTFS data (June 2026, Open Data Telangana). Stops residents added because they were missing from that data have ids starting `new-`, `place_type` = `missing`, and the coordinates of the pin they placed. For other stops the coordinates are TGSRTC's.
- `place_type`: how the stop was picked: `gps` (from the nearest stops to the phone; the phone's location is not kept), `search` (by name or area, or tapped on a map), `preset` (from the stop's page), `missing` (added on a map).
- `here`: `yes` if the person said they were at the stop, `no` if they described a stop they use from memory.
- Answers (empty = skipped): `what` shelter / sign (signboard only) / nothing; `shelter_state` good / worn / broken (only with a shelter); `roof` keeps people dry yes / partly / no; `seats` good (comfortable) / poor (uncomfortable) / none; `pass` can walk or wheel past without stepping onto the road; `blocked` footpath blocked no / partly / badly; `access` footpath_both, ramp (working), tactile (paving), crossing (nearby), or none; `bus_stops_at` kerb / step (one step out) / lane (in the traffic lane) / away (away from the stop); `view` ads or structures block the view of buses or stop information; `crowded` at busy times; `shade` yes / partly / no; `light` at night good / poor / none; `safe` safe / somewhat / unsafe; `floods` when it rains; `name_sign` clear / faded / missing; `route_info` current / outdated / none; `facilities` dustbin, water (drinking), toilet (in sight), cctv, board (live arrival), or none. Several values are separated by `;`.
- `improve`: one thing the person would improve, in their words. `nick`: the nickname they play under on the leaderboard, if any (made up; not a real name; its PIN is never published).
- `confirmed`: how many people later said the stop is still like this.
- The questions are a shortened version of a 2026 bus stop audit form used in Bengaluru.
- Not checked on the ground. Rows flagged as spam are left out; photos are not included.
- No names, phone numbers or IP addresses are collected.

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/) — Hyderabad Urban Observatory, community data.
