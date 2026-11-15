# Water tanker orders: community data

Sent by residents through the Hyderabad Urban Observatory's form at
https://hyderabad.urbanobservatory.in/contribute/tankers/ . Updated daily.

- `tankers-reports.csv` and `tankers-reports.geojson` hold the same rows.
- Times are UTC (ISO 8601). Coordinates are WGS 84. `ward` and `zone` are the 2026 corporation wards, worked out
  from the coordinates.
- One row per tanker order, sent by the person who ordered it (or who looks after a building's water). The same home can send many orders; nothing links them.
- Place: the sender chose how exactly to share it (`place_detail`): `exact` (the phone's location or a map pin), `500m` (moved to the nearest point of a grid about 500 m apart), `area` (the centre of a colony or area they searched; its name in `place`), or `ward` (no coordinates at all). `ward` and `zone` are given for every row that falls inside the 2026 corporation wards.
- `for`: home (one household) or building (someone who looks after the building's water); `building` house / house_rented (house with rented portions) / apartment_small (up to 20 flats) / apartment_large (over 20 flats) / basti / other; `households` sharing the tank or sump.
- `supplier`: hmwssb (the water board), private, society (arranged by the residents' association), other. `size_l`: litres, 5000 / 10000 / 20000 (20,000 or more) / dk (didn't know).
- `paid`: paid / free / dk (the sender didn't know the price, e.g. the association paid); `price`: rupees paid for that one tanker, only when `paid` = paid; `extra`: rupees given to the driver on top. As told by the sender; not checked.
- `ordered_on` (date) and `ordered_tod` (morning / afternoon / evening / night): when it was ordered. `observed_at` is the same date. `came`: same_day / next_day / 2_days / 3_days (3 or more) / not_yet (still waiting when sent) / never.
- `tankers_week`: how many tankers the same home or building orders in a usual week (0 = less than once a week, 30 = 30 or more). `season`: when they usually need tankers: summer (only in summer, March to June) / summer_and_more (summer and some other months) / all_year / first_time. `why`: piped_irregular (piped water doesn't come often enough), piped_low (comes, but too little), borewell (dried up or gave less), no_connection, other; several separated by `;`.
- Not checked on the ground. Rows flagged as spam are left out; photos are not included.
- No names, phone numbers or IP addresses are collected.

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/) — Hyderabad Urban Observatory, community data.
