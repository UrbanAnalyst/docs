4. UA Variables
###############

All UA variables are measured such that lower or negative values are good,
whereas higher values are bad. (Exceptions are neutral variables such as
population density which are nevertheless straightforward to interpret.) For
example, unemployment or transport times are both better when values are lower.
Indices of bicycle infrastructure and access to natural spaces are also
transformed so that lower values indicate better or more of either. In these
cases, the transformations are simply one minus the respective proportions of
journeys out to a fixed distance travelled along bicycle infrastructure, or
through or alongside natural spaces. Values of 0 then reflect 100% of all
journeys spent on bicycle infrastructure or in natural spaces, while values of
1 would represent complete absence of either bicycle infrastructure or natural
spaces.

Variables are measured for every way, path, or street intersection within each
city. Values for the maps are aggregated within polygons defined by the
*Socio-demographic variables* described in the following sub-section, while
values within the statistics page are aggregated across entire cities. Unless
explicitly described otherwise, values of all variables are weighted by
population density. This means that, for example, distances to nearest schools
represent average distances that each person must travel to get to school. Full
descriptions of the calculation of all variables are given in the :ref:`*Software
and Algorithms* chapter<6. Software and Algorithms>`.

Socio-demographic variables
***************************

The extent and structure of each city is defined by its "socio-demographic
variable," or "social variable" for short. These are taken from open-source
datasets provided by the cities as a series of geographic areas, defined as
polygonal shapes, and some corresponding measure of socio-demographic
disadvantage. The cities themselves decide the resolution and extent of these
polygonal data. These polygons then define the extent and shape of cities
analysed in Urban Analyst, and the individual polygons into which the map data
are aggregated.

Values of these socio-demographic variables are the only aspect that differs
between different cities. One of the simplest versions is unemployment rate,
generally measured either as a percentage (0-100), or a proportion (0-1). The
UA platform selects the most representative measure of general social
disadvantage provided by each city, and defaults to rates of unemployment only
where no more comprehensive of integrative measures are openly provided by
cities.

Travel Variables
****************

Urban Analyst provides highly detailed statistics on transport systems. Many of
these are derived from estimates of times required to travel fixed distances of
10km. This value is chosen to capture the general efficiency of public
transport systems. Shorter distances do not sufficiently capture the influence
of transport modes such as express or long-distance train services, while
longer distances unfairly penalise smaller cities in which most journeys are
only of shorter distances.

Values at this distance of 10km are obtained by following these three steps,
taking the example statistic of travel times:

1. Calculate total travel times from all street intersections to all other
   street intersections within a city.
2. Calculate a straight line of "best fit" (a "least squares regression" line)
   which describes how travel times vary with distance.
3. Use that line to obtain the "average" value of travel time at the distance
   of 10km.

Values shown in the maps are aggregated within each polygon of a chosen city,
while values shown in the statistics page are aggregated over entire cities.

The remainder of this section describes the five travel variables:

- Absolute travel times
- Relative travel times
- Numbers of transfers
- Intervals between consecutive services
- Compound travel statistic

Absolute and Relative Travel Times
==================================

Urban Analyst enables comparisons of travel times between two primary modes of
transport:

- *Private Automobile.* Travel times with private automobile are used as a
  benchmark for measures of travel time using other modes. UA generates
  realistic estimates of private automobile travel times through scaling to
  empirically observed data on actual vehicular travel times. (Calibration
  procedures are implemented and documented in `this GitHub
  repository <https://github.com/UrbanAnalyst/ttcalib>`_.) Importantly, UA
  includes an additional, unique aspect of automobile travel times not
  quantified in any other equivalent system, through an algorithm to accurately
  estimate the likely time required to park a private vehicle, and then to walk
  to a desired destination. These parking times are crucial, as direct travel
  times to many inner-city destinations do not provide realistic estimates of
  actual journey times to locations where it may be impossible to actually park
  a private automobile.

- *Multi-Modal Transport.* UA's "multi-modal travel times" represent fastest
  possible times taken for journeys from every single point in a city to travel
  10km using any combination of transport modes excluding private automobile.
  The primary modes considered are walking, bicycling, and all available modes
  of public transport within each city. Where it is faster to cycle 10km than
  to take public transport (such as from locations with very poor public
  transport connections, or on the top of long hills where downhill cycling may
  actually be faster), these times will represent the single mode of cycling
  only, but multi-modal times will generally reflect fastest times formed by
  combining multiple modes of transport.

Travel times measured these two ways are then combined to generate the
following two primary travel time statistics:

- *Absolute travel times* as the multi-modal travel times; that is, using any
  mode except private automobile.

- *Relative travel times* as the ratios of absolute travel times compared with
  equivalent travel times with private automobile. Relative travel times of
  less than one indicate that multi-modal transport is faster than equivalent
  transport with private automobile, while values greater than one indicate
  that private automobile transport is faster.

Intervals and Numbers of Transfers
==================================

In addition to travel times, UA also includes the following two additional
statistics quantifying other aspects of public transport systems. Both are
measured for every point of origin with a city, with final values again derived
by following the steps described above to obtain average values of each for all
trips of 10km distance. Numbers of transfers are thus the average number
required for all journeys of 10km, while intervals are the required waiting
times for the next equivalent journey out to that distance.

- *Intervals to Next Service* are measured in minutes. For each point of origin
  in a city, this statistic measures the waiting time necessary before
  departing to each destination within a city on the service after the one
  corresponding to the fastest journey. This delayed service may not be fast as
  the original, or it may even be faster in some cases, as the UA algorithms
  also prioritise connections with the fewest possible transfers. It can happen
  that subsequent services are actually faster, yet involve additional
  transfers not required in the originally identified "fastest" service.

- *Numbers of Transfers* measure the number of transfers necessary for a
  *minimal-transfer* journey out to a distance of 10km. These
  *minimal-transfer* journeys are selected to allow for journeys slightly
  slower than absolute fastest journeys (generally by up to 5 minutes) if they
  involve fewer transfers.

The Compound Travel Statistic
=============================

All three of the statistics described above - travel times, intervals, and
numbers of transfers - are measured such that lower values are more desirable.
Travel times are then directly multiplied by (a logarithmically-transformed
version of) intervals between services to generate a "*compound travel
statistic*". Low values of this statistic only arise in locations which have
fast travel times and short intervals between services. Low values may
accordingly always be interpreted as indicating overall good transport
services. In contrast, high values may arise through various combinations of
variables, from extremely high values of one single variable, to less extreme
combinations of the two variables. It is thus generally not possible to
directly discern reasons for high values of this compound travel statistic.
Urban Analyst nevertheless provides direct insight into all individual values,
as well as all pairwise combinations of values, permitting indirect insight.

Population density
******************

Population density values are taken directly from the `European Union *Global
Human Settlement Layer* <https://ghsl.jrc.ec.europa.eu/index.php>`_ data,
aggregated into polygons for maps, or across entire cities for statistics.

Distance to nearest schools
***************************

Distances to nearest schools are measured in kilometres, as shortest walking
distances from each point to the nearest school. These are network distances,
and not simple straight line distances. A single value is ascribed to each
point within a city, and all points aggregated after weighting by local
population densities.

Bicycle infrastructure
**********************

The bicycle infrastructure index is derived from a measure of the proportion of
all possible journeys from each point out to a fixed distance of five
kilometres that travel along dedicated bicycle infrastructure. To conform with
all other UA variables, the index is one minus this proportion, so that low
values reflect high proportions of bicycle infrastructure. Values of zero would
then reflect all journeys taken along dedicated bicycle paths, while values of
one would mean a complete absence of dedicated bicycle infrastructure.

Travel is calculated using a bicycle-specific algorithm that only extends along
ways unsuitable for bicycle travel where no alternatives exist. The weighting
scheme used adds total distances for all portions of travel along designated
cycleways that are separated from vehicular traffic. Portions of trips
extending along other types of ways are added with "half weightings" so, for
example, one kilometre along these types is equivalent to two kilometres on
dedicated bicycle ways. These "half-weight" ways include residential or
"living" streets, unpaved tracks, and bicycle lanes directly alongside
automobile lanes. A third category of ways are weighted at one-quarter,
including footpaths and general pedestrian areas which permit bicycle travel.
The precise weighting scheme can be viewed in `this source code file
<https://github.com/UrbanAnalyst/uaengine/blob/main/R/bicycle-infrastructure.R>`_.

The weighted sums of all distances along these types of ways traversed out to
five kilometres from any given point are then divided by the sum of all
distances travelled regardless of way type to give a ratio between zero and
one. This bicycle infrastructure index is then one minus this value.

Natural space accessibility
***************************

Natural space accessibility is measured in a similar way to the bicycle
infrastructure variable, except it quantifies proportions of walking distances
out to maximal distances of two kilometres that traverse natural spaces. This
provides a more realistic measure of natural space than simple aggregations of
areas, because it measures the ability of people to directly walk from every
point in a city through or alongside nearby natural spaces.

Moreover, aggregate metrics do not generally capture the ability of people to
actually access natural spaces. A park may, for example, have restricted or
even private access. This would count as a natural space in a simply aggregate
metric, yet not in UA because access restrictions are taken into account in the
routing algorithms.

The algorithm also measures lengths of ways walked adjacent to water -
so-called "blue space", providing a comprehensive metric of the actual ability
to access natural spaces from every point in a city. A natural space index of
zero would represent an entire city of natural space, with no built structures
at all, while a value of one would represent a complete absence of natural
spaces.

Parking index
*************

The parking index is the ratio of numbers of nearby parking spaces to total
volumes of nearby buildings. The parking statistic is calculated for each point
by adding all nearby parking spaces with a weighting scheme that decreases
exponentially with distance, so that nearby parking spaces count more than
parking spaces that are farther away. Building volumes are also aggregated
using an identical weighting scheme. The parking index at each point is then
the ratio of the sum of distance-weighted numbers of parking spaces to the sum
of distance-weighted total building volumes.

All publicly accessible parking spaces are counted, including on-street
parking, open parking lots, and multi-level parking garages. Building volumes
are aggregated regardless of type or purpose.

Housing value and rent
**********************

For USA cities only, additional statistics are provided for average housing
value per room, and average rental per room, both in US dollars.
