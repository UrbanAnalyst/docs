# Example

This chapter demonstrates most of the capabilities of the [Urban Analyst
platform](https://urbananalyst.city) through exploring comparisons between the
cities of Paris, France, and Berlin, Germany. It is important to remember
throughout that lower values in all UTA statistics are always better. Values
are also weighted by local population densities. This is important because, for
example, public transport systems should be constructed to offer the fastest
services to the areas where most people live. Not implementing this weighting
would, in contrast, leave measures in some form of times per unit area,
weighting times from unpopulated parts of a city equally to times from very
densely populated parts. Weighting by population density effectively converts,
for example, transport times to the times averaged across each person in a
city.

The comparisons in this chapter between Paris and Berlin are mostly drawn from
the "Stats" page, which provides overviews of entire cities, and comparisons
with all other UTA cities. The "Maps" page can then be used to examine the
actual spatial distributions of particular variables or relationships within
any given city.

This comparison starts by stepping through each variable to describe kinds of
information able to be extracted, before concluding with a general summary. The
[Urban Analyst platform](https://urbananalyst.city) currently measures 11
variables, along with strengths of relationship between all paired combinations
of these. This amounts to 11 * (11 - 1) / 2 = 55 pairwise combinations. Four of
these variables quantify aspects of the transport system, and are considered
together in the following comparisons.

## Individual Variables.

### Transport

The "Transport Absolute" variable measures the absolute time (in minutes)
required to travel a distance of 10km from each point in a city, using any
combination of travel modes except private automobile (including walking,
bicycling, and any available public transport options). Travelling 10km in
Paris takes just under 40 minutes on average, while equivalent journeys in
Berlin require a bit over one minute more.

The "Transport Relative" values divide the absolute travel times described above
by times for equivalent journeys with private automobile. Ratios of one imply
automobile times equal to multi-modal times; ratios of less than one imply that
multi-modal transport is faster than private automobile. Paris and Berlin both
have comparably low values for this ratio, implying relatively fast multi-modal
transport, with Paris notably faster than Berlin.

All individual variables also enable comparison in terms of "Variation", rather
than "Average" values. Comparing these reveals that Berlin generally has
markedly lower variation than Paris. A comparison of these statistics on the
"Maps" page reveals that this is largely because Paris is simply much larger
than Berlin, and the ranges of both absolute and relative transport times are
correspondingly greater. The fact that relative transport in Paris is still
better on average than in Berlin is thus even more impressive considering this
stark difference in scale.

Travelling in Paris requires notably greater numbers of transfers to travel
equivalent distances than Berlin. The values in the "Number of Transfers" layer
are for journeys of 10km total distance (including walking or cycling distances
at either end). Travelling in Paris requires > 50% more transfers than journeys
in Berlin.

The fourth transport variable, "Interval", measures the time to wait (in
minutes) until the next equivalent service. Intervals in Paris are slightly
under 5 minutes, whereas values in Berlin are just under 7 minutes.

Finally, the "Compound Transport" variable simply multiplies absolute travel
times by numbers of transfers by intervals. Low values of this statistic
reflect fast and frequent transport with few transfers. Because of the
relatively high numbers of transfers necessary in Paris, it has a considerably
higher value of this statistic than Berlin.

### Other Variables

- "School Distance": Paris has notably shorter distances from each point in the
  city to the nearest school than does Berlin.
- "Bicycle Index": Paris has very notably better bicycle infrastructure than
  Berlin. This index is simply one minus the average portion of all bicycle
  journeys out to 5km from each point which may be taken on dedicated bicycle
  infrastructure. Around one quarter of all bicycle journeys in Paris may be
  taken along dedicated bicycle ways, compared to less than one fifth in
  Berlin. Moreover, comparing the maps for this variable reveal that the
  bicycle infrastructure in Berlin generally improves with distance away from
  the city centre, whereas Paris has the best bicycle infrastructure
  concentrated towards the centre of the city.
- "Nature Index": Access to natural spaces in the two cities is effectively the
  opposite of the bicycle index. Paris provides relative little
  access to natural spaces for anybody not close to one of the two huge parks
  in the city, whereas Berlin provides an abundance of generally smaller
  natural spaces dispersed throughout the city. Note that natural space access
  includes walks alongside water bodies. Both cities include dominant rivers,
  yet Berlin also provides greater pedestrian access to the banks of its river
  and canals.
- "Parking": Finally, both Paris and Berlin offer relatively little opportunity
  to park private automobiles compared with the other UTA cities, with Berlin
  slightly less than Paris.
