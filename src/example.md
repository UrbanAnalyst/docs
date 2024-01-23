# Example

This chapter demonstrates most of the capabilities of the [Urban Analyst
platform](https://urbananalyst.city) through exploring comparisons between the
cities of Paris, France, and Berlin, Germany. It is important to remember
throughout that lower values in all UTA statistics are always better. Values
are also weighted by local population densities. This is important because, for
example, public transport systems should be constructed to offer the fastest
services to the areas where most people live. Not implementing this weighting
would, in contrast, leave measures in some form of times per unit area, so that
for example travel times from unpopulated parts of a city would be weighted
equally to times from densely populated parts. Weighting travel times, and all
other UTA variables, by population density converts them to values as
experienced on average by each person in a city.

The comparisons in this chapter between Paris and Berlin are mostly drawn from
the "Stats" page, which provides overviews of entire cities, and comparisons
with all other UTA cities. The "Maps" page can then be used to examine the
actual spatial distributions of particular variables or relationships within
any given city.

This comparison starts by stepping through each variable to describe kinds of
information able to be extracted, before examining pairwise relationships
between these variables, and concluding with a general summary. The [Urban
Analyst platform](https://urbananalyst.city) currently measures 11 variables,
along with strengths of relationship between all paired combinations of these.
This amounts to 11 * (11 - 1) / 2 = 55 pairwise combinations. Strengths of
relationship are standardised, so are comparable throughout between all pairs
of variables, and between different cities.

## Individual Variables.

The following table summarises the values of the individual variables for each
city (each measured on its own distinct scale).

| Variable | Berlin | Paris |
|:----:|:---------|:---------|
| Times (abs; min) | 40.9 | 39.5 |
| Times (rel) | 1.09 | 1.03 |
| Num. Transfers | 0.9 | 1.5 |
| Intervals (min) | 6.9 | 4.9 |
| Transport | 33.2 | 25.5 |
| Pop. Dens. | 3 | 3 |
| School Dist (m) | 338 | 186 |
| Bike Index | 0.81 | 0.76 |
| Nature Index | 0.88 | 0.93 |
| Parking | 1.32 | 1.55 |

Social disadvantage is also quantified for all cities. However, each city
calculates this in different ways, and values are not comparable between
cities. Values are nevertheless standardised for the pairwise comparisons, and
strengths of relationship described there remain valid.

### Transport

The "Transport Absolute" variable measures the absolute time (in minutes)
required to travel a distance of 10km from each point in a city, using any
combination of travel modes except private automobile, including walking,
bicycling, and any available public transport options. Travelling 10km in
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

(Note that travel times with private automobiles include estimates of times
required to park a vehicle and ultimately walk to any desired destination.
Vehicular times calculated here are thus notably longer than with most
commercial routing engines, which give vehicular travel times only, and ignore
the critical need to park a vehicle and walk to a destination.)

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
times by intervals between services. Low values of this statistic reflect fast
and frequent transport. This statistic also indicates considerably superior
service in Paris compared with Berlin.

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
  opposite of the bicycle index. Paris provides relatively little
  access to natural spaces for anybody not close to one of the two huge parks
  in the city, whereas Berlin provides an abundance of generally smaller
  natural spaces dispersed throughout the city. Note that natural space access
  includes walks alongside water bodies. Both cities include dominant rivers,
  yet Berlin also provides greater pedestrian access to the banks of its rivers
  and canals. Comparison of this layer on the maps reveals the comparably
  greater access in Berlin to walking paths alongside canals and rivers,
  whereas most of the Seine in Paris is effectively inaccessible to
  pedestrians.
- "Parking": Finally, both Paris and Berlin offer relatively little opportunity
  to park private automobiles compared with the other UTA cities, with Berlin
  notably less than Paris.

## Relationships between variables

This section considers relationships between each individual variable and all
other variables. All strengths of relationship shown in the "Stats" page are
assessed in standardised ways, so they may be directly compared between cities.
Moreover, the scales shown in the "Stats" page may also be directly compared.
Values of one or greater indicate very strong relationships, whereas values
less than 0.1 or so indicate weak relationships, and values less than around
0.01 should generally be interpret to indicate no relationship. Pairs of
variables with very weak or negligible strengths of relationship are generally
not interpreted in the following sub-sections.

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
Relative transport times are only very weakly related to most other variables.
In contrast, absolute transport times are strongly related to most other
variables.

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

## Conclusions

### Lessons for Berlin

Paris's transport system is considerably faster and more frequent.
Nevertheless, it also involves greater numbers of transfers, suggesting that
any attempt to improve the system in Berlin should take care to avoid
inadvertently increasing numbers of transfers.

Berlin's average relative speed is also notably higher than Paris's, and at
1.09 likely too high to effectively discourage large numbers of people from
opting to travel via private automobile. Examination of the map of relative
travel times clearly reveals the effect of the connected ring out autobahns
encircling the city. While reducing speeds on these carriageways may not be
feasible, a uniform 30km/hour limit as introduced in Paris may nevertheless
significantly reduce this ratio, and further incentivise many more people to
opt for public transport rather than private automobile.

Although Paris is a far larger city, its average population density is
nevertheless very similar to Berlin's. It is then even more striking that Paris
offers considerably shorter average distances to schools than Berlin. School
distances in Berlin are also only weakly correlated with social conditions,
whereas average distances to schools in Paris are shorter in less socially
advantaged areas. Both of these factors indicate a need in Berlin for more
provision of local schooling in general, and particularly in socially
disadvantaged regions, if it is to match the educational opportunities provided
in Paris. 

Paris's bicycle infrastructure is considerably better than Berlin's, and
perhaps even more importantly, becomes better towards the inner city regions.
In contrast, Berlin really only offers good bicycle infrastructure in the
relatively peripheral, and more affluent, outer regions. Berlin really needs to
proactively focus on improving bicycle infrastructure in the inner city
regions.

Berlin is fortunately greatly enhanced by an abundance of natural space,
including access to the city's rivers and canals, and access to these natural
spaces is only weakly related to social advantage. This provides robust
evidence for Berlin to appreciate its natural spaces, and to ensure that they
remain accessible for everybody.

### Lessons for Paris

Paris's transport system is notably better than Berlin's in almost all ways
except for the number of transfers necessary to travel equivalent distances.
This difference is especially notable given that Paris is much larger than
Berlin. Improvements to Paris's public transport system should focus on
decreasing numbers of transfers.

Paris's average relative speed is very close to the "magical" value of one, at
which point private automobiles are no faster than multi-modal transport
including walking and cycling.

Paris has done a great job of providing bicycle infrastructure in the inner
city regions, and notably of proactively enhancing or creating bicycle
infrastructure in regions of social disadvantage.

Contrasts with Berlin nevertheless emphasise a couple of aspects which Paris
could focus on improving. The most notable of these is the index of
accessibility to natural spaces, and the relationship of this to other
variables. Paris simply has far less natural space than Berlin, and much poorer
general accessibility. Moreover, access to natural spaces is positively
associated with social advantage, so that it is relatively difficult for
socially disadvantaged Parisians to access natural spaces.
