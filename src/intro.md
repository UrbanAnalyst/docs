# Introduction

This is the documentation for [Urban Analyst platform
(UA)](https://urbananalyst.city), providing open source analyses of urban
structure and function across the world.

Urban Analyst provides interactive maps of the properties of cities, including
socio-demographic conditions and the structure and function of transport
systems. Each property is measured in terms of a "variable". Relationships
between individual variables are also analysed and presented, such as between
socio-demographic conditions and frequency of transport services, or between
distances to nearest schools and access to natural spaces.

UA also provides statistical summaries of all cities, enabling relationships
between any pair of variables, such as transport and socio-demographic
disadvantage, to be compared across all UA cities.

# Variables

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

Most statistics of the UTA are derived from estimates of times required to
travel a fixed distance of 10km. This value is chosen to capture the general
efficiency of public transport systems. Shorter distances do not sufficiently
capture the influence of transport modes such as express or long-distance train
services, while longer distances unfairly penalise smaller cities in which most
journeys are only of shorter distances.

Travel times are compared throughout for two primary modes of transport:

- *Private Automobile.* Travel times with private automobile are used as a
  benchmark for measures of travel time using other modes. The UTA generates
  realistic estimates of private automobile travel times through scaling to
  empirically observed data. Importantly, the UTA includes an additional,
  unique aspect of automobile travel times not quantified in any other
  equivalent system, through an algorithm to accurately estimate the likely
  time required to park a private vehicle, and then to walk to a desired
  destination. These parking times are crucial, as direct travels times alone
  to many inner-city destinations do not provide realistic estimates of actual
  journey times to locations where it may be impossible to actually park a
  private automobile.

- *Multi-Modal Transport.* All other UTA travel times represent fastest
  possible times taken for journeys from every single point in a city to travel
  10km using any combination of transport modes excluding private automobile.
  The primary modes considered are walking, bicycling, and all available modes
  of public transport within each city. Where it is faster to cycle 10km than
  to take public transport (such as from locations with very poor public
  transport connections, or on the top of long hills where downhill cycling may
  actually be faster), these times will represent the single mode of cycling
  only, but multi-modal times will generally reflect fastest times formed by
  combining multiple modes of transport.
