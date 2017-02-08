## Point-by-Point Files

Point-by-point data for tennis matches.  All matches have been validated using the [Universal Match Object](https://github.com/TennisVisuals/universal-match-object) to insure that point progressions produce scores that match  'official' scores.

The format of these files follows the format established by [Jeff Sackmann's GitHub repository](https://github.com/JeffSackmann/tennis_pointbypoint) and adds additional attributes.

For the first time there are also Doubles Matches.

Matches are represented on a single row of each file.  The attributes for each match are:

- date
- start_time
- tournament
- tour
- draw
- server1 (The player who served first)
- server2
- winner (0 for server1, 1 for server2)
- pbp (coded representation of point progression)
- score
- adf_flag (boolean: whether the pbp sequence contains Aces/Double Faults)
- round
- surface
- duration
- server1_ioc (ioc code for country player represents)
- server2_ioc

Characters in the PBP field each represent one point:

- S (Server Won)
- R (Returner Won)
- A (Ace - Server Won)
- D (Double Fault - Returner Won)

For files where the boolean **adf_flag** is **true** lowercase letters indicate that the point was played on a ***2nd Serve***.

Files names which end in **_pbp.csv** contain points coded with only 'S' and 'R'.  Files which end in **_pbpx.csv** contain points with richer detail.  This means that currently the **adf_flag** is redundant; in the future all files will be combined and there will be no duplication of matches. Where rich point coding is available it will be favored.
