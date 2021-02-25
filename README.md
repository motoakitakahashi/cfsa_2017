# A Concordance Table for CFS 2017 Areas
The Commodity Flow Survey (CFS) records trade volume and trade values of various sectors across the US regions. The finest geographic units adopted by CFS are CFS areas, which are finer than states and more coarse than counties.

The US Census Bureau publishes the shape file for 2017 CFS areas, which enables us to create maps and to analyze geography of CFS areas using QGIS or ArcGIS.
https://www.census.gov/programs-surveys/cfs/technical-documentation/geographies.html
On the other hand, the Census Bureau gives trade data across CFS areas.
https://www.census.gov/data/tables/2017/econ/cfs/aff-2017.html
For example, if you would like to download the trade values across CFS areas by sectors classified by North American Industry Classification System, go to
https://www2.census.gov/programs-surveys/cfs/data/2017/
and download "CF1700A25.zip."

A problem is that the shape file and the trade data do not share the consistent identifiers for CFS areas. Both seem to have a number to identify a CFS area. However, for example, Albany-Schenectady CFS area of New York state has the id "36091" in the shape file, and has the id "E330000US3610400000" in the trade data. Thus it is difficult to merge the information in the shape file and the one in the trade data.

Therefore I made a concordance table that maps identifiers for CFS areas in the shape file to those in the trade data. Both "cfsa_concordance.csv" and "cfsa_concordance.rda" contain the same information. I describe variables in them:
- geoid_shape: the identifiers for CFS areas in the shape file
- geottl_shape: the names of CFS areas in the shape file
- state: the states to which CFS areas belong
- geoid_trade: the identifiers for CFS areas in the trade data
- geottl_trade: the names of CFS areas in the trade data
