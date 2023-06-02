# Example

This chapter demonstrates most of the capabilities of the [Urban Analyst
platform](https://urbananalyst.city) through exploring comparisons between the
cities of Paris, France, and Berlin, Germany. It is important to remember
throughout that lower values in all UTA statistics are always better. These
comparisons are mostly drawn from the "Stats" page, which provides overviews of
entire cities, and comparisons with all other UTA cities. The "Maps" page can
then be used to examine the actual spatial distributions of particular
variables or relationships within any given city.

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

