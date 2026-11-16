# Flood reports: community data

Sent by residents through the Hyderabad Urban Observatory's form at
https://hyderabad.urbanobservatory.in/contribute/flood/ . Updated daily.

- `flood-reports.csv` and `flood-reports.geojson` hold the same rows.
- Times are UTC (ISO 8601). Coordinates are WGS 84. `ward` and `zone` are the 2026 corporation wards, worked out
  from the coordinates.
- One row per report.
- `place_type`: `gps` = the phone's location (`accuracy_m` says how close; since 16 Nov 2026 every new report is made at the place, from the phone, and the sender may move the point up to 100 m to the water), `search` = a place found by name plus the street and landmark given, `map` = a pin placed on a map, `legacy-pin` = a pin from the earlier flood report form (June–September 2026).
- `depth_cm`: 30 = half the tyre or less, 60 = over the tyres, 90 = door handles, 140 = over the car roof, 200 = door height; other values were set exactly with a slider (`depth_exact` = true).
- `quality`: murky (muddy), contaminated (full of garbage), sewage, or cant_say (the sender couldn't say, since 15 Nov 2026); several may apply, separated by `;`; `clear` appears only in the earlier form's reports.
- `confirmed`: how many other people said "I saw this too".
- Not checked on the ground. Rows flagged as spam are left out; photos are not included.
- No names, phone numbers or IP addresses are collected.

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/) — Hyderabad Urban Observatory, community data.
