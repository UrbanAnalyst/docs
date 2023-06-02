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

The following table summarises the values of the individual
variables for each city.

| Variable | Berlin | Paris |
|:----:|:---------|:---------|
| Times (abs; min) | 40.9 | 39.5 |
| Times (rel) | 1.09 | 1.03 |
| Num. Transfers | 0.9 | 1.5 |
| Intervals (min) | 6.9 | 4.9 |
| Transport | 30.1 | 36.6 |
| Pop. Dens. | 3 | 3 |
| School Dist (km) | 2.2 | 1.5 |
| Bike Index | 0.81 | 0.76 |
| Nature Index | 0.88 | 0.93 |
| Parking | 1.32 | 1.55 |

### Transport

The "Transport Absolute" variable measures the absolute time (in minutes)
required to travel a distance of 10km from each point in a city, using any
combination of travel modes except private automobile (including walking,
bicycling, and any available public transport options). Travelling 10km in
Paris takes under 40 minutes on average, while equivalent journeys in
Berlin require almost 1.5 minutes more.

The "Transport Relative" values divide the absolute travel times described above
by times for equivalent journeys with private automobile. Ratios of one imply
automobile times equal to multi-modal times; ratios of less than one imply that
multi-modal transport is faster than private automobile. Paris and Berlin both
have comparably low values for this ratio, implying relatively fast multi-modal
transport, with Paris notably faster than Berlin. This is likely influenced by
Paris's recent introduction of a uniform maximum speed limits of 30km/hour
through the city, whereas Berlin features a number of "autobahns" with much
higher speed limits.

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
  notably less than Paris.

## Relationships between variables

This section considers relationships between each individual variable and all
other variables. The first section thus considers relationships between
absolute transport times and all 10 other variables; the second then considers
relationships with the 9 remaining variables not previously considered, and so
on.

All strengths of relationship shown in the "Stats" page are assessed in
standardised ways, so they may be directly compared between cities. Moreover,
the scales shown in the "Stats" page may also be directly compared. Values of
one or greater indicate very strong relationships, whereas values less than 0.1
or so indicate weak relationships, and values less than around 0.01 should
generally be interpret to indicate no relationship. Pairs of variables with
very weak or negligible strengths of relationship are generally not interpreted
in the following sub-sections.

The following table summarises the values of the strongest pairwise
relationships for each city:

| Variable1 | Variable2 | Berlin | Paris |
|:------:|:----:|:---------|:---------|
| Times (abs) | Bike |  1.0 |  2.0 |
| Times (abs) | Natural |  -1.0 |  -0.5 |
| Times (abs) | Parking |  0 |  -0.15 |
| Times (abs) | Pop. Dens. |  -0.15 |  -0.11 |
| Times (abs) | School dist |  0.12 |  0.06 |
| Times (abs) | Transfers |  -0.31 |  -0.48 |
| Times (rel) | Bike |  0 |  0.16 |
| | | |
| Transport | Natural |  -0.22 |  2.46 |
| Transport | Parking |  1.7 |  1.9 |
| | | |
| School dist | Bike | 0  |  0.4 |
| School dist | Natural |  -0.12 |  -0.06 |
| | | |
| Social | Bike |  0.52 |  -0.38 |
| Social | Natural |  -0.1 |  2.0 |
| Social | Parking |  0.04 |  -2.18 |
| Social | School dist |  -0.05 |  -0.25 |


### Transport Variables

This sub-section only considers transport times, both in absolute and relative
sense. The other transport variables, of intervals and numbers of transfers,
generally follow similar patterns and are not explicitly considered here.

Relative transport times are ratios of absolute times with multi-modal
transport compared with equivalents times with private automobiles. This
variable is only very weakly related to most others. In contrast, absolute
transport times are strongly related to most other variables.

Relative transport times are negligibly associated with population densities,
while absolute times are particularly strongly and negatively correlated. These
negative relationships indicate that faster transport is associated with higher
population densities, more so in Berlin than Paris.

Slightly weaker relationships are manifest between absolute travel times and
distances to nearest schools. Relationships in both Berlin and Paris are
positive, indicating that fast public transport is positively associated with
shorter distances to schools, with the relationship about twice as strong in
Berlin as in Paris.

Travel times are very strongly, and positively, correlated with bicycle
infrastructure, indicating faster travel times in regions with better bicycle
infrastructure. This relationship is much stronger in Paris than in Berlin, for
reasons easy to discern by looking at the maps of Berlin for these two
variables. Bicycle infrastructure there is much better in the periphery of the
city, whereas transport times exhibit more of a systematic discrepancy between
the east (fast) and west (slow) portions of the city. In Paris, in contrast,
faster transport times and better bicycle infrastructure are both concentrated
more towards the centre of the city.

Relationships between transport times and the index of accessibility to natural
spaces are also very strong, and negative. This means that faster transport
times are associated with lower accessibility to natural spaces, as might be
generally expected of most high-density cities. The relationship is stronger in
Berlin than Paris, indicating that faster transport times are most strongly
associated with poorer access to natural spaces there than in Paris.

Finally, absolute transport times are slightly negatively associated with
numbers of automobile parking spaces in Paris, whereas there is no relationship
in Berlin. This negative relationship indicates that regions with faster public
transport also tend to have more automobile parking spaces, reflecting planning
decisions that associate use of public transport with the driving of private
automobiles. No such relationship appears to exist in Berlin.

### Non-Transport Variables

Shorter school distances are positively associated with the bicycle index in
Paris, indicating a positive association between good bicycle infrastructure
and short distances to schools. Berlin manifests no such relationship, likely
for reasons described above, that bicycle infrastructure in Berlin is generally
more peripheral than in Paris.

Although much weaker, relationships between schools distances and the index of
accessibility to natural spaces are negative, indicating that locations closer
to schools are further from nature, and more so in Berlin than in Paris.

Finally, the social variables are more strongly related to all other
non-transport variables in Paris than in Berlin, except for with the index of
bicycle infrastructure. This variable is more strongly, and positively,
correlated with the social indicator in Berlin than in Paris, where the
relationship is negative. The positive relationship in Berlin indicates that
the provision of bicycle infrastructure is positively associated with social
advantage, an effect again readily seen in examining the map of Berlin. In
contrast, Paris is more effective in providing bicycle infrastructure in areas
of relative social disadvantage.

Paris also seems to be more effective in educational provision in areas of
social disadvantage, with the strong negative correlation indicating that
socially disadvantaged Parisians generally have to travel shorter distances to
schools. Although this relationship is also negative in Berlin, it is much
weaker.

In contrast, Paris's very strong and positive relationship between social
advantage and access to natural spaces indicates the relatively far greater
difficulty experienced by less socially advantaged Parisians in accessing
natural spaces compared with equivalent inhabitants of Berlin.

Finally, Paris manifests a very strong and negative association between social
advantage and numbers of automobile parking spaces, indicating that low social
disadvantage is strongly associated with high numbers of automobile parking
spaces, or conversely that socially disadvantaged parts of the city offer
relatively few automobile parking spaces. The relationship in Berlin is, in
contrast, slightly positive.
