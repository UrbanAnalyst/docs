Data Sources
###############

The Urban Analyst platform aims to be applicable to as much of the world as
possible. To achieve this, data sources are chosen which are ideally have
global coverage, and which are not specific to any one city. The global sources used are:

- `Open Street Map <https://openstreetmap.org>`_ for all data on traversable
  ways, natural spaces, parking infrastructure, and locations of schools.
- Population density data from the `European Union *Global Human Settlement
  Layer* <https://ghsl.jrc.ec.europa.eu/index.php>`_.
- Elevation data from `NASA Earth Observation
  Data <https://www.earthdata.nasa.gov/>`_, used to include effects of incline
  on both pedestrian and bicycle travel times.

The following additional data are then required for each city:

- Data on some measure of socio-demographic inequality or disadvantage, such as
  rates of unemployment, quantified within a series of polygonal shapes which
  are also used to define each city.
- Data on public transport timetables in *General Transit Feed Specification*
  (GTFS) format, or in other formats able to be converted to GTFS format.

The last of these data requirements is the most restrictive, as most cities of
the world do not have or provide public transport data in GTFS format. There
are nevertheless thousands of cities which do provide GTFS feeds, as can be
seen for example in the GTFS feed aggregation platform
`transit.land <https://transit.land>`_.

For USA cities, data for the additional two variables of housing value and
rental price per room are obtained from US Government census data.
