# Bus stop contributions: community data

Sent by residents through the Hyderabad Urban Observatory's form at
https://hyderabad.urbanobservatory.in/contribute/bus-stops/ . Updated daily.

- `bus-stops-reports.csv` and `bus-stops-reports.geojson` hold the same rows.
- Times are UTC (ISO 8601). Coordinates are WGS 84. `ward` and `zone` are the 2026 corporation wards, worked out
  from the coordinates.
- Published times (`observed_at` on the map and in the download) are rounded down to the hour, since rows carry a nickname (from 16 Nov 2026).
- One row per contribution about a bus stop. A stop can have many; the newest shows its latest state.
- `stop_id` is the stop's id in TGSRTC's open GTFS data (June 2026, Open Data Telangana). Stops residents added because they were missing from that data have ids starting `new-`, `place_type` = `missing`, and the coordinates of the pin they placed. For other stops the coordinates are TGSRTC's.
- `place_type`: how the stop was picked: `gps` (from the nearest stops to the phone; the phone's location is not kept), `search` (by name or area, or tapped on a map), `preset` (from the stop's page), `missing` (added on a map; since 16 Nov 2026 within 100 m of where the person stood), `map` (since 16 Nov 2026: the phone's location failed, so the person found the stop under a pin on a map, at the stop). `located`: phone or map, how the person's own place was found.
- `stop_place` (asked only of people at the stop who shared their location): is the stop where TGSRTC's data puts it? yes / here (no, it is where the person stood: `stop_lat`, `stop_lng` are their phone's location) / marked (no, they dragged it: `stop_lat`, `stop_lng` are where they put it) / dk (not sure). Corrections are as given, not checked.
- `here`: `yes` if the person said they were at the stop, `no` if they described a stop they use from memory.
- Answers (empty = skipped, or not asked because of an earlier answer): `shelter` yes / no; if yes `shelter_state` good / broken and `shelter_protects` (from sun and rain) yes / partly / no; if no `shade` (from trees or buildings) yes / partly / no. `seats` yes / no; if yes `seats_state` good (comfortable) / poor (uncomfortable) / broken. `footpath` yes / no; if yes `blocked` no / partly / badly and `pass` (can walk or wheel past without stepping onto the road) yes / no. `access` ramp (working), tactile (paving), or none. `crossing` (a pedestrian crossing near the stop: zebra, signal, foot overbridge or subway) yes / no; if yes `crossing_safe` (feels safe to cross) yes / somewhat / no. `bus_stops_at` kerb / step (one step out) / lane (in the traffic lane) / away (away from the stop). `view` ads or structures block the view of buses or stop information. `room`: enough room to wait at busy times, yes / no. `light` (at night) yes / no / dk (don't know); if yes `light_state` good / poor. `safe_day` and `safe_night` (how safe it feels to wait there during the day / after dark) safe / somewhat / unsafe. `floods` when it rains. `name_sign` yes / no; if yes `name_state` clear (easy to read) / faded. `route_info` yes / no; if yes `route_state` current / outdated. `facilities` dustbin, water (drinking), toilet (in sight), cctv, board (live arrival), or none. Several values are separated by `;`.
- `improve`: one thing the person would improve, in their words. `nick`: the nickname they play under on the leaderboard, if any (made up; not a real name; its PIN is never published).
- `confirmed`: how many people later said the stop is still like this; `disputed`: how many said something is wrong.
- `located`: how the place was given — `phone` (the phone's location, standing there), `map` (standing there, but the phone's location failed, so the person put the place under a pin on a map) or `memory` (not there when sending: the person knows the place well and marked it on the map from memory; `observed_at` is then the time it was sent). Use it to weigh rows: `phone` is the most reliable. `here`: `yes` (at the stop) or `known` (from memory).
- The questions are a shortened version of a 2026 bus stop audit form used in Bengaluru.
- Not checked on the ground by us. `confirmed`: how many other people (one count per device) later said the row is
  still right; `disputed`: how many said something about it is wrong. Rows flagged as spam are left out; photos are
  not included.
- No names, phone numbers or IP addresses are collected.

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/) — Hyderabad Urban Observatory, community data.
