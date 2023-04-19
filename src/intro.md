# Introduction

Documentation for [Urban Analyst platform](https://urbananalyst.city),
providing open source analyses of urban transport systems across the world.

Urban Transport Analyst provides interactive maps of the properties of urban
transport systems, and relationships of these properties to socio-demographic
conditions.  UTA also provides statistical summaries of all cities, including
representation in the "UTA Index", which captures the extent to which transport
systems effectively counter-balance socio-demographic disadvantage.

## Travel Times and Modes of Transport

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
