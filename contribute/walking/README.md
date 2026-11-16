# Walking: footpaths and crossings: community data

Sent by residents through the Hyderabad Urban Observatory's form at
https://hyderabad.urbanobservatory.in/contribute/walking/ . Updated daily.

- `walking-reports.csv` and `walking-reports.geojson` hold the same rows.
- Times are UTC (ISO 8601). Coordinates are WGS 84. `ward` and `zone` are the 2026 corporation wards, worked out
  from the coordinates.
- One row per footpath spot or crossing, sent by a person standing there (from their phone's location; they may move the point up to 100 m, so they can stand somewhere safe). Started 16 Nov 2026. `place_type`: `gps` (the phone's location, `accuracy_m` how close) or `map` (the phone's location failed, so the person put the place under a pin on a map; single spots and crossings only).
- `item`: `spot` (a footpath spot) or `crossing`. `mode`: how it was sent: a single `spot`, a single `crossing`, or as part of a `walk` — rows of the same walk share a `walk_id` and are numbered in order by `seq`. The route between the points is not kept.
- `side` (footpath spots): the side of the road the person stood on, north / east / south / west. `side_how`: `phone` (they pointed the phone at the road and its compass gave the direction; they are on the opposite side) or `buttons` (they chose which way they faced, `facing` n/e/s/w, and left or right). `facing` on a walk is the direction they were walking. `same` = true: the person said this spot was the same as the one before on their walk, and the answers were copied.
- Footpath answers (empty = skipped, or not asked because of an earlier answer): `footpath` yes / no on their side; if no, `other_side` yes / no / dk and `walk_where` road / edge (dirt or gravel edge) / parked (between parked vehicles) / cross (people cross to the other side); if yes, `walkable` easy / somewhat / hard, `blocked` no / partly / fully with `blocked_by` vehicles / shops (or vendors) / debris (building material) / garbage / poles (poles, trees or transformers) / other, `damaged` no / some (in places) / badly with `damage` slabs (broken or loose) / drain (open drain or manhole) / holes (or dug up) / uneven (steps or uneven height) / other, and `access` (usable with a wheelchair or pram) yes / partly / no. Always: `shade` most / some / none, `lights` working / broken / none / dk, `safe_day` and `safe_night` safe / somewhat / unsafe (/ dk: not been after dark). Several values are separated by `;`.
- Crossing answers: `x_where` junction / between (junctions); `x_marked` zebra / faded / none; `x_signal` (for people walking) working / broken / none, and if working `x_time` (enough time to cross) yes / just / no; `x_stop` (vehicles stop for people crossing) usually / sometimes / rarely; `x_divider` yes / no, and if yes `x_gap` (a gap to walk through) level / climb / none; `x_wait` (space to wait safely) yes / cramped / no; `x_lit` (at night) yes / poor / no / dk; `x_kerb` (easy on and off the footpath with a wheelchair or pram) yes / partly / no; `x_fob` (foot over bridge or subway nearby) used / unused / no; `x_safe` (feels safe to cross) safe / somewhat / unsafe.
- `note`: in the person's words. `nick`: the nickname they contribute under on the leaderboard, if any (made up; its PIN is never published). `confirmed`: how many people later said it is still like this.
- Not checked on the ground. Rows flagged as spam are left out; photos are not included.
- No names, phone numbers or IP addresses are collected.

Licence: CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/) — Hyderabad Urban Observatory, community data.
