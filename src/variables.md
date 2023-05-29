# Variables

Almost all UA variables are measured such that lower or negative values are
good, whereas higher values are bad. For example, unemployment or transport
times are both better when values are lower. The only exceptions to this are
the indices of bicycle infrastructure and access to natural spaces, both of
which are quantified as proportions between 0 and 1, with higher values
respectively indicating either greater availability of bicycle infrastructure
or access to natural spaces.

## Socio-demographic variables

The extent and structure of each city is defined by its "socio-demographic
variable." These are taken from open-source datasets provided by the cities as
a series of geographic areas, defined as polygonal shapes, and some
corresponding measure of socio-demographic disadvantage. The cities themselves
decide the resolution and extent of these polygonal data, and with that the
spatial extent of UA analyses.

These socio-demographic variables are the only aspect that differs between
different cities. One of the simplest versions is unemployment rate, generally
measured as a percentage. The UA platform selects the most representative
measure of general social disadvantage provided by each city, and defaults to
rates of unemployment only where no more comprehensive of integrative measures
are openly provided by cities.

## Travel Statistics

Urban Analyst provides highly detailed statistics on transport systems. Many of
these are derived from estimates of times required to travel fixed distances of
10km. This value is chosen to capture the general efficiency of public
transport systems. Shorter distances do not sufficiently capture the influence
of transport modes such as express or long-distance train services, while
longer distances unfairly penalise smaller cities in which most journeys are
only of shorter distances.

Travel times are compared throughout for two primary modes of transport:

- *Private Automobile.* Travel times with private automobile are used as a
  benchmark for measures of travel time using other modes. UA generates
  realistic estimates of private automobile travel times through scaling to
  empirically observed data on actual vehicular travel times. Importantly, UA
  includes an additional, unique aspect of automobile travel times not
  quantified in any other equivalent system, through an algorithm to accurately
  estimate the likely time required to park a private vehicle, and then to walk
  to a desired destination. These parking times are crucial, as direct travels
  times alone to many inner-city destinations do not provide realistic
  estimates of actual journey times to locations where it may be impossible to
  actually park a private automobile.

- *Multi-Modal Transport.* All other UA travel times represent fastest
  possible times taken for journeys from every single point in a city to travel
  10km using any combination of transport modes excluding private automobile.
  The primary modes considered are walking, bicycling, and all available modes
  of public transport within each city. Where it is faster to cycle 10km than
  to take public transport (such as from locations with very poor public
  transport connections, or on the top of long hills where downhill cycling may
  actually be faster), these times will represent the single mode of cycling
  only, but multi-modal times will generally reflect fastest times formed by
  combining multiple modes of transport.

In addition to travel times, UA also includes the following two additional
statistics quantify other aspects of public transport systems. Both are
measured for every point of origin with a city, both of these are quantified by
measuring values for connections to every other location in the city, and by
calculating the average value at a distance of 10km. For example, numbers of
transfers generally increase with distance, and the value chosen represents the
average number of transfers required at a distance of 10km.

- *Intervals to Next Service,* measured in minutes. For each point of origin in
  a city, this statistic measures the waiting time necessary before departing
  to each destination within a city on the service after the one corresponding
  to the fastest journey. This delayed service may not be fast as the original,
  or it may even be faster in some cases, as the UA algorithms also prioritise
  connections with the fewest possible transfers. It can happen that subsequent
  services are actually faster, yet involve additional transfers not required
  in the originally identified "fastest" service.

- *Numbers of Transfers*. This measures the number of transfers necessary for a
  *minimal-transfer* journey out to a distance of 10km. These
  *minimal-transfer* journeys are selected to allow for journeys slightly
  slower than absolute fastest journeys (generally by up to 5 minutes) if they
  involve fewer transfers.

### Compound Travel Statistics

All three of the statistics described above - travel times, intervals, and
numbers of transfers - are measured such that low values are good, while high
values are bad. All three are then directly multiplied to generate a "*compound
travel statistic*". Low values of this statistic reflect only arise in
locations which have fast travel times, short intervals between services, and
few transfers. Low values may accordingly always be interpreted as good. In
contrast, high values may arise through various combinations of variables, from
extremely high values of one single variable, to less extreme combinations of
two or three of the variables. It is thus generally not possible to directly
discern reasons for high values of this compound travel statistic. The UA
nevertheless provides direct insight into all individual values, as well as all
pairwise combinations of values, permitting indirect insight.
