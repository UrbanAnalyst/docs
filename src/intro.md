# Introduction

This is the documentation for [Urban Analyst platform
(UA)](https://urbananalyst.city), providing open source analyses of urban
structure and function across the world. The source for this documentation can
be found in [this GitHub repository](https://githu.com/UrbanAnalyst/docs).

Urban Analyst provides [interactive maps](https://urbananalyst.city/maps) of
the properties of cities, including socio-demographic conditions and the
structure and function of transport systems. Each property is measured in terms
of a "variable". Relationships between individual variables are also analysed
and presented, such as between socio-demographic conditions and frequency of
transport services, or between distances to nearest schools and access to
natural spaces.

UA also provides [statistical summaries](https://urbananalyst.city/stats) of
all cities, enabling relationships between any pair of variables, such as
transport and socio-demographic disadvantage, to be compared across all UA
cities.

# How does it work?

Urban Analyst present a variety of [statistics](./variables.md) for each city
analysed, as well as relationships between these statistics. Values for each
statistic are derived at every street intersection in each city. These values
are then aggregated into the polygons shown in the ["Maps"
page](https://urbananalyst.city/maps), and across entire cities for the values
shown in the ["Stats" page](https://urbananalyst.city/stats). Aggregations are
always weighted by local population densities, to generate values representing
equivalent values *per person* as experienced in each city.

Details are provided in the [*Data Sources*](./data.md) and [*Software and
Algorithms*](./software.md) chapters.

# How many calculations are involved?

The values presented in Urban Analyst represent the first truly comprehensive
routing analyses for each city, derived from estimates of travel times from
every point in each city to every other point using any combination of possible
modes of transport. The following table summarises numbers of street
intersections, public transport ("PT") stops, and calculations for current
Urban Analyst cities.

 city    | intersections<br>(thousands) | PT stops | PT calcs<br>(millions) | routing calcs<br>(billions)
-------- | ------------- | -------- | -------- | -----------
Berlin   |      360      |   9,302  |      173 |  150
Hamburg  |      192      |   4,585  |       42 |   56
Mannheim |       44      |   1,107  |        2 |    8
Münster  |       44      |   1,554  |        5 |    6
London   |      506      |  20,072  |      806 |  160
Paris    |      313      |  29,393  |    1,728 |  124

One way to appreciate the scale of these calculations is through comparison
with commercial alternatives. One service, *traveltime.com*, charges a flat
subscription fee of €540 per month for a maximum of 60 requests per minute.
That rate would permit 31.5 million queries per year. The city of Hamburg, for
example, would then take almost 2,000 years to calculate, and would cost
€12 million. Google also offers a commercial routing service, limited to a
maximum of 500,000 queries per month, for a total price of US$2,000. At that
rate, the analyses for Hamburg would cost US$224 million.

The results presented in Urban Analyst are simply not possible using commercial
tools, or indeed any other open source tools. These analyses truly are uniquely
powerful, and provide a depth of insight into how people move through cities
not available in any other way.


# Can I access the full data?

Not directly, but feel free to open a [GitHub
issue](https://github.com/mpadge/UrbanAnalyst/issues) to start a discussion
about requesting full data sources.

# Structure

This documentation includes the following five chapters:

1. This introduction
2. ["Example"](./example.md): A walk-through example comparison between Berlin, Germany and Paris, France, illustrating the kinds of comparisons enabled by the Urban Analyst platform.
3. ["UTA Variables"](./variables.md): Providing descriptions of all variables included in the Urban Analyst platform.
4. ["Data Sources"](./data.md): Providing descriptions of all data sources used to derive these variables.
5. ["Software and Algorithms"](./software.md): Providing descriptions of, and links to, all software used to generate the UTA variables.

Contributions to, or questions regarding, this documentation, are welcome at
[this GitHub repository](https://githu.com/UrbanAnalyst/docs).
